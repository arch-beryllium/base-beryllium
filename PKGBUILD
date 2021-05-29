pkgname=base-beryllium
pkgver=0.4
pkgrel=1
arch=(aarch64)
license=(Unlicense)
source=('ignore-power-key.conf'
        'locale.conf'
        'first_time_setup.service'
        'first_time_setup.sh'
        'resizerootfs-hooks.sh'
        'resizerootfs-install.sh'
        'rootfsdetect-hooks.sh'
        'rootfsdetect-install.sh'
        'random-mac.conf')
sha256sums=('784c1237e8c553fd9717e4caf8b996abb4631348b27e3425bb8e39bd7e617476'
            '151b67da4450eb4f81143835f2342a4302284a0f336c4e13bb9de69009611c9b'
            'f5da6ca27d1b6d9d21f603be7831baf2524a2549a11de880829c094ef6d7f278'
            '269d8668f0f0e14d0044f84aa64696d28d27172cc869a49f5f0cb94d4c86e058'
            'a5c6210a890d0d37aadd8acad94038c7b8ef26d7bdc5301f9a64f989f8e10f46'
            '2110dd40aba8d9c9b5b408296eb3368303e94158d505440496dbb70a86e18023'
            'dc5c1a7e7d0c702daaa2de181b65b9f6a3272708fdbb65c3b53e2143bdab7dce'
            '8bef324054662f2873924a262a06ad18f7b0f8d4a28a61411965748a99cd3965'
            '06198df3c43c556d0fe8388fafc22527342714e163235cc7792cba18e3a903b2')

package_base-beryllium() {
  install=base-beryllium.install
  depends=(
    alsa-ucm-conf
    alsa-utils
    base-beryllium
    bluez
    bluez-libs
    bluez-utils
    firmware-xiaomi-beryllium
    glibc-locales
    haveged
    iw
    linux-beryllium
    linux-beryllium-headers
    networkmanager
    openssh
    pd-mapper-git
    qrtr-git
    reboot-mode
    rmtfs-git
    sudo
    tqftpserv-git
    usb-file-transfer
    usb-tethering
    wireless-regdb
    wpa_supplicant
    xdg-user-dirs
  )
  install -Dm644 "$srcdir"/random-mac.conf "$pkgdir"/etc/NetworkManager/conf.d/random-mac.conf
  install -Dm644 "$srcdir"/ignore-power-key.conf "$pkgdir"/etc/systemd/logind.conf.d/ignore-power-key.conf
  install -Dm644 "$srcdir"/locale.conf "$pkgdir"/etc/locale.conf
  install -Dm644 "$srcdir"/first_time_setup.service "$pkgdir"/usr/lib/systemd/system/first_time_setup.service
  install -Dm755 "$srcdir"/first_time_setup.sh "$pkgdir"/opt/first_time_setup.sh
  install -Dm755 "$srcdir"/resizerootfs-hooks.sh "$pkgdir"/usr/lib/initcpio/hooks/resizerootfs
  install -Dm755 "$srcdir"/resizerootfs-install.sh "$pkgdir"/usr/lib/initcpio/install/resizerootfs
  install -Dm755 "$srcdir"/rootfsdetect-hooks.sh "$pkgdir"/usr/lib/initcpio/hooks/rootfsdetect
  install -Dm755 "$srcdir"/rootfsdetect-install.sh "$pkgdir"/usr/lib/initcpio/install/rootfsdetect
}