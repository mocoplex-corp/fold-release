## FoldDisplay Windows Host 0.1.828

Signed Windows host installers for x64 and ARM64.

### Included

- Driver-free mirroring of the current Windows desktop to a FoldDisplay receiver
- More reliable reconnect and session-state handling
- Crash and dead-capture recovery fixes
- Full-resolution mirroring fixes
- Video converter resource-leak fixes
- Local setup guide available from the tray app

The MSI contains no display driver, INF, catalog, driver installer, or NT service. The separately distributed virtual-display driver remains optional and is only needed for extended-desktop mode.

Silent installation: `msiexec /i <installer.msi> /quiet /norestart`

Both installers and their packaged executables are Authenticode signed by **Mocoplex, Inc.** SHA-256 values are provided in `SHA256SUMS-0.1.828.txt`.
