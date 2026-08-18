# Mstar stuff
## Reverse engineering
- msc313e etc camera pipeline, in progress, claude RE'd/modelled it in QEMU
- ssd202d h246 decoder

## Mainline

## Miyoo

# M68K stuff
## Amiga
- Clean up, resend mediator
- Test PCI bounce buffer on A4000
- Test Geforce 6200 "everything is VRAM" on A4000
- Get mah boi claude to whip a module to boot the sonnet g3 card and load linux onto it. (In progress)
- nommu linux on amiga.

## MAC
- Finish up bootable u-boot CD/HD image thing.

## MVME147
- Write new u-boot SPL with autoboot to EPROMs

## E17
- Get new u-boot to boot. (Partially done, claude fixed the uart issues?)
  - wip: https://github.com/fifteenhex/u-boot/tree/e17
- Get linux to boot (Done, this uart SUUUUCKS)
- Add SMP support (DONE! BOOM!)
```
e17:/# cat /proc/interrupts 
            CPU0       CPU1       
   4:          0      21640  auto            vicclock-cpu1
   6:          0        218  auto            ipi-mailbox
   8:        286          0  user        8  ipi-icms
  10:      21487          0  user       10  vicclock-cpu0
 200:         54          0  VIC068A    19  ttyS
 201:          0          0  VIC068A    16  ttyS-rxexc
 202:      11933          0  VIC068A     4  e17-frame
 203:        647          0  VIC068A     7  eth0
 204:          0          0  VIC068A     1  e17-kbd
 ERR:          0
e17:/# cat /proc/cpuinfo 
processor       : 0
CPU:            68040
MMU:            68040
FPU:            68040
Clocking:       31.8MHz
BogoMips:       21.24
Calibration:    106240 loops
processor       : 1
CPU:            68040
MMU:            68040
FPU:            68040
Clocking:       31.8MHz
BogoMips:       21.24
Calibration:    106240 loops
e17:/#
```

## u-boot virt
- Clean up virt booting series, resend

# nolibc
- set dirfd().
- send sendfile() series
- rework, send static pie series.
