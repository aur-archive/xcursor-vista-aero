#######
pkgname=xcursor-vista-aero
_pkgname=vista-aero
pkgver=0
pkgrel=1
pkgdesc="a clone of Windows Vista's default cursors."
url="https://github.com/izmntuk"
arch=('any')
license=('unknown')
source=("${_pkgname}-${pkgrel}.tar")
makedepends=('bash' 'xorg-xcursorgen')
md5sums=('e6ed628c4dd81fbc3e43a9524f716844')

build() {
	cd "${srcdir}/${_pkgname}"
	./makexmc.sh
	rm -r vista-aero-cursors-png makexmc.sh
}

package() {
	mkdir -p "${pkgdir}/usr/share/icons"
	cp -r "${srcdir}/${_pkgname}" "${pkgdir}/usr/share/icons"
	find "${pkgdir}/usr/share/icons" -type d -exec chmod 755 '{}' \;
	find "${pkgdir}/usr/share/icons" -type f -exec chmod 644 '{}' \;
}
