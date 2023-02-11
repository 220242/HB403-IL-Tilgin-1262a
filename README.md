```
# cat /proc/version
Linux version 2.6.32.42 (lajo@tilgin00144) (gcc version 4.3.3 (GCC) ) #1 Fri May 5 10:43:41 CEST 2017
```

```
# cat /proc/mtd
dev:    size   erasesize  name
mtd0: 00080000 00020000 "U-Boot"
mtd1: 07f80000 00020000 "ubi"
mtd2: 00000076 0001f800 "test_data"
mtd3: 0017a000 0001f800 "old.kernel"
mtd4: 0111a800 0001f800 "sam"
mtd5: 01255800 0001f800 "old.rootfs"
mtd6: 00001f00 0001f800 "Environment"
mtd7: 0001f800 0001f800 "old.appfs"
mtd8: 0017a000 0001f800 "kernel"
mtd9: 01255800 0001f800 "rootfs"
mtd10: 0001f800 0001f800 "appfs"
mtd11: 0001f800 0001f800 "caldata"
mtd12: 00003000 0001f800 "Config-C"
mtd13: 00008000 0001f800 "Config-A"
mtd14: 00007000 0001f800 "Log"
mtd15: 00001000 0001f800 "Misc-A"
```
```
# cat /proc/cpuinfo
system type             : VR9
processor               : 0
cpu model               : MIPS 34Kc V5.6
BogoMIPS                : 332.59
wait instruction        : yes
microsecond timers      : yes
tlb_entries             : 16
extra interrupt vector  : yes
hardware watchpoint     : yes, count: 4, address/irw mask: [0x0ffc, 0x0ffc, 0x0ff8, 0x0ffb]
ASEs implemented        : mips16 dsp mt
shadow register sets    : 1
core                    : 0
VCED exceptions         : not available
VCEI exceptions         : not available
```
```
# cat /proc/diskstats
   7       0 loop0 0 0 0 0 0 0 0 0 0 0 0
   7       1 loop1 0 0 0 0 0 0 0 0 0 0 0
   7       2 loop2 0 0 0 0 0 0 0 0 0 0 0
   7       3 loop3 0 0 0 0 0 0 0 0 0 0 0
   7       4 loop4 0 0 0 0 0 0 0 0 0 0 0
   7       5 loop5 0 0 0 0 0 0 0 0 0 0 0
   7       6 loop6 0 0 0 0 0 0 0 0 0 0 0
   7       7 loop7 0 0 0 0 0 0 0 0 0 0 0
  31       0 mtdblock0 0 0 0 0 0 0 0 0 0 0 0
  31       1 mtdblock1 0 0 0 0 0 0 0 0 0 0 0
  31       2 mtdblock2 0 0 0 0 0 0 0 0 0 0 0
  31       3 mtdblock3 0 0 0 0 0 0 0 0 0 0 0
  31       4 mtdblock4 0 0 0 0 0 0 0 0 0 0 0
  31       5 mtdblock5 0 0 0 0 0 0 0 0 0 0 0
  31       6 mtdblock6 0 0 0 0 0 0 0 0 0 0 0
  31       7 mtdblock7 0 0 0 0 0 0 0 0 0 0 0
  31       8 mtdblock8 0 0 0 0 0 0 0 0 0 0 0
  31       9 mtdblock9 454 7266 15440 2730 0 0 0 0 0 2700 2730
  31      10 mtdblock10 0 0 0 0 0 0 0 0 0 0 0
  31      11 mtdblock11 1 1 8 0 0 0 0 0 0 0 0
  31      12 mtdblock12 4 8 24 0 0 0 0 0 0 0 0
  31      15 mtdblock15 3 0 6 0 0 0 0 0 0 0 0
  31      13 mtdblock13 0 0 0 0 0 0 0 0 0 0 0
  31      14 mtdblock14 0 0 0 0 0 0 0 0 0 0 0
```

