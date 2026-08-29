## FoldDisplay Windows Host 0.1.829

Signed Windows host installers for x64 and ARM64.

### Included

- The setup and user guide pages are now served from the website rather than the copy inside the app, so corrected instructions and moved download links reach installs that already exist. The bundled copies remain as the offline fallback.
- The host now tells the receiver why a picture never starts. A pipeline that cannot begin - a locked desktop, or a virtual display driver that is not responding - previously left the phone showing "negotiating" indefinitely with nothing to explain it.
- Reconnect now happens in the host itself for the duration of the grace period, holding the virtual display across a short drop instead of relying on the tray to relaunch the whole process.
- Fixes for two transport lifetime faults that could terminate the process on a clean shutdown after any disconnect.
- The JSON parser bounds its nesting depth, closing a pre-authentication crash reachable from any peer that completes the TLS handshake.
- Input is only injected while streaming, so an unapproved peer cannot type into the PC.
- A mouse button held when the link drops is released, rather than leaving the desktop stuck mid-drag.
- Sign-out and shutdown now release the virtual display instead of leaving it attached into the next sign-in.
- The uptime clock no longer overflows after a few days, which used to freeze pacing and corrupt every timestamp.

The MSI contains no display driver, INF, catalog, driver installer, or NT service. The separately distributed virtual-display driver remains optional and is only needed for extended-desktop mode.

Silent installation: `msiexec /i <installer.msi> /quiet /norestart`

Both installers and their packaged executables are Authenticode signed by **Mocoplex, Inc.** SHA-256 values are provided in `SHA256SUMS-0.1.829.txt`.
