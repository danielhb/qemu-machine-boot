# RISC-V tests innfo

## Supported machines

* `virt` machine, both 32 and 64 bit

## Building

The images were created with buildroot @ 7e9929e9a826d9:

https://github.com/buildroot/buildroot.git

The 32 bit 'virt' image was created using:

```
make qemu_riscv32_virt_defconfig && make
```

And the 64 bit 'virt' image:

```
make qemu_riscv64_virt_defconfig && make
```