```
# cat /etc/passwd
root:$1$q15RrcVp$8S2kplj9i7e3NfEJ3MS.Z/:0:0:root:/root:/bin/sh
nobody:x:65534:65534:nobody:/nonexistent:/bin/false
storage_guest:x:65533:1:storage_guest:/var/mnt:/bin/false
```
```
# cat /etc/build-info.rootfs
BUILD_INFO_PRODUCT_GENERATION="D"
BUILD_INFO_VOIP_PROTOCOL="SIP"
BUILD_INFO_CUSTOM="330"
BUILD_INFO_PRODUCT="vood/ng/02_07"
BUILD_INFO_USER="root"
BUILD_INFO_HOST="tilgin00144"
BUILD_INFO_REVISION="DSx330-02_07_01_25"
BUILD_INFO_SHORT_VERSION="02_07_01_25"
BUILD_INFO_DOT_VERSION="2.7.1.25"
BUILD_INFO_TIMESTAMP="2017/05/05-10:37:27"
BUILD_INFO_NAMES="HG125x HG126x HG22xx HG231x_HG235x HG237x"
```
```
# df
Filesystem           1K-blocks      Used Available Use% Mounted on
/dev/root                18688     18688         0 100% /
none                     62080       824     61256   1% /ramdisk
none                     62080         0     62080   0% /dev
none                       512       180       332  35% /ramdisk/var/log
tmpfs                     1244         0      1244   0% /ramdisk/var/spool/clp
ubi0:sam                 14692      1648     12272  12% /ramdisk/mnt/sam
# free
             total         used         free       shared      buffers
Mem:        124164        69956        54208            0         7892
-/+ buffers:              62064        62100
Swap:            0            0            0
```


```
VR9 # version

Tilgin UBI HG126x U-Boot 2010.06-LANTIQ-v-2.3.10 (May 20 2016 - 11:22:50) 02_07_01_20
```
```
VR9 # ubi info
UBI: MTD device name:            "ubi"
UBI: MTD device size:            127 MiB
UBI: physical eraseblock size:   131072 bytes (128 KiB)
UBI: logical eraseblock size:    129024 bytes
UBI: number of good PEBs:        1019
UBI: number of bad PEBs:         1
UBI: smallest flash I/O unit:    2048
UBI: VID header offset:          512 (aligned 512)
UBI: data offset:                2048
UBI: max. allowed volumes:       128
UBI: wear-leveling threshold:    256
UBI: number of internal volumes: 1
UBI: number of user volumes:     14
UBI: available PEBs:             535
UBI: total number of reserved PEBs: 484
UBI: number of PEBs reserved for bad PEB handling: 10
UBI: max/mean erase counter: 263/9
```

```
# ls /root/ -la
-rw-r--r--    1 root     root         12288 Feb 23  2015 BMCFw.BIN
-rw-r--r--    1 root     root         51620 Nov 25  2015 COSICFw.BIN
-rw-r--r--    1 root     root        458752 Jun 18  2014 firmware.bin

# ls /firmware/ -la
drwxr-xr-x    1 root     root            36 May  5  2017 HG1262a
-rwxr-xr-x    1 root     root        923140 Aug 15  2015 xcpe_a_hw.bin
-rw-r--r--    1 root     root            11 May  5  2017 xcpe_a_hw.bin_ver
-rwxr-xr-x    1 root     root        904388 Dec  5  2014 xcpe_b_hw.bin
-rw-r--r--    1 root     root            11 May  5  2017 xcpe_b_hw.bin_ver

# ls /firmware/HG1262a/ -la
-rw-r--r--    1 root     root        923200 May  5  2017 xcpe_hw.bin
-rw-r--r--    1 root     root            11 May  5  2017 xcpe_hw.bin_ver
```



