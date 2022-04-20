# Basic Usage / Options

```markup
optional arguments:
  -h, --help           show this help message and exit
  --unix UNIX          convert from Unix Seconds
  --umil UMIL          convert from Unix Milliseconds
  --wh WH              convert from Windows 64-bit Hex BE
  --whle WHLE          convert from Windows 64-bit Hex LE
  --chrome CHROME      convert from Google Chrome time
  --active ACTIVE      convert from Active Directory value
  --uhbe UHBE          convert from Unix Hex 32-bit BE
  --uhle UHLE          convert from Unix Hex 32-bit LE
  --cookie COOKIE      convert from Windows Cookie Date (Low Value,High Value)
  --oleb OLEB          convert from Windows OLE 64-bit BE - remove 0x and spaces!
                       - Example from SRUM: 0x40e33f5d 0x97dfe8fb should be 40e33f5d97dfe8fb
  --olel OLEL          convert from Windows OLE 64-bit LE
  --mac MAC            convert from Mac Absolute Time
  --hfsdec HFSDEC      convert from Mac OS/HFS+ Decimal Time
  --hfsbe HFSBE        convert from HFS(+) BE times (HFS = Local, HFS+ = UTC)
  --hfsle HFSLE        convert from HFS(+) LE times (HFS = Local, HFS+ = UTC)
  --fat FAT            convert from FAT Date + Time (wFat)
  --msdos MSDOS        convert from 32-bit MS-DOS time - result is Local Time
  --systime SYSTIME    convert from 128-bit SYSTEMTIME
  --ft FT              convert from FILETIME timestamp
  --hotmail HOTMAIL    convert from a Hotmail timestamp
  --pr PR              convert from Mozilla's PRTime
  --auto AUTO          convert from OLE Automation Date format
  --ms1904 MS1904      convert from MS Excel 1904 Date format
  --ios IOS            convert from iOS 11 timestamp
  --sym SYM            convert from Symantec's 12-byte AV timestamp
  --gps GPS            convert from a GPS timestamp
  --eitime EITIME      convert from a Google EI URL timestamp
  --bplist BPLIST      convert from an iOS Binary Plist timestamp
  --gsm GSM            convert from a GSM timestamp
  --vm VM              convert from a VMWare Snapshot (.vmsd) timestamp - enter as "high value,low value"
  --tiktok TIKTOK      convert from a TikTok URL value
  --twitter TWITTER    convert from a Twitter URL value
  --discord DISCORD    convert from a Discord URL value
  --ksuid KSUID        convert from a KSUID value
  --mastodon MASTODON  convert from a Mastodon URL value
  --meta META          convert from a Metasploit Payload UUID
  --sony SONY          convert from a Sonyflake URL value
  --uu UU              convert from a UUID: 00000000-0000-0000-0000-000000000000
  --guess TS_VALUE     guess timestamp and output all reasonable possibilities
  --timestamp [DATE]   convert date to every timestamp - enter date as "YYYY-MM-DD HH:MM:SS.f" in 24h fmt.
                       - Without argument gives current date/time
  --version, -v        show program's version number and exit
```

