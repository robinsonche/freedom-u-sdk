# freedom-u-sdk
Freedom Unleashed Software Development Kit

The original file has no README about how to compiler it, here I list the procedure as following:
I do it on a Ubuntu 16.06 64 bit desktop .

1. install packages

sudo apt-get install autoconf automake autotools-dev curl libmpc-dev libmpfr-dev libgmp-dev libusb-1.0-0-dev gawk build-essential bison flex texinfo gperf libtool patchutils bc zlib1g-dev device-tree-compiler pkg-config libexpat-dev

2. use git  to pull submodules, this will take a long time to wait the files get downloaded,  I failed my times to get the file, however the situation is better in midnight,
I get a whole night to get all files.  P.S: I'm in China, hahha....

git submodule update --init --recursive


3.after that in top directory:

make all

This command will automatically build the kernel, tool chain, rootfs for you, and download something...

4.after the above command finished, the kernel will be ready, any error will prohibit the next step.
again in top directory:

make qemu

This command will build the simulation machine for you, and will download a lot of files again.
But in China, as you known you can't download it, so use a proxy will help you finish the process.

5.when the qemu runs, it will display the kernel running information.

Note: I try to run "make sim" in top directory, the command use another simulator 'spike', but the kernel failed boot at lack of Uart...
I don't know why, maybe bugs still in spike.

Ok, Enjoy the Process.