Serial output 
```
ROM VER: 1.1.4
CFG 06
NAND
NAND Read OK

ROM VER: 1.1.4
CFG 06
NAND
NAND Read OK

DDR autotuning Rev 1.0
DDR size from 0xa0000000 - 0xa7ffffff
DDR check ok... start booting...



Tilgin UBI HG126x U-Boot 2010.06-LANTIQ-v-2.3.10 (May 20 2016 - 11:22:50) 02_07_01_20

CLOCK CPU 500M RAM 250M
DRAM:  128 MiB
NAND:  ONFI flash detected
ONFI param page 0 valid
NAND device: Manufacturer ID: 0xef, Chip ID: 0xf1 (WINBOND W29N01HV)
128 MiB
Creating 1 MTD partitions on "nand0":
0x000000000000-0x000000080000 : "U-Boot"
Creating 1 MTD partitions on "nand0":
0x000000080000-0x000008000000 : "ubi"
UBI: attaching mtd2 to ubi0
UBI: physical eraseblock size:   131072 bytes (128 KiB)
UBI: logical eraseblock size:    129024 bytes
UBI: smallest flash I/O unit:    2048
UBI: sub-page size:              512
UBI: VID header offset:          512 (aligned 512)
UBI: data offset:                2048
UBI: max. sequence number:       8929
UBI: attached mtd2 to ubi0
UBI: MTD device name:            "ubi"
UBI: MTD device size:            127 MiB
UBI: number of good PEBs:        1019
UBI: number of bad PEBs:         1
UBI: number of corrupted PEBs:   0
UBI: max. allowed volumes:       128
UBI: wear-leveling threshold:    256
UBI: number of internal volumes: 1
UBI: number of user volumes:     14
UBI: available PEBs:             535
UBI: total number of reserved PEBs: 484
UBI: number of PEBs reserved for bad PEB handling: 10
UBI: max/mean erase counter: 263/9
UBI: image sequence number:  931528877
Volume Environment (ID 4) found at slot 4
Read 7936 bytes from volume 4 to 86bf32a8(buf address)
In:    serial
Out:   serial
Err:   serial
Board reset caused by unknown (3c08a060).

Net:   internal phy using 36Mhz clock
Firmware is VR9 V1.2 GPHY FE
Internal phy(FE) firmware version: 0xc40d
vr9 Switch

Type "run flash_flash" to start the Linux kernel

Hit any key to stop autoboot:  0
```
```
No private boot packet is detected
Volume kernel (ID 6) found at slot 6
Read 0 bytes from volume 6 to 80500000(buf address)
Read [1548288] bytes
## Booting kernel from Legacy Image at 80500000 ...
   Image Name:   MIPS Linux-2.6.32
   Created:      2017-05-05   8:43:50 UTC
   Image Type:   MIPS Linux Kernel Image (lzma compressed)
   Data Size:    1472042 Bytes = 1.4 MiB
   Load Address: 80002000
   Entry Point:  800061b0
   Verifying Checksum ... OK
   Uncompressing Kernel Image ... OK

Starting kernel ...

Lantiq xDSL CPE VR9
mips_hpt_frequency = 250000000, counter_resolution = 2
Linux version 2.6.32.42 (lajo@tilgin00144) (gcc version 4.3.3 (GCC) ) #1 Fri May 5 10:43:41 CEST 2017


phym = 08000000, mem = 07f00000, max_pfn = 00007f00
Reserving memory for CP1 @0xa7f00000, size 0x00100000
CPU revision is: 00019556 (MIPS 34Kc)
Determined physical RAM map:
User-defined physical RAM map:
 memory: 0040f000 @ 00000000 (usable)
 memory: 005f0000 @ 00410000 (usable)
 memory: 074ff000 @ 00a01000 (usable)
Zone PFN ranges:
  Normal   0x00000000 -> 0x00007f00
Movable zone start PFN for each node
early_node_map[3] active PFN ranges
    0: 0x00000000 -> 0x0000040f
    0: 0x00000410 -> 0x00000a00
    0: 0x00000a01 -> 0x00007f00
Built 1 zonelists in Zone order, mobility grouping on.  Total pages: 32256
Kernel command line: mtdparts=ifx_nand:0x80000@0x0(U-Boot),-@0x80000(ubi) ubi.mtd=ubi root=mtd:rootfs ip=192.168.1.1:192.168.1.3::::eth0:on console=ttyS0,115200 ethaddr=14:AE:DB:B2:A0:F8 ID_ProductID=HG1262a ID_MAC_0=14:AE:DB:B2:A0:F8 ID_MAC_1=14:AE:DB:B2:A0:F9 ID_MAC_2=14:AE:DB:B2:A0:FA ID_MAC_3=14:AE:DB:B2:A0:FB ID_MAC_4=14:AE:DB:B2:A0:FC ID_MAC_5=14:AE:DB:B2:A0:FD ID_MAC_6=14:AE:DB:B2:A0:FE ID_MAC_7=14:AE:DB:B2:A0:FF panic=1 loglevel=7 UBOOT_VERSION="02_07_01_20" UBOOT_DATETIME="May 20 2016 - 11:23:03" RESET_CAUSE=unknown boot_cond= vpe1_load_addr=0x87f00000 vpe1_mem=1M mem=0x40f000 mem=0x5f0000@0x410000 mem=0x74ff000@0xa01000
PID hash table entries: 512 (order: -1, 2048 bytes)
Dentry cache hash table entries: 16384 (order: 4, 65536 bytes)
Inode-cache hash table entries: 8192 (order: 3, 32768 bytes)
Primary instruction cache 32kB, VIPT, 4-way, linesize 32 bytes.
Primary data cache 32kB, 4-way, VIPT, cache aliases, linesize 32 bytes
Writing ErrCtl register=00060610
Readback ErrCtl register=00060610
Memory: 123812k/130040k available (3178k kernel code, 6064k reserved, 1129k data, 188k init, 0k highmem)
Hierarchical RCU implementation.
NR_IRQS:185
Lantiq ICU driver, version 3.0.1, (c) 2001-2013 Lantiq Deutschland GmbH
console [ttyS0] enabled
Calibrating delay loop... 332.59 BogoMIPS (lpj=1662976)
Security Framework initialized
Mount-cache hash table entries: 512
NET: Registered protocol family 16
```
```
 Home gateway product HG1262a


Registered platform device tilgin-hg-ltq-nand:-1
Registered platform device vr9-ssi0:-1
Registered platform device tilgin-hg-ltq-gphy:-1
Registered platform device input-irq:-1
Lantiq Danube/Twinpass/Vinax GPIO
danube-gpio danube-gpio.0: gpio_base=0
danube-gpio danube-gpio.1: gpio_base=16
danube-gpio danube-gpio.2: gpio_base=32
Lantiq Danube/Twinpass/Vinax LED controller GPO
On/off switch class
GPIO-based on/off switch with auto-off
Lantiq PCI host controller driver, version 1.2.0, (c) 2001-2013 Lantiq Deutschland GmbH
Lantiq PCIe Root Complex driver, version 2.0.0, (c) 2001-2013 Lantiq Deutschland GmbH
bio: create slab <bio-0> at 0
SCSI subsystem initialized
usbcore: registered new interface driver usbfs
usbcore: registered new interface driver hub
usbcore: registered new device driver usb
pci 0000:00:00.0: PME# supported from D1 D2
pci 0000:00:00.0: PME# disabled
ifx_pcie_rc_class_early_fixup port 0: fixed pcie host bridge to pci-pci bridge
pci 0000:01:00.0: PME# supported from D0 D3hot
pci 0000:01:00.0: PME# disabled
pci 0000:02:00.0: PME# supported from D0 D1 D3hot
pci 0000:02:00.0: PME# disabled
pci 0000:01:00.0: PCI bridge, secondary bus 0000:02
pci 0000:01:00.0:   IO window: disabled
pci 0000:01:00.0:   MEM window: 0x1c000000-0x1c0fffff
pci 0000:01:00.0:   PREFETCH window: disabled
NET: Registered protocol family 8
NET: Registered protocol family 20
Switching to clocksource MIPS
NET: Registered protocol family 2
IP route cache hash table entries: 1024 (order: 0, 4096 bytes)
TCP established hash table entries: 4096 (order: 3, 32768 bytes)
TCP bind hash table entries: 4096 (order: 2, 16384 bytes)
TCP: Hash tables configured (established 4096 bind 4096)
TCP reno registered
NET: Registered protocol family 1
gptu: totally 6 16-bit timers/counters
gptu: misc_register on minor 63
gptu: succeeded to request irq 118
gptu: succeeded to request irq 119
gptu: succeeded to request irq 120
gptu: succeeded to request irq 121
gptu: succeeded to request irq 122
gptu: succeeded to request irq 123
IFX DMA driver, version ifxmips_dma_core.c:v1.1.5
,(c)2009 Infineon Technologies AG
Lantiq CGU driver, version 1.1.38, (c) 2001-2013 Lantiq Deutschland GmbH
vpe1_mem = 100000
Wired TLB entries for Linux read_c0_wired() = 0
squashfs: version 4.0 (2009/01/31) Phillip Lougher
Squashfs 2.2-r2 (released 2005/09/08) (C) 2002-2005 Phillip Lougher
msgmni has been set to 242
alg: No test for stdrng (krng)
Infineon Technologies DEU driver version 2.0.0
Lantiq Technologies DEU Driver version 2.0.0
alg: cipher: setkey failed on test 5 for ifxdeu-des: flags=100
alg: skcipher: setkey failed on test 5 for ifxdeu-ecb(des): flags=100
alg: cipher: setkey failed on test 1 for ifxdeu-des3_ede: flags=200000
IFX DEU DES initialized (multiblock).
Lantiq Technologies DEU Driver version 2.0.0
IFX DEU AES initialized (multiblock).
Infineon Technologies DEU driver version 2.0.0
IFX DEU ARC4 initialized (multiblock).
Infineon Technologies DEU driver version 2.0.0
IFX DEU SHA1 initialized.
Infineon Technologies DEU driver version 2.0.0
IFX DEU MD5 initialized.
Infineon Technologies DEU driver version 2.0.0
Key length exceeds maximum key length
alg: hash: setkey failed on test 5 for ifxdeu-sha1_hmac: ret=22
IFX DEU SHA1_HMAC initialized.
Infineon Technologies DEU driver version 2.0.0
alg: hash: setkey failed on test 5 for ifxdeu-md5_hmac: ret=22
IFX DEU MD5_HMAC initialized.
DEU driver initialization complete!
io scheduler noop registered (default)
I/O Memory GPIO Emulation
ifx_pmu_init: Major 253
Lantiq PMU driver, version 1.2.6, (c) 2001-2013 Lantiq Deutschland GmbH
Lantiq GPIO driver, version 1.3.2, (c) 2001-2013 Lantiq Deutschland GmbH
Infineon Technologies RCU driver version 1.1.1
Lantiq Thermal Sensor driver, version 1.0.3, (c) 2001-2013 Lantiq Deutschland GmbH
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: Lantiq GPHY kthread created
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: gpio_base=96
Tilgin initialization is OK
ttyS0 at MMIO 0xbe100c00 (irq = 105) is a IFX_ASC
Lantiq ASC (UART) driver, version 1.0.14, (c) 2001-2013 Lantiq Deutschland GmbH
loop: module loaded
ifx_mtd_init: No support flash chips found!
slram: not enough parameters.
Tilgin HG Lantiq NAND driver
ifx_nand_init
Probe for NAND flash...
Checking if ONFI complient
ONFI param page 0 valid
ONFI flash detected, val i = 0
writesize: 2048, erasesize: 131072, chipsize: 134217728
NAND device: Manufacturer ID: 0xef, Chip ID: 0xf1 (Unknown NAND 128MiB 3,3V 8-bit)
Scanning device for bad blocks
Bad eraseblock 143 at 0x0000011e0000
2 cmdlinepart partitions found on MTD device ifx_nand
Creating 2 MTD partitions on "ifx_nand":
0x000000000000-0x000000080000 : "U-Boot"
0x000000080000-0x000008000000 : "ubi"
UBI: attaching mtd1 to ubi0
UBI: physical eraseblock size:   131072 bytes (128 KiB)
UBI: logical eraseblock size:    129024 bytes
UBI: smallest flash I/O unit:    2048
UBI: sub-page size:              512
UBI: VID header offset:          512 (aligned 512)
UBI: data offset:                2048
UBI: max. sequence number:       8929
UBI: attached mtd1 to ubi0
UBI: MTD device name:            "ubi"
UBI: MTD device size:            127 MiB
UBI: number of good PEBs:        1019
UBI: number of bad PEBs:         1
UBI: number of corrupted PEBs:   0
UBI: max. allowed volumes:       128
UBI: wear-leveling threshold:    256
UBI: number of internal volumes: 1
UBI: number of user volumes:     14
UBI: available PEBs:             535
UBI: total number of reserved PEBs: 484
UBI: number of PEBs reserved for bad PEB handling: 10
UBI: max/mean erase counter: 263/9
UBI: image sequence number:  931528877
UBI: background thread "ubi_bgt0d" started, PID 232
Lantiq SSC driver, version 2.4.2, (c) 2001-2013 Lantiq Deutschland GmbH
PPP generic driver version 2.4.2
NET: Registered protocol family 24
PPPoL2TP kernel driver, V1.0
IFX SWITCH API, Version 1.2.6
SWAPI: Registered character device [switch_api] with major no [81]
Switch API: PCE MicroCode loaded !!

 GPHY:!!!!  chip-ID :4, chipID.family_ver:2
Init GPHY Driver for A12 !!
Lantiq GPHY #0 in FE mode
Lantiq GPHY #1 in FE mode
IFX GPHY driver version ifxmips_xrx_gphy: V1.1.1 - Firmware: GPHY0 FE c434, GPHY1 FE c434
res = 878b7980
Initializing USB Mass Storage driver...
usbcore: registered new interface driver usb-storage
USB Mass Storage support registered.
input: input-gpio-polled as /devices/platform/input-gpio-polled.0/input/input0
input: input-irq as /devices/platform/input-irq/input/input1
Lantiq Danube/Twinpass/Vinax Watchdog
danube-wdt danube-wdt: Starting Watchdog Timer
Start watchdog with maximum timeout 64 seconds
Registered led device: 1:green
Registered led device: 2:green
Registered led device: 3:green
Registered led device: 4:green
Registered led device: 5:green
Registered led device: 6:green
Registered led device: 7:green
Registered led device: 8:green
Netfilter messages via NETLINK v0.30.
nf_conntrack version 0.5.0 (1937 buckets, 7748 max)
ctnetlink v0.93: registering with nfnetlink.
nf_ct_ipsec_ike: registering helper for pf: 2 port: 500
xt_time: kernel timezone is -0000
ip_tables: (C) 2000-2006 Netfilter Core Team
TCP cubic registered
Initializing XFRM netlink socket
NET: Registered protocol family 10
ip6_tables: (C) 2000-2006 Netfilter Core Team
IPv6 over IPv4 tunneling driver
NET: Registered protocol family 17
NET: Registered protocol family 15
Bridge firewalling registered
Ebtables v2.0 registered
KOAM is loaded successfully.
802.1Q VLAN Support v1.8 Ben Greear <greearb@candelatech.com>
All bugs added by David S. Miller <davem@redhat.com>
Use /dev/mtdblock9 instead of mtd:rootfs
VFS: Mounted root (squashfs_old filesystem) readonly on device 31:9.
Freeing unused kernel memory: 188k freed
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: switch port #2 PHY ID is 0x11
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: switch port #3 PHY ID is 0x12
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: switch port #4 PHY ID is 0x13
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: switch port #5 PHY ID is 0x14
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: PHY MDIO register value write failed: phy_id=0x11 addr=0x14 write=0xb806 read=0x8006
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: PHY MDIO register value write failed: phy_id=0x12 addr=0x14 write=0xb806 read=0x8006
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: PHY MDIO register value write failed: phy_id=0x13 addr=0x14 write=0xb806 read=0x8006
tilgin-hg-ltq-gphy tilgin-hg-ltq-gphy: PHY MDIO register value write failed: phy_id=0x14 addr=0x14 write=0xb806 read=0x8006
init started: BusyBox v1.21.1 (2017-05-05 10:49:49 CEST)
starting pid 299, tty '': '/etc/init.d/rcS'
real    0m 0.03s
user    0m 0.00s
sys     0m 0.04s
crm-cleanup: running...
iptables v1.4.6: can't initialize iptables table `mangle': Table does not exist (do you need to insmod?)
Perhaps iptables or your kernel needs to be upgraded.
iptables v1.4.6: can't initialize iptables table `mangle': Table does not exist (do you need to insmod?)
Perhaps iptables or your kernel needs to be upgraded.
grep: /proc/649/cmdline: No such file or directory
grep: /proc/664/cmdline: No such file or directory
All modules unloaded
crm-cleanup: done
pmem-name2path: Failed to map MTD device 'Environment2'
pmem-read.squashfs: Restoring /var/log from Log (/dev/mtd/13)
mount: mounting /dev/mtdblock/13 on /tmp/pmem.okdinb failed: Invalid argument
mount: mounting /dev/mtdblock/14 on /tmp/pmem.dGm2tT failed: Invalid argument
cat: can't open '/tmp/pmem.dGm2tT/VERSION': No such file or directory
pmem-read.squashfs: Failed to read Config-A version file
pmem-name2path: Failed to map MTD device 'Config-B'
pmem-read.squashfs: Restoring /var/etc from Config-A (/dev/mtd/14)
mount: mounting /dev/mtdblock/14 on /tmp/pmem.dGm2tT failed: Invalid argument
pmem-read.squashfs: Restoring /tmp/pmem.8pito7 from Config-C (/dev/mtd/12)
mount: mounting /dev/mtdblock/12 on /tmp/pmem.dGm2tT failed: Invalid argument
pmem-name2path: Failed to map MTD device 'Config-B'
pmem-name2path: Failed to map MTD device 'Environment2'
pmem-name2path: Failed to map MTD device 'rootfs-ram'
pmem-name2path: Failed to map MTD device 'appfs-ram'
pmem-read.squashfs: Restoring /var/miscA from Misc-A (/dev/mtd/15)
mount: mounting /dev/mtdblock/15 on /tmp/pmem.gKk32g failed: Invalid argument
pmem-name2path: Failed to map MTD device 'Misc-B'
Jan  1 00:00:13 C Dispatcher: Init module logger        OK

