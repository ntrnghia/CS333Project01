Author:
1651025 - Nguyen Trung Nghia
1651071 - Nguyen Truong Hoang Phuc
This is our source code to build kernel module to generate random number. The folder includes 5 files: understand.docx, Kbuild, Makefile, ran.c, README.
How to build:
- make
- sudo insmod ran.ko		//insert module
- lsmod | grep ran		//list module is running
- ls -l /dev/mynull		//list to check /dev/mynull
- sudo -i			//switch to root mode
- echo 8 > /dev/mynull		//write 8 to buffer
- dmesg | tail			//read tail messege from module
- cat /dev/mynull		//read 8 from buffer
- dmesg | tail			//read tail messege from module
- exit				//exit to root mode
- sudo rmmod ran.ko		//remove module
- lsmod | grep ran		//check wheather module is running
- make clean			//clean folder
