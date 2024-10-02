# Xilinx DMA IP Reference drivers

These drivers were taken from <https://github.com/Xilinx/dma_ip_drivers> and
updated for the latest kernel (6.11.1). They work on Arch Linux as of 2024-10-02.

# Build and install

`cd xdma/xdma'
`sudo make -j8 clean install`

# Use
`sudo rmmod xdma`
`sudo modprobe xdma poll_mode=1 interrupt_mode=2` or just `sudo modprobe xdma`

I had to boot with kernel parameters `pci=nomsi` because of `config bar not found`.

To use it as a non-root user:
`sudo chmod a+rw /dev/xdma0_*`