RootFS version DSx330-02_07_01_25


BusyBox v1.21.1 (2017-05-05 10:49:49 CEST) built-in shell (ash)
Enter 'help' for a list of built-in commands.

# IFXOS, Version 1.5.16 (c) Copyright 2009, Lantiq Deutschland GmbH
Lantiq (VRX) DSL CPE MEI driver, version 1.4.4.1, (c) 2013 Lantiq Deutschland GmbH

Lantiq CPE API Driver version: DSL CPE API V4.16.6.3

Predefined debug level: 3
Trying to start watchdog with timeout 10 seconds
umount: can't umount /usr/share/webui: Invalid argument
IFXUSB: ifxusb_hcd: version 3.2 B140220-tilgin271015
IFXUSB:    OPTION: __IS_VR9__
IFXUSB:    OPTION: __UEIP__
IFXUSB:    OPTION: __PHY_LONG_PREEMP__
IFXUSB:    OPTION: __UNALIGNED_BUF_ADJ__
IFXUSB:    OPTION: __ENABLE_DUMP__
IFXUSB:    OPTION: __NEW_COC__
IFXUSB:    OPTION: __IS_HOST__
IFXUSB:            __IS_DUAL__
IFXUSB:            __DYN_SOF_INTR__
IFXUSB:            __UEIP__
IFXUSB:            __DO_OC_INT__
IFXUSB:            __INTRNAKRETRY__
IFXUSB:            __INTRINCRETRY__
Chip Version :0002 BurstSize=4
IFXUSB: USB core #0 soft-reset
IFXUSB: USB core #0 soft-reset
ifxusb_hcd ifxusb_hcd: IFX USB Controller
ifxusb_hcd ifxusb_hcd: new USB bus registered, assigned bus number 1
ifxusb_hcd ifxusb_hcd: irq 54, io mem 0xbe101000
IFXUSB: Init: Power Port (0)
on/off switch 'usb_power' not found
usb usb1: configuration #1 chosen from 1 choice
hub 1-0:1.0: USB hub found
hub 1-0:1.0: 1 port detected
IFXUSB: USB core #1 soft-reset
IFXUSB: USB core #1 soft-reset
ifxusb_hcd ifxusb_hcd: IFX USB Controller
ifxusb_hcd ifxusb_hcd: new USB bus registered, assigned bus number 2
ifxusb_hcd ifxusb_hcd: irq 83, io mem 0xbe106000
IFXUSB: Init: Power Port (0)
on/off switch 'usb_power' not found
usb usb2: configuration #1 chosen from 1 choice
hub 2-0:1.0: USB hub found
hub 2-0:1.0: 1 port detected
cryptodev: module license 'BSD' taints kernel.
Disabling lock debugging due to kernel taint
usbcore: registered new interface driver usblp
usbcore: registered new interface driver cdc_ether
usbcore: registered new interface driver rndis_host
usbcore: registered new interface driver cdc_ncm
Loading E5 (MII0/1) driver ...... Succeeded!
PPE datapath driver info:
  Version ID: 64.3.3.1.0.1.1
  Family    : VR9
  DR Type   : Normal Data Path | Indirect-Fast Path
  Interface : MII0 | MII1
  Mode      : Routing
  Release   : 0.1.1
