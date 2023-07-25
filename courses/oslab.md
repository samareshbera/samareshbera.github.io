Note: This page is created based on https://www.ccs.neu.edu/home/skotthe/classes/cs5600/fall/2016/labs/pintos-setup.html

**Virtual Machine Setup**

-- Create a Linux virtual machine (VM) using [Virtual Box](https://www.virtualbox.org/)

-- Check whether the installation is successful

**PintOS installation and Setup**

1. **Download and Install**
   
   a) Download the PintOS source files using:
   
   `wget https://samareshbera.github.io/files/pintos-src.tgz`

   Note: `wget` will store the file in the same directory from which you run `wget`. Let's consider the directory as `PINTOS_DOWNLOAD_PATH`.

   b) Extract the PinOS source file using:

   `tar xvzf PINTOS_DOWNLOAD_PATH/pintos-src.tgz`

   c) Adding PintOS programs to `PATH`:

    `sudo .bashrc` and add `$PINTOS_HOME/pintos/src/utils`

      Note: `PINTOS_HOME = /home/` in this case

    For example, `PATH=/usr/local/bin:$PATH:/home/pintos/src/utils`

   d) Configure `gdb` macros to use `gdb` with PintOS. The macros are stored in `$PINTOS_HOME/pintos/src/utils/pintos-gdb`

      * Go to `$PINTOS_HOME/pintos/src/utils/`

      * Open `pintos-gdb` using `gedit pintos-gdb`

      * Change `GDBMACROS` as follows: `GDBMACROS=$PINTOS_HOME/pintos/src/misc/gdb-macros`

   e) Go to `$PINTOS_HOME/pintos/src/utils` and build PintOS using `make`

   f) We will use `qemu` emulator in this course. To do so, change the following:

      * Go to `$PINTOS_HOME/pintos/src/threads`
   
      * Open `Make.vars` using `gedit Make.vars`
   
      * Change `SIMULATOR = --bochs` to `SIMULATOR = --qemu`
      
   
3. **Running PintOS Test-Cases**



