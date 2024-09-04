<h1 align="center"> Infinix X1 Pro Hackintosh</h1>

<br>
<p align="center">
  <img
      src="assets/laptop.png"
      alt="x1 pro"
      class="center"
      width=500px>

A Hackintosh project for the Infinix X1 PRO 14" built on top of the [OpenCore](https://github.com/acidanthera/OpenCorePkg) bootloader

<h3>macOS Version Supported:</h3>

Ventura latest version (I only tested for ventura, but it should work for other versions too. Just change the `.kext` files according to your version)

<img alt="ventura-information.png" src="assets/ventura-information.png"/>
Eligible for beta tester (Which means you can do OTA update)
<img alt="beta-tester.png" src="assets/beta-tester.png"/>

<h3>Hardware Information</h3>

| Component        | Model                                      |
|------------------|--------------------------------------------|
| Processor        | Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz  |
| Memory           | 16GB LPDDR4X 3200MHz                       |
| Storage          | TEAM TM8FP6 512GB NVMe SSD                 |
| Graphics         | Intel Iris Plus Graphics G7                |
| Audio            | Realtek ALC269 (alcid = 99)                |
| Wifi & Bluetooth | Intel AX201                                |

<h3>What's working</h3>
<table>
  <thead>
    <tr>
      <th>Component</th>
      <th>Device</th>
      <th colspan=2>Status</th>
    </tr>
  </thead>
  <tbody>
  <!-- Processor -->
    <tr>
      <td>CPU</td>
      <td>Intel(R) Core(TM) i7-1065G7 CPU @ 1.30GHz<br>
      <td style="text-align: center;">✅</td>
      <td>Natively supported (since macOS Catalina).</td>
    </tr>
  <!-- Graphics -->
    <tr>
      <td rowspan=2>Graphics</td>
      <td>Intel Iris Plus Graphics G7 (Ice Lake)</td>
      <td style="text-align: center;">✅</td>
      <td>Full acceleration (QE/CI)</td>
    </tr>
    <tr>
    </tr>
  <!-- Displays -->
    <tr>
      <td rowspan=2>Displays</td>
      <td>13,9-inch (1920 × 1080)<br>(IPS 60 Hz)</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (with backlight control).</td>
    </tr>
    <tr>
    </tr>
  <!-- Interfaces -->
    <tr>
      <td rowspan=6>Interfaces</td>
      <td>Built-in Keyboard</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (with media keys and backlight control).</td>
    </tr>
    <tr>
      <td>Built-in Trackpad</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (GPIO pinned with multi-touch gestures)
<img src="assets/trackpad.png">
</td>
    </tr>
    <tr>
    </tr>
    <tr>
    </tr>
    <tr>
<tr>
</tr>
    </tr>
  <!-- Audio -->
    <tr>
      <td rowspan=2>Audio<br>(Realtek ALC269)</td>
      <td>Built-in speakers</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (with volume control).</td>
    </tr>
    <tr>
      <td>Built-in microphone</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (with volume controll)</td>
    </tr>
  <!-- Camera -->
    <tr>
      <td>Camera</td>
      <td>MTD Camera</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported</td>
    </tr>
  <!-- Wi-Fi + Bluetooth -->
    <tr>
      <td>Wi-Fi</td>
      <td rowspan=2>Intel AX201<br>(Wi-Fi 6 + Bluetooth 5.0)</td>
      <td rowspan=2 style="text-align: center;">✅</td>
      <td rowspan=2>Fully supported (with limited Continuity support).
<img src="assets/wifi.png">
<img src="assets/bluetooth.png">
</td>
    </tr>
    <tr>
      <td>Bluetooth</td>
    </tr>
  <!-- Storage -->
    <tr>
      <td>Storage</td>
      <td>TEAM TM8FP6 512GB NVMe SSD</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (with power management) and fiixed random kernel panic by adding (forceRenderStandby=0) in boot-args</td>
    </tr>
  <!-- Ports -->
    <tr>
      <td>Ports</td>
      <td>(Left)
• 1x USB 3.0 Gen 2 Type-A<br>
• 1x USB 3.0 Gen 2 Type-C<br>
• 1x USB 2.0 Gen 2 Type-C<br>
(Right)<br>• 1x USB 3.0 Gen 1 Type-A<br>
• 1x 3.5 mm Audio combo jack<br>
• 1x USB 3.0 Gen 2 Type-A<br>
• 1x USB 2.0 Gen 2 Type-A<br>
      <td style="text-align: center;">✅</td>
      <td>Fully supported.</td>
    </tr>
  <!-- Battery and Power -->
    <tr>
      <td rowspan=2>Battery</td>
      <td>Built-in Battery</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (with power reading).</td>
    </tr>
    <tr>
      <td>AC Power Adapter</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported (with hotplug and charge limit feature).</td>
    </tr>
  </tbody>
