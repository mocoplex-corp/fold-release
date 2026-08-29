# FoldDisplay releases

Public, signed binary releases for FoldDisplay by Mocoplex, Inc.

## Windows host

Latest release: [v0.1.829](https://github.com/mocoplex-corp/fold-release/releases/tag/v0.1.829)

Permanent download links — they always resolve to the newest published release, so an installed app never points at a file that has been replaced:

- [Windows x64 MSI](https://github.com/mocoplex-corp/fold-release/releases/latest/download/FoldDisplay-x64.msi) — most Intel/AMD Windows PCs
- [Windows ARM64 MSI](https://github.com/mocoplex-corp/fold-release/releases/latest/download/FoldDisplay-arm64.msi) — Windows on ARM PCs
- [Virtual display driver, x64](https://github.com/mocoplex-corp/fold-release/releases/latest/download/FoldDisplay-Driver-x64.msi) — optional, for the extended desktop
- [Virtual display driver, ARM64](https://github.com/mocoplex-corp/fold-release/releases/latest/download/FoldDisplay-Driver-arm64.msi) — optional, for the extended desktop
- [macOS DMG](https://github.com/mocoplex-corp/fold-release/releases/latest/download/FoldDisplay-macOS.dmg) — Apple-notarized
- [SHA-256 checksums](https://github.com/mocoplex-corp/fold-release/releases/latest/download/SHA256SUMS.txt)

These are the **direct-download build**: screen mirroring works on its own, and
the tray offers the optional virtual display driver for anyone who wants a real
extended desktop.

### Microsoft Store package endpoints

The Store needs a versioned URL that does not redirect, so its packages live
under `downloads/<version>/` instead of the release assets:

- [Store x64 MSI](https://raw.githubusercontent.com/mocoplex-corp/fold-release/main/downloads/0.1.829/FoldDisplay-Store-x64-0.1.829.msi)
- [Store ARM64 MSI](https://raw.githubusercontent.com/mocoplex-corp/fold-release/main/downloads/0.1.829/FoldDisplay-Store-arm64-0.1.829.msi)
- [SHA-256 checksums](https://raw.githubusercontent.com/mocoplex-corp/fold-release/main/SHA256SUMS-Store-0.1.829.txt)

**These are a different build from the ones above, and the two are not
interchangeable.** The Store variant is mirror-only by construction: it is
compiled without the virtual-display capture source, has no driver download or
installation path, no extended-display controls, and does not carry the user
guide, because that guide is written about the extended display. Microsoft Store
policy 10.2.4.2 does not allow an app that includes or depends on a driver
Microsoft did not provide, and this variant is how FoldDisplay complies.

The `FoldDisplay-Store-` prefix exists because both builds otherwise produce a
file named `FoldDisplay-<arch>-<version>.msi`, and pointing a Store submission
at the wrong one is a mistake that is only visible after certification fails.

Neither MSI contains a display driver, INF, catalog, driver installer, or NT
service. The virtual-display driver is always a separate, optional package.

You can also install FoldDisplay from the [Microsoft Store](https://apps.microsoft.com/store/detail/XPDLJZ75GNBLXD).

## Links

- Product site: <https://fold.mocoplex.com/>
- Source code: <https://github.com/mocoplex-corp/folddisplay>
- Release history: <https://github.com/mocoplex-corp/fold-release/releases>

---

# FoldDisplay 릴리스

Mocoplex, Inc.가 서명한 FoldDisplay 공개 설치 파일 저장소입니다.

- 일반 Intel/AMD Windows PC는 `x64` MSI를 사용하세요.
- Windows on ARM PC는 `ARM64` MSI를 사용하세요.
- Windows 호스트는 드라이버 없이 현재 PC 화면을 휴대폰에 미러링합니다.
- 새 Windows 확장 화면을 만드는 가상 디스플레이 드라이버는 선택 기능이며 호스트 MSI에 포함되지 않습니다.
- `downloads/<버전>/FoldDisplay-Store-*.msi`는 **Microsoft Store 전용 빌드**입니다.
  가상 디스플레이 캡처 경로와 드라이버 설치 경로가 아예 컴파일되지 않은 미러링
  전용 빌드이며, 직접 다운로드용 설치 파일과 교체해서 쓸 수 없습니다.
