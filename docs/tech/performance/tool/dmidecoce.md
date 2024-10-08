dmidecode 可以获取服务器的硬件信息，包括：CPU、methed、disk、BIOS等

```shell
$ sudo dmidecode
# dmidecode 3.3
Getting SMBIOS data from sysfs.
SMBIOS 2.8 present.
9 structures occupying 451 bytes.
Table at 0x7BBCB000.

Handle 0x0100, DMI type 1, 27 bytes
System Information
        Manufacturer: Alibaba Cloud
        Product Name: Alibaba Cloud ECS
        Version: pc-i440fx-2.1
        Serial Number: 489790e7-ab40-4783-86ad-4b29245db3f2
        UUID: 489790e7-ab40-4783-86ad-4b29245db3f2
        Wake-up Type: Power Switch
        SKU Number: Not Specified
        Family: Not Specified

Handle 0x0300, DMI type 3, 21 bytes
Chassis Information
        Manufacturer: Alibaba Cloud
        Type: Other
        Lock: Not Present
        Version: pc-i440fx-2.1
        Serial Number: Not Specified
        Asset Tag: Not Specified
        Boot-up State: Safe
        Power Supply State: Safe
        Thermal State: Safe
        Security Status: Unknown
        OEM Information: 0x00000000
        Height: Unspecified
        Number Of Power Cords: Unspecified
        Contained Elements: 0

Handle 0x0400, DMI type 4, 42 bytes
Processor Information
        Socket Designation: CPU 0
        Type: Central Processor
        Family: Other
        Manufacturer: Alibaba Cloud
        ID: 54 06 05 00 FF FB 8B 1F
        Version: pc-i440fx-2.1
        Voltage: Unknown
        External Clock: Unknown
        Max Speed: Unknown
        Current Speed: Unknown
        Status: Populated, Enabled
        Upgrade: Other
        L1 Cache Handle: Not Provided
        L2 Cache Handle: Not Provided
        L3 Cache Handle: Not Provided
        Serial Number: Not Specified
        Asset Tag: Not Specified
        Part Number: Not Specified
        Core Count: 1
        Core Enabled: 1
        Thread Count: 2
        Characteristics: None

Handle 0x1000, DMI type 16, 23 bytes
Physical Memory Array
        Location: Other
        Use: System Memory
        Error Correction Type: Multi-bit ECC
        Maximum Capacity: 2 GB
        Error Information Handle: Not Provided
        Number Of Devices: 1

Handle 0x1100, DMI type 17, 40 bytes
Memory Device
        Array Handle: 0x1000
        Error Information Handle: Not Provided
        Total Width: Unknown
        Data Width: Unknown
        Size: 2 GB
        Form Factor: DIMM
        Set: None
        Locator: DIMM 0
        Bank Locator: Not Specified
        Type: RAM
        Type Detail: Other
        Speed: Unknown
        Manufacturer: Alibaba Cloud
        Serial Number: Not Specified
        Asset Tag: Not Specified
        Part Number: Not Specified
        Rank: Unknown
        Configured Memory Speed: Unknown
        Minimum Voltage: Unknown
        Maximum Voltage: Unknown
        Configured Voltage: Unknown

Handle 0x1300, DMI type 19, 31 bytes
Memory Array Mapped Address
        Starting Address: 0x00000000000
        Ending Address: 0x0007FFFFFFF
        Range Size: 2 GB
        Physical Array Handle: 0x1000
        Partition Width: 1

Handle 0x2000, DMI type 32, 11 bytes
System Boot Information
        Status: No errors detected

Handle 0x0000, DMI type 0, 26 bytes
BIOS Information
        Vendor: EFI Development Kit II / OVMF
        Version: 0.0.0
        Release Date: 02/06/2015
        Address: 0xE8000
        Runtime Size: 96 kB
        ROM Size: 64 kB
        Characteristics:
                BIOS characteristics not supported
                Targeted content distribution is supported
                UEFI is supported
                System is a virtual machine
        BIOS Revision: 0.0

Handle 0xFEFF, DMI type 127, 4 bytes
End Of Table
```