PPE 0 firmware info:
  Version ID: 7.3.2.14.1
  Family    : VR9
  FW Package: E1
  Release   : 2.14.1
PPE 1 firmware info:
  Version ID: 7.5.2.14.1
  Family    : VR9
  FW Package: D5
  Release   : 2.14.1
PPE firmware feature:
  ATM/PTM TC-Layer Bonding        Support
  L2 Trunking                     Support
  Packet Acceleration             Support
  IPv4                            Support
  IPv6                            Support
  6RD                             Support
  DS-Lite                        PPA API --- init successfully
ifx_ppa_init - init succeeded
2+0 records in
2+0 records out
ath_hal: 0.9.17.1 (AR5416, AR9380, REGOPS_FUNC, WRITE_EEPROM, TX_DATA_SWAP, RX_DATA_SWAP, 11D)
ath_rate_atheros: Copyright (c) 2001-2005 Atheros Communications, Inc, All Rights Reserved
ath_dfs: Version 2.0.0
Copyright (c) 2005-2006 Atheros Communications, Inc. All Rights Reserved
ath_dev: Copyright (c) 2001-2007 Atheros Communications, Inc, All Rights Reserved
ath_pci: 10.2.85 (Atheros/multi-bss)
__ath_attach: Set global_scn[0]
*** All the minfree values should be <= ATH_TXBUF-32, otherwise default value will be used instead ***
ACBKMinfree = 48
ACBEMinfree = 32
ACVIMinfree = 16
ACVOMinfree = 0
CABMinfree = 48
UAPSDMinfree = 0
ATH_TXBUF=540
Reading Flash for Calibraton data from 0x1000 and partition name is caldata
ath_get_caps[6113] rx chainmask mismatch actual 3 sc_chainmak 0
ath_get_caps[6088] tx chainmask mismatch actual 3 sc_chainmak 0
ath_attach_dfs[12507] dfsdomain 1
wifi0: Atheros 5416: mem=0x1c000000, irq=136 hw_base=0xbc000000
Getting Nss: 1
watchdog: disabled
Trying to start watchdog with timeout 10 seconds
ifx_ppa_init - init succeeded
ath_attach_dfs[12507] dfsdomain 1
PPA REG DONE, if_id=3, dev_if_index = 8, os_unit=0
Setting Max Stations:16
device eth0 entered promiscuous mode
device wlan2 entered promiscuous mode
PPA REG DONE, if_id=4, dev_if_index = 10, os_unit=1
Setting Max Stations:5
device eth0.4031 entered promiscuous mode
device eth0 entered promiscuous mode
device wlan3 entered promiscuous mode
watchdog: disabled
Configuration file: /tmp/h ieee80211_ioctl_siwmode: imr.ifm_active=131712, new mode=3, valid=1
ostapd-wlan2.conf
Trying to start watchdog with timeout 64 seconds
 DEVICE IS DOWN ifname=wlan2
 DEVICE IS DOWN ifname=wlan2
