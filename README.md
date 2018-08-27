Basys 3 Keyboard Demo
==============

Description
--------------
This project is a Vivado demo using the Basys 3's USB HID Host port and USB UART bridge, written in Verilog. When programmed onto the board, whenever the user presses a key on a keyboard connected to the USB HID port (J2, labeled "USB"), a scan code is sent to the Basys3 through a PS/2 interface. This scan code is read and transmitted to a serial terminal emulator application via the USB-UART bridge. When the key is released, a scan code of 0xF0XX is transmitted, indicating that the key with PS/2 code "XX" has been released.

For example: If the user presses the space bar on a keyboard connected to the Basys 3, the scan code "29" will be sent to and printed with the connected serial terminal emulator.  When the space bar is released, "F0 29" will be printed.

Requirements
--------------
* **Basys 3**: To purchase a Basys 3, see the [Digilent Store](https://store.digilentinc.com/basys-3-artix-7-fpga-trainer-board-recommended-for-introductory-users/)
* **Vivado 2018.2 Installation**: To learn how to get Vivado, see the [Installing Vivado and Digilent Board Files Tutorial](https://reference.digilentinc.com/vivado/installing-vivado/start).
* **Serial Terminal Emulator**: For more information, see the [Installating and Using a Terminal Emulator Tutorial](https://reference.digilentinc.com/learn/programmable-logic/tutorials/tera-term).
* **MicroUSB Cable**
* **USB Keyboard**

Demo Setup
--------------
1. Download and extract the most recent release ZIP archive from this repository's [Releases Page](https://github.com/Digilent/Basys-3-Keyboard/releases).
2. Open the project in Vivado 2018.2 by double clicking on the included XPR file found at "\<archive extracted location\>/vivado_proj/Basys-3-Keyboard.xpr".
3. In the *Flow Navigator* panel on the left side of the Vivado window, click **Open Hardware Manager**.
4. Plug a Basys 3 into the computer running Vivado using a MicroUSB cable.
5. Open a serial terminal emulator (such as TeraTerm) and connect it to the Basys 3's serial port, using a baud rate of 9600.
6. Click "Open target" in the green bar at the top of the window. Select "Auto connect" from the drop down menu.
7. Click "Program device" in the green bar at the top of the window. In the "Program Device" Wizard, enter "\<archive extracted location\>vivado_proj/Basys-3-Keyboard.runs/impl_1/top.bit" into the "Bitstream file" field. Then click **Program**.
8. The demo will now be programmed onto the Basys 3. See the *Introduction* section of this README for a description of how this demo works.

Next Steps
--------------
This demo can be used as a basis for other projects, either by adding sources included in the demo's release to those projects, or by modifying the sources in the release project.

Check out the Basys 3's [Resource Center](https://reference.digilentinc.com/reference/programmable-logic/basys-3/start) to find more documentation, demos, and tutorials.

If there are any issues with running this demo, contact Digilent Support through the FPGA section of the [Digilent Forum](https://forum.digilentinc.com).

Additional Notes
--------------
For more information on how this project is version controlled, refer to the [Digilent Vivado Scripts Repository](https://github.com/digilent/digilent-vivado-scripts)
