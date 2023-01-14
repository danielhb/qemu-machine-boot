# QEMU boot tester

Run a test doing a basic boot with network and poweroff for QEMU
machines.

At this moment it is supported ARM Aspeed and RISC-V virt. Check
the README file for each architecture for more info.

## Run

For all ARM tests, simply run :

```
$ ./boot.sh -q --prefix=/path/to/qemu/install/ arm
ast2500-evb - buildroot-2022.05/flash.img : FW Linux /init net login poweroff PASSED
ast2500-evb - buildroot-2022.11-2-g15d3648df9/flash.img : FW Linux /init net login poweroff PASSED
ast2600-evb - buildroot-2022.05/flash.img : FW Linux /init net login poweroff PASSED
ast2600-evb - buildroot-2022.11-2-g15d3648df9/flash.img : FW Linux /init net login poweroff PASSED
```

And for all RISC-V tests :

```
$ ./boot.sh -q --prefix=/path/to/qemu/install/ riscv
virt32 - buildroot/rootfs.ext2 : Linux /init net login poweroff PASSED
virt64 - buildroot/rootfs.ext2 : Linux /init net login poweroff PASSED
```

For a simple machine with a verbose output, run

```
$ ./boot.sh --prefix=/path/to/qemu/install/ <arch> <machine>
```
