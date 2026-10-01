# AkisLink

Rootless phone-to-PC mobile internet over Wi-Fi Direct, with optional DPI bypass. Android forwards TCP/UDP through mobile data; Windows routes supported application traffic through a temporary sing-box network adapter. No remote VPN server is used.

**Preview release:** [AkisLink 2.0.0-preview.2](https://github.com/mazejk/AkisLink/releases/tag/v2.0.0-preview.2)

## Downloads

- [Android APK](https://github.com/mazejk/AkisLink/releases/download/v2.0.0-preview.2/AkisLink-2.0.0-preview.2.apk) — Android 10+, ARM64. Separately signed release package: `app.akislink.hotspot.release`.
- [Windows EXE](https://github.com/mazejk/AkisLink/releases/download/v2.0.0-preview.2/AkisLink-2.0.0-preview.2-windows-x64.exe) — Windows 10/11 x64, Windows PowerShell 5.1 and .NET Framework 4.8. Client and engine included; Windows asks for administrator permission when routing starts.
- [Complete release bundle](https://github.com/mazejk/AkisLink/releases/download/v2.0.0-preview.2/AkisLink-2.0.0-preview.2.zip) — binaries, corresponding source, notices, guides and SHA-256 checksums.

![AkisLink desktop](https://github.com/mazejk/AkisLink/releases/download/v2.0.0-preview.2/desktop-preview.png)

## Getting connected

1. Disconnect any old desktop client and stop PdaNet/other phone sharing.
2. Enable mobile data and Wi-Fi, open AkisLink on the phone, and start sharing.
3. Join the displayed Wi-Fi network on the PC with the displayed password.
4. Open the Windows EXE, enter that network name, select Connect and allow the administrator prompt.
5. Select Check internet, then try your applications.

**Default** keeps DPI bypass off. **Default + DPI Bypass** enables the tested OOB method for restricted platforms. Advanced settings expose custom methods. Both apps have visible English/Türkçe controls. Change hotspot name/password/band while phone sharing is stopped. Windows connection settings apply after reconnecting; language/theme apply immediately.

Windows has a borderless interface, light/dark/system themes and a matching tray popup. Its one connection button changes between Connect, Cancel and Disconnect. Closing hides to the tray by default; Disconnect restores normal routing. Disconnect before joining GSBWIFI or eduroam.

## Türkçe

AkisLink, root gerektirmeden Wi-Fi Direct üzerinden telefonun mobil internetini PC'ye iletir. DPI engel aşma isteğe bağlıdır. Uzak VPN sunucusu kullanılmaz.

APK'yi telefona kurun, eski paylaşımı durdurun ve AkisLink'te paylaşımı başlatın. PC'den gösterilen Wi-Fi ağına/parolaya katılın. Windows EXE'sini açın, ağ adını girip Bağlan'a tıklayın ve yönetici isteğine izin verin. Ardından İnterneti kontrol et'i kullanın.

**Varsayılan**, DPI engel aşmayı kapalı tutar. Kısıtlı platformlar için **Varsayılan + DPI engel aşma** seçilebilir. İki uygulamada da English/Türkçe görünürdür. Telefon Wi-Fi ayarları paylaşım dururken değiştirilir; PC bağlantı ayarları yeniden bağlanınca, dil/tema hemen uygulanır. GSBWIFI/eduroam'a geçmeden önce bağlantıyı kesin.

## Preview status

Build, configuration, GUI and cryptographic checks passed. The latest release still needs phone installation and end-to-end network testing. Carrier sharing accounting, sustained/screen-off stability, games/voice performance, campus Wi-Fi compatibility and general IPv6 support remain unverified. A successful internet check does not establish carrier billing behavior or support for every application/protocol. USB remains an ADB TCP diagnostic.

The APK is signed with a persistent release key. The Windows EXE has no Authenticode publisher signature. This is a prerelease for evaluation, with development continuing later.

## Source and notices

The exact source snapshot is attached as `Source.zip`; it includes Android, the modified native ByeDPI engine, Windows UI/launcher, branding and packaging/build instructions. Matching sing-box source is attached separately. Private signing keys, build caches and runtime logs are excluded.

AkisLink derives from [ByeDPIAndroid](https://github.com/dovecoteescapee/ByeDPIAndroid) (GPL-3.0), incorporates modified [ByeDPI](https://github.com/hufrea/byedpi) native code (MIT), and packages official [sing-box](https://github.com/SagerNet/sing-box) 1.14.2 (GPL-3.0-or-later). Preserve the included notices/licenses and corresponding source when redistributing. No PdaNet code or branding is distributed.
