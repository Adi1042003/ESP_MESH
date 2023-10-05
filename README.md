# ScaleBot Mesh Network with ESP's and PainlessMesh

This project demonstrates a simple mesh network using Arduino and the PainlessMesh library. The network consists of multiple nodes that can exchange JSON data with each other. This README provides an overview of the code and how to set up and use the network.

## Prerequisites

To run this project, you will need:

- Arduino IDE installed on your computer.
- The PainlessMesh library installed in your Arduino IDE.
- Basic knowledge of Arduino programming.

## Components

- ESP32/ESP8266 (multiple nodes).
- PainlessMesh library.
- ArduinoJson library.

## Getting Started

1. Clone or download this repository to your local machine.

2. Open the Arduino IDE.

3. Ensure that you have installed the required libraries:
   - PainlessMesh library
   - ArduinoJson library

4. Connect your Arduino boards to your computer.

5. Open the `ScaleBot_Mesh_Node.ino` and `ScaleBot_Mesh_Gateway.ino` files in separate Arduino IDE windows for each node and the gateway.

6. Configure the settings in the code:
   - Set the `MESH_PREFIX` to your desired network name.
   - Set the `MESH_PASSWORD` to your desired network password.
   - Set the `MESH_PORT` to the communication port for the mesh network (default is 5555).

7. Upload the code to each Arduino board, ensuring that you select the correct board and port for each one.

8. After uploading the code to all nodes, open the serial monitor for each node to monitor the network activity.

## How It Works

- The network consists of one gateway node and multiple client nodes.
- Each client node sends JSON data containing sensor information to the gateway node.
- The gateway node receives the JSON data and parses it to extract sensor values.
- The extracted values are printed on the serial monitor of the gateway node.

## Code Structure

- `ScaleBot_Mesh_Node.ino`: Code for the client nodes.
- `ScaleBot_Mesh_Gateway.ino`: Code for the gateway node.
- `painlessMesh.h`: The PainlessMesh library for mesh networking.
- `ArduinoJson.h`: The ArduinoJson library for JSON parsing.

## Usage

1. Upload the `ScaleBot_Mesh_Gateway.ino` code to one of the Arduino boards. This board will act as the gateway.

2. Upload the `ScaleBot_Mesh_Node.ino` code to the remaining Arduino boards. These boards will act as client nodes.

3. Monitor the serial output of the gateway node to view the received JSON data from client nodes.

4. Client nodes will periodically send JSON data containing sensor information to the gateway node.

5. Customize the sensor data and transmission intervals in the `sendJsonData` function of the client node code.

6. Experiment with different sensor values and node configurations as needed for your project.

## Contributing

If you find any issues with this code or have suggestions for improvements, please feel free to contribute by opening an issue or submitting a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
