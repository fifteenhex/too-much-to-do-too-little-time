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

## MVME147
- Write new u-boot SPL with autoboot to EPROMs

## E17
- Get new u-boot to boot. (Partially done, claude fixed the uart issues?)
  - wip: https://github.com/fifteenhex/u-boot/tree/e17
- Get linux to boot
- Add SMP support

## u-boot virt
- Clean up virt booting series, resend

# nolibc
- set dirfd().
- send sendfile() series
- rework, send static pie series.