</table>


### Software Features:
<table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Feature</th>
      <th colspan=2>Status</th>
    </tr>
  </thead>
  <tbody>
  <!-- iServices -->
    <tr>
      <td colspan=2>iServices (iCloud)</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported.</td>
    </tr>
  <!-- Continuity -->
    <tr>
      <td rowspan=6>Continuity</td>
      <td>Airplay to Mac</td>
      <td style="text-align: center;">❌</td>
      <td>Untested.</td>
    <tr>
      <td>Sidecar</td>
      <td style="text-align: center;">❌</td>
      <td>Untested.</td>
    <tr>
      <td>Handoff</td>
      <td style="text-align: center;">❌</td>
      <td>Untested.</td>
    </tr>
    <tr>
      <td>Continuity Camera</td>
      <td style="text-align: center;">✅</td>
      <td>Supported.</td>
    </tr>
    <tr>
      <td>Universal Clipboard</td>
      <td style="text-align: center;">❌</td>
      <td>Untested.</td>
    </tr>
    <tr>
      <td>Universal Control</td>
      <td style="text-align: center;">❌</td>
      <td>Untested.</td>
    </tr>
  <!-- Sleep + Wake -->
    <tr>
      <td rowspan=2>Sleep / Wake</td>
      <td>Sleep</td>
      <td style="text-align: center;">✅</td>
      <td>Supported.</td>
    </tr>
    <tr>
      <td>Hibernation</td>
      <td style="text-align: center;">✅</td>
      <td>Supported.</td>
    </tr>
  <!-- Battery meter -->
    <tr>
      <td colspan=2>Battery Indication</td>
      <td style="text-align: center;">✅</td>
      <td>Fully supported.</td>
    </tr>
</table>

## Installation Guide

### BIOS Settings
#### Disable
* Secure boot
* Disable wakeup on wlan and bluetooth (chipset > PCH IO > disable wake on wlan+bt)
* Virtualization (VT-d > Advanced > cpu > virtualization technology)

#### Enable
* iGPU Memory `DVMT Pre-Allocated` to `64MB` or `MAX` (Advanced > System Agent (SA) Configuration > Graphics Configuration > DVMT Pre-Allocated)
* Set `DVMT Total Gfx Mem` to `MAX` (Advanced > System Agent (SA) Configuration > Graphics Configuration > DVMT Total Gfx Mem)
* Set `DVM Total Dfx Mem` to `256MB` or `MAX` (Advanced > System Agent (SA) Configuration > Graphics Configuration > DVM Total Dfx Mem)
* Intel Virtualization Technology (Advanced > CPU Configuration > Intel Virtualization Technology)
<br>
<br>
If those settings are not available in your BIOS, skip them and continue the installation.

### Create USB Installer
1. Download macOS Ventura from https://068fx-my.sharepoint.com/:f:/g/personal/ekopuryanto_068fx_onmicrosoft_com/EpzotHNX6yJOlCE-DJcATFMByyNJgirB_c5Ix7PGu1Fguw?e=0SB6Tv (Thanks for hackintosh lover Indonesia for providing the installer)
2. Download from this repository
3. Download flasher, you can use [Balena Etcher](https://www.balena.io/etcher/) or [TransMac](https://www.acutesystems.com/scrtm.htm)
4. Flash the macOS Ventura to your USB Drive
5. Mount the EFI partition of the USB Drive
6. Copy the EFI folder from this repository to the EFI partition of the USB Drive
7. Generate your own SMBIOS by using [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS)
8. Copy the generated SMBIOS to the EFI partition of the USB Drive
9. Boot from the USB Drive
10. Install macOS Ventura
11. After installation, boot from the USB Drive again
12. Copy the EFI folder from the EFI partition of the USB Drive to the EFI partition of your SSD
13. Reboot and enjoy

### Dual booting with Windows
1. Install macOS Ventura first
2. Backup your EFI folder
3. Install Windows
4. Boot from the USB Drive
5. Copy the EFI folder from the EFI partition of the USB Drive to the EFI partition of your SSD (if popup shows up, click replace)
6. Reboot and enjoy

### ⚠️ NOTE ⚠️
This EFI is not recommended for daily use, because it's still in development stage. If you want to use it for daily use, you can use it at your own risk.
I'm not responsible for any damage caused by this EFI.
