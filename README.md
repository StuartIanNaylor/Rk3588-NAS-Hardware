# Rk3588-NAS-Hardware
Rk3588-NAS Hardware

6x Western Digital WD GreenPower 1tb SATA 3.5"

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






