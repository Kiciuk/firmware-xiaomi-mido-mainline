
pkgname=firmware-xiaomi-mido-mainline
pkgver=5
pkgrel=0
pkgdesc="Firmware for Xiaomi Redmi Note 4x"
url="https://github.com/Kiciuk/proprietary_firmware_mido"
arch="aarch64"
license="proprietary"
options="!check !strip !archcheck"
_commit="bc001cbb255a0ded2b58af07b93f712cd9322483"
source="https://github.com/Kiciuk/proprietary_firmware_mido/archive/$_commit.zip"
builddir="$srcdir/proprietary_firmware_mido-$_commit"

_fwdir="/lib/firmware/postmarketos"

package() {
	# parent package is empty
	mkdir -p "$pkgdir"

	# modem firmware
	install -Dm644 modem/mba.mbn -t "$pkgdir/$_fwdir"
	install -Dm644 modem/modem.* -t "$pkgdir/$_fwdir"

	# video firmware
	install -Dm644 apnhlos/venus.* -t "$pkgdir/$_fwdir"

	# WiFi/BT firmware
	install -Dm644 apnhlos/wcnss.* -t "$pkgdir/$_fwdir"
	install -Dm644 firmware/wlan/prima/WCNSS_qcom_wlan_nv.bin -t "$pkgdir/$_fwdir"/wlan/prima

	# ADSP firmware
	install -Dm644 modem/adsp.* -t "$pkgdir/$_fwdir"

	# GPU firmware
	install -Dm644 apnhlos/a506_zap.* -t "$pkgdir/$_fwdir"
}

