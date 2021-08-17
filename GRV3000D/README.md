# Introduction

Run this for GRV3000D on ArtyA7-100T board

After connecting the board to a Windows PC, please make sure the COM port for the board is determined by looking it up in the Device Manager.

Under Cygwin, the COM port mapping is like:

COM1 - /dev/ttyS0
COM2 - /dev/ttyS1
COM3 - /dev/ttyS2
COM4 - /dev/ttyS3
COM5 - /dev/ttyS4

And setup the COM port for LOAD and RUN in core_portme.mak
Please also install pyserial under Cygwin pip3 install pyserial

# Clean

make clean PORT_DIR=GRV3000D

# Building and Running

	% make XCFLAGS="-DPERFORMANCE_RUN=1" REBUILD=1 PORT_DIR=GRV3000D run1.log
	% make XCFLAGS="-DVALIDATION_RUN=1" REBUILD=1 PORT_DIR=GRV3000D run2.log
