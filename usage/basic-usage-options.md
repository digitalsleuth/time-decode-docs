# Basic Usage / Options

The basic usage for time-decode is to either "guess" what a timestamp is, or to generate a timestamp based on a specific date:

```markup
time-decode --guess 01d8eed637a776ec
Outputs which do not result in a date/time value are not displayed.
Most likely results (within +/- 5 years) are highlighted.

GMail Message ID time:          1974-01-09 08:26:13.754000 UTC
Google EI time:                 2034-08-03 04:28:03.000000 UTC
Windows 64-bit Hex BE:          2022-11-02 16:14:43.156350 UTC
Windows OLE 64-bit double BE:   1899-12-30 00:00:00.000000 UTC

```

```
time-decode --timestamp "2022-11-02 16:14:43.156350 -4"

Converting Date: 2022-11-02 16:14:43.156350 -4

Active Directory/LDAP dt:       133118936831563500
BitDate time:                   0e146b7e
Bitwise Decimal time:           2120946958
DHCP6 DUID time:                000100012af58c33000000000000
exFAT time:                     556281d5
FAT Date + Time:                6255d581
GMail Boundary time:            000000000000bf757e05ec827d00
GMail Message ID time:          18439fb53d400000
Google Chrome:                  13311893683156350
Google EI time:                 M19iYw
GPS time:                       1351455301
GSM time:                       22112061413469
HFS/HFS+ 32-bit Hex BE:         df888033
HFS/HFS+ 32-bit Hex LE:         338088df
KSUID Decimal:                  267420083
Mac OS/HFS+ Decimal Time:       3750264883
Mastodon time:                  109276042559488000
Microsoft 128-bit SYSTEMTIME:   e6070b000300020014000e002b009c00
Microsoft FILETIME time:        beb916ec:01d8eef7
Microsoft Hotmail time:         f7eed801:ec16b9be
Microsoft .NET DateTime:        638030168831563520
Motorola time:                  340b02100e2b
Mozilla PRTime:                 1667420083156350
MS-DOS 32-bit Hex Value:        d5816255
MS Excel 1904 Date:             43405.843555050349
Nokia S40 time:                 07e60b02140e2b
Nokia S40 time LE:              e6070b02140e2b
Nokia time:                     cce859b3
Nokia time LE:                  b359e8cc
NSDate - Binary Plist / Cocoa:  689112883
NSDate - iOS 11+:               689112883156350080
NSDate - Mac Absolute time:     689112883.156350
OLE Automation Date:            44867.843555050349
Symantec AV time:               340a02100e2b
Unix Hex 32-bit BE:             6362cfb3
Unix Hex 32-bit LE:             b3cf6263
Unix Seconds:                   1667420083
Unix Milliseconds:              1667420083156
VMSD time:                      388226,2109543104
Windows 64-bit Hex BE:          01d8eef7beb916ec
Windows 64-bit Hex LE:          ec16b9bef7eed801
Windows Cookie Date:            3198237568,30994167
Windows OLE 64-bit double BE:   40e5e87afe672934
Windows OLE 64-bit double LE:   342967fe7ae8e540
```

You can also choose the specific timestamp you want by selecting it from the following:

```markup
optional arguments:
  -h, --help          show this help message and exit
  --guess             guess format and output possibilities
  --timestamp [DATE]  convert date to every timestamp
                      enter date as "YYYY-MM-DD HH:MM:SS.f" in 24h fmt.
                      Without argument gives current date/time
  --active            convert from Active Directory value
  --auto              convert from OLE Automation Date format
  --bitdate           convert from a Samsung/LG 4-byte value
  --bitdec            convert from a bitwise decimal 10-digit value
  --bplist            convert from an iOS Binary Plist value
  --chrome            convert from Google Chrome value
  --cookie            convert from Windows Cookie Date (Low,High)
  --dhcp6             convert from a DHCP6 DUID value
  --discord           convert from a Discord URL value
  --dotnet            convert from a .NET DateTime value
  --eitime            convert from a Google EI URL value
  --exfat             convert from an exFAT 4-byte value
  --fat               convert from FAT Date + Time (wFat)
  --ft                convert from FILETIME value
  --gbound            convert from a GMail Boundary value
  --gmsgid            convert from a GMail Message ID value
  --gps               convert from a GPS value
  --gsm               convert from a GSM value
  --hfsbe             convert from HFS(+) BE, HFS Local, HFS+ UTC
  --hfsle             convert from HFS(+) LE, HFS Local, HFS+ UTC
  --hfsdec            convert from Mac OS/HFS+ Decimal Time
  --hotmail           convert from a Hotmail value
  --ios               convert from iOS 11 value
  --kstime            convert from a KSUID 9-digit value
  --ksuid             convert from a KSUID 27-character value
  --mac               convert from Mac Absolute Time
  --mastodon          convert from a Mastodon URL value
  --meta              convert from a Metasploit Payload UUID
  --moto              convert from Motorola's 6-byte value
  --ms1904            convert from MS Excel 1904 Date format
  --msdos             convert from 32-bit MS-DOS time, result is Local
  --nokia             convert from a Nokia 4-byte value
  --nokiale           convert from a Nokia 4-byte LE value
  --ns40              convert from a Nokia S40 7-byte value
  --ns40le            convert from a Nokia S40 7-byte LE value
  --nsdate            convert from an Apple NSDate (iOS, BPList, Cocoa, Mac Absolute)
  --oleb              convert from Windows OLE 64-bit BE, remove 0x & space
                      - example from SRUM: 0x40e33f5d 0x97dfe8fb should be 40e33f5d97dfe8fb
  --olel              convert from Windows OLE 64-bit LE
  --pr                convert from Mozilla's PRTime
  --sony              convert from a Sonyflake URL value
  --sym               convert from Symantec's 6-byte AV value
  --systime           convert from 128-bit SYSTEMTIME value
  --tiktok            convert from a TikTok URL value
  --twitter           convert from a Twitter URL value
  --uhbe              convert from Unix Hex 32-bit BE
  --uhle              convert from Unix Hex 32-bit LE
  --unix              convert from Unix Seconds
  --umil              convert from Unix Milliseconds
  --uu                convert from a UUID: 00000000-0000-0000-0000-000000000000
  --vm                convert from a VMWare Snapshot (.vmsd) value
                      - enter as "high value,low value"
  --wh                convert from Windows 64-bit Hex BE
  --whle              convert from Windows 64-bit Hex LE
  --version, -v       show program's version number and exit
```

For example:

```markup
time-decode --ms1904 43405.843555050349
MS Excel 1904 Date: 2022-11-02 20:14:43.156350 UTC
```

