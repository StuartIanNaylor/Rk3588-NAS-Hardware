# Rk3588-NAS-Hardware
Rk3588-NAS Hardware
![Rk3588-NAS Hardware](https://github.com/StuartIanNaylor/Rk3588-NAS-Hardware/blob/main/img/rk3588nas1.jpg)

6x Western Digital WD GreenPower 1tb SATA 3.5". Likely the slowest you can get and all benches will be bottlenecked by the drives

https://www.ebay.co.uk/itm/175548988967 M.2 To SATA3.0 6Gbps ASM1166 PCIE £19.43

https://www.ebay.co.uk/itm/155827163009 DC-DC 24V 12V to 5V 5A Buck £4.49

https://www.aliexpress.com/item/1005003413283663.html 8 bay 3.5" Hard Drive Hard Disk Box Transparent with Fans Space ￡8.38

https://www.aliexpress.com/item/1005001338308949.html SATA Cable 3.0 to Hard Disk Drive SSD HDD Sata 3 90 Degree Left-angle x6 ￡11.79

https://www.ebay.co.uk/itm/195722529195 Automatic Temperature Control CPU Fan Speed DC Controller 12V PWM £6.95

https://www.ebay.co.uk/itm/352213388309 Sata Power Splitter Cable 3 Way Male to Female Hard Drive Adapter x2 £6.98

https://www.ebay.co.uk/itm/355017364263 Molex to SATA Cable Power x2 £3.58

https://www.ebay.co.uk/itm/185634263363 ARCTIC F8 P8 TC Silent PWM PST CO 80mm x2 £12.94

https://www.ebay.co.uk/itm/126071921551 DC12V Power Supply With Kettle Lead Adapter Connector 6A £10.99

```
ubuntu@ubuntu:~$ sudo mdadm --detail /dev/md0
/dev/md0:
           Version : 1.2
     Creation Time : Sat Nov 11 16:37:56 2023
        Raid Level : raid5
        Array Size : 4883146240 (4.55 TiB 5.00 TB)
     Used Dev Size : 976629248 (931.39 GiB 1000.07 GB)
      Raid Devices : 6
     Total Devices : 6
       Persistence : Superblock is persistent

     Intent Bitmap : Internal

       Update Time : Sat Nov 11 20:27:12 2023
             State : clean
    Active Devices : 6
   Working Devices : 6
    Failed Devices : 0
     Spare Devices : 0

            Layout : left-symmetric
        Chunk Size : 512K

Consistency Policy : bitmap

              Name : ubuntu:0  (local to host ubuntu)
              UUID : 3e111291:a3d59b11:2badfe6c:733fd483
            Events : 2431

    Number   Major   Minor   RaidDevice State
       0       8        1        0      active sync   /dev/sda1
       1       8       17        1      active sync   /dev/sdb1
       2       8       33        2      active sync   /dev/sdc1
       3       8       49        3      active sync   /dev/sdd1
       4       8       65        4      active sync   /dev/sde1
       6       8       81        5      active sync   /dev/sdf1
```
```
        Record Size 1 kB
        File size set to 1048576 kB
        Command line used: iozone -t1 -i0 -i2 -r1k -s1g ./
        Output is in kBytes/sec
        Time Resolution = 0.000001 seconds.
        Processor cache size set to 1024 kBytes.
        Processor cache line size set to 32 bytes.
        File stride size set to 17 * record size.
        Throughput test with 1 process
        Each process writes a 1048576 kByte file in 1 kByte records

        Children see throughput for  1 initial writers  =  758864.31 kB/sec
        Parent sees throughput for  1 initial writers   =  174167.80 kB/sec
        Min throughput per process                      =  758864.31 kB/sec
        Max throughput per process                      =  758864.31 kB/sec
        Avg throughput per process                      =  758864.31 kB/sec
        Min xfer                                        = 1048576.00 kB

        Children see throughput for  1 rewriters        = 1221363.88 kB/sec
        Parent sees throughput for  1 rewriters         =  203864.18 kB/sec
        Min throughput per process                      = 1221363.88 kB/sec
        Max throughput per process                      = 1221363.88 kB/sec
        Avg throughput per process                      = 1221363.88 kB/sec
        Min xfer                                        = 1048576.00 kB

        Children see throughput for 1 random readers    =  760140.56 kB/sec
        Parent sees throughput for 1 random readers     =  693441.61 kB/sec
        Min throughput per process                      =  760140.56 kB/sec
        Max throughput per process                      =  760140.56 kB/sec
        Avg throughput per process                      =  760140.56 kB/sec
        Min xfer                                        = 1048576.00 kB

        Children see throughput for 1 random writers    =  597619.56 kB/sec
        Parent sees throughput for 1 random writers     =   96005.26 kB/sec
        Min throughput per process                      =  597619.56 kB/sec
        Max throughput per process                      =  597619.56 kB/sec
        Avg throughput per process                      =  597619.56 kB/sec
        Min xfer                                        = 1048576.00 kB
```
```

ubuntu@ubuntu:/mnt/raid5$ iozone -s 102400


        File size set to 102400 kB
        Command line used: iozone -s 102400
        Output is in kBytes/sec
        Time Resolution = 0.000001 seconds.
        Processor cache size set to 1024 kBytes.
        Processor cache line size set to 32 bytes.
        File stride size set to 17 * record size.
                                                              random    random     bkwd    record    stride
              kB  reclen    write  rewrite    read    reread    read     write     read   rewrite      read   fwrite frewrite    fread  freread
          102400       4  1172444  2516654  5832082  3731904  2796898  2008939  3261253   4400499   2837269  2354880  2340035  5575866  5607899
```
```

ubuntu@ubuntu:/mnt/raid5$ dd if=/dev/zero of=./test bs=8k count=500k conv=fsync; rm -f ./test
512000+0 records in
512000+0 records out
4194304000 bytes (4.2 GB, 3.9 GiB) copied, 17.223 s, 244 MB/s
```
```
ubuntu@ubuntu:/mnt/raid5$ sudo hdparm -t /dev/md0

/dev/md0:
 Timing buffered disk reads: 878 MB in  3.01 seconds = 291.89 MB/sec
```
The above is just a test on Mainline Ubuntu to install OMV use a Debian Cli image.
https://wiki.omv-extras.org/doku.php?id=omv6:armbian_bullseye_install
Any Debian Bullseye Cli image as used the Radxa images.
https://github.com/radxa-build/rock-5b/releases


