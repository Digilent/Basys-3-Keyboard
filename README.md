Basys 3 Keyboard Demo
==============
 [Link to the project wiki](https://reference.digilentinc.com/learn/programmable-logic/tutorials/basys-3-keyboard-demo/start)
Introduction
--------------
This project is a Verilog demo using the Basys 3, USB HID Host with keyboard and the USB UART. When programmed onto the board, the user presses a key on the keyboard, this sends a keyboard PS/2 scan code to the Basys3 over the USB-HID port. This scan code is read and transmitted to a terminal application via the USB-UART bridge. When the key is released, a scan code of F0XX is transmitted, indicating that the key with PS/2 code XX has been released.
 
 Requirements
--------------
* **Basys 3**: [Store Link](https://store.digilentinc.com/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/)
* **Vivado 2018.2 Installation**: See [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start) to learn how to get Vivado.
* **Serial Terminal Emulator**: See [Installation and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term) for more information.
* **MicroUSB Cable**: For programming the Basys 3
* **USB Keyboard**

 Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Basys-3-Keyboard/releases).
2. Open the project in Vivado 2018.2 by double clicking on the included XPR file found at "\<archive extracted location\>/vivado_proj/basys-3-Keyboard.xpr".
3. In the *Flow Navigator* panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug a Basys 3 into the computer running Vivado using a MicroUSB cable.
5. Open a serial terminal application (such as TeraTerm) and connect it to the Basys 3's serial port, using a baud rate of 9600.
6. Click "Open target" in the green bar at the top of the window. Select "Auto connect" from the drop down menu.
7. Click "Program device" in the green bar at the top of the window. In the "Program Device" wizard, enter "\<archive extracted location\>vivado_proj/Basys-3-Keyboard.runs/impl_1/top.bit" into the "Bitstream file" field. Then click **Program**.
8. The demo will now be programmed onto the Basys 3. See the *Introduction* section of this README for a description of how to interact with this demo.
 Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project. Check out the Basys 3's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/basys-3/start?redirect=1) to find more documentation, demos, and tutorials.
 Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)
