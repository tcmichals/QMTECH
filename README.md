# What is this?
QMTECH Zynq 7020 FPGA board files to create a linux distro using buildroot

# Basic How to
How to create an Linux distro using buildroot

mkdir -p projects/qmtech
cd projects/qmtech
git clone  --recurse-submodules https://github.com/tcmichals/QMTECH.git \
git clone https://gitlab.com/buildroot.org/buildroot.git \
mkdir bld \
cd bld \
make -C ../buildroot/ O=$PWD BR2_EXTERNAL=$PWD/../QMTECH/zynq_qmtech_xc720 zynq_qmtech_xc720_defconfig \
make

# Articles
https://www.hackster.io/MichalsTC/zynq-fpga-board-using-buildroot-a6c63a
