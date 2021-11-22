obj-m += lkm_example.o
all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules
clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

test:
	sudo insmod lkm_example.ko
	sudo rmmod lkm_example.ko
	dmesg | tail

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean

setup:
	sudo mknod /dev/lkm_example c 236 0
