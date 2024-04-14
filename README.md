# Windows 11 Unattended Installation Configuration

This repository contains an unattend.xml file for configuring an unattended installation of Windows 11 Pro.

## Author
- Praveen Kumar Soni

## Installation Notes
- Location: US
- Installing Windows 11 Pro Without User Intervention

## Installation Configuration Details

- Language and Locale:
  - Setup UI Language: English (United States)
  - Input Locale: English (United States)
  - System Locale: English (United States)
  - UI Language: English (United States)
  - UI Language Fallback: English (United States)
  - User Locale: English (United States)
  - Time Zone: Eastern Standard Time

- Disk Configuration:
  - Disk ID: 0
  - Will Wipe Disk: true
  - Partitions:
    1. Windows RE Tools partition (Size: 300 MB, Format: NTFS)
    2. System partition (ESP) (Size: 100 MB, Format: FAT32)
    3. Microsoft reserved partition (MSR) (Size: 128 MB)
    4. Windows partition (Primary, Extend: true, Letter: C, Format: NTFS)

- Image Installation:
  - OS Image Index: 6
  - Install To: Disk 0, Partition 4
  - Install To Available Partition: false
  - Will Show UI: OnError

- User Data:
  - Product Key: *Not specified (Uncomment and insert your own key if using retail or volume license ISOs)*
  - Accept EULA: true
  - Full Name: WinUser
  - Organization: *Not specified*

- Offline Servicing:
  - Enable LUA: false

- Generalize:
  - Skip Rearm: 1

- Specialize:
  - Input Locale: English (United States)
  - System Locale: English (United States)
  - UI Language: English (United States)
  - UI Language Fallback: English (United States)
  - User Locale: English (United States)
  - Skip Auto Activation: true
  - CEIP Enabled: false
  - Computer Name: Win-PC
  - Product Key: W269N-WFGWX-YVC9B-4J6C9-T83GX

- OOBE System:
  - Auto Logon:
    - Username: WinUser
    - Password: *P@ssw0r3d@123*
    - Enabled: true
  - OOBE:
    - Hide EULA Page: true
    - Hide OEM Registration Screen: true
    - Hide Online Account Screens: true
    - Hide Wireless Setup in OOBE: true
    - Network Location: Home
    - Skip User OOBE: true
    - Skip Machine OOBE: true
    - Protect Your PC: 1
  - User Accounts:
    - Local Accounts:
      - Name: WinUser
      - Description: *Not specified*
      - Display Name: WinUser
      - Group: Administrators
      - Password: *P@ssw0r3d@123* (Plaintext: true)
  - Registered Owner: WinUser
  - Disable Auto Daylight Time Set: false
  - First Logon Commands:
    1. Control Panel View: Set to Icons view
    2. Control Panel Icon Size: Set to normal
    3. Password Never Expires: Set the user's password to never expire
   
  - Please rename the XML file as autounattend.xml and then burn that into the ISO in the root, and then use that ISO image to install windows 11.
