# DeskRadar Web Flasher

This folder is ready to deploy on any HTTPS static host.

The manifest flashes bootloader, partition table, boot app and application
separately. The NVS partition at `0x9000` is intentionally omitted so Wi-Fi,
location and personal settings remain stored.

Before deployment, copy the current build artifacts into `firmware/`:

- `bootloader.bin`
- `partitions.bin`
- `boot_app0.bin`
- `firmware.bin`

Then deploy this folder over HTTPS.

On Windows, refresh the files after a successful PlatformIO build with:

```powershell
.\scripts\prepare-web-flasher.ps1
```
