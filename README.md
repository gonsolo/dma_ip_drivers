# Xilinx DMA IP Reference drivers

These drivers were taken from <https://github.com/Xilinx/dma_ip_drivers> and
updated for the latest kernel (6.8.9). They work on Arch Linux as of 2024-05-09.

# Build and install

`cd xdma/xdma'
`sudo make -j8 clean install`

# Use
`rmmod xdma`
`sudo modprobe xdma poll_mode=1 interrupt_mode=2` or just `sudo modprobe xdma`