Usin
 DES SSID SET=Pezeq_WiFi
g interface wlan2 with hwaddr 14:ae:db:b2:a0:fd and ssid "Pezeq_WiFi"
Configuration file: ieee80211_ioctl_siwmode: imr.ifm_active=393856, new mode=3, valid=1
 /tmp/hostapd-wlan2.conf
Using interface wlan2 with hwaddr 14:ae:db:b2:a0:fd and ssid "Pezeq_WiFi"
CRM state '/' flags=0 saving...
CRM state '/' flags=0 saving... done. Status=EOK Count=1364
find: /sys/class/tty/wwan?/uevent: No such file or directory
find: /sys/class/scsi_disk/*/uevent: No such file or directory
find: /sys/class/usb/lp*/device/uevent: No such file or directory
Volume ID:   2 (on ubi0)
Type:        dynamic
Alignment:   1
Size:        139 LEBs (17934336 bytes, 17.1 MiB)
State:       OK
Name:        sam
Character device major/minor: 249:3
UBIFS: recovery needed
UBIFS: recovery completed
UBIFS: mounted UBI device 0, volume 2, name "sam"
UBIFS: file system size:   16773120 bytes (16380 KiB, 15 MiB, 130 LEBs)
UBIFS: journal size:       1032193 bytes (1008 KiB, 0 MiB, 6 LEBs)
UBIFS: media format:       w4/r0 (latest is w4/r0)
UBIFS: default compressor: lzo
UBIFS: reserved for root:  792235 bytes (773 KiB)
1970-01-01 02:00:58: (/space/sources/02_07/Srael/02_07_01_25/factory/src/vood/ng/02_07/lighttpd/src/log.c.164) server started
udhcpd (v1.21.1) started
```
