
obj-m += hello-1.o

KERNELDIR ?= /lib/modules/$(shell uname -r)/build
PWD       := $(shell pwd)
# EXTRAVERSION=-arch1-1

all: build
	#make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

build:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules

install:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules_install

clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
