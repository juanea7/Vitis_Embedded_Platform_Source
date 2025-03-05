Read the other README for info about the platform.

To build the whole platform (HW and SW) you have to follow this steps:

1. Prepare environment

source /tools/Xilinx/Vitis/2024.2/settings64.sh

2. Build the HW in this folder

make xsa

3. Build the petalinux project with its makefile
   Remember to copy there the generate XSA (hw/build/hw.xsa), you'll need it

4. Build the whole infrastructure (HW and SW) after petalinux project finishes successfully

make all PREBUILT_LINUX_PATH=<path to petalinux project>/build/petalinux/images/linux

(this will just create the SW since the xsa makefile rule has already been built)

* The folder "./platform_repo/xilinx_zcu102_monitor_dfx_202420_1/export/xilinx_zcu102_monitor_petalinux_dfx_202420_1" can be used as a Vitis platform
(maybe copy it on other place to keep it safe)

