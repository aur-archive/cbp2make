# Contributor: attila589 <attila589 at gmail dot com>
# Maintainer: Ben R <thebenj88 *AT* gmail *DOT* com>

pkgname=cbp2make
pkgver=rev147
pkgrel=1
pkgdesc="Makefile generation tool for Code::Blocks IDE"
arch=(i686 x86_64)
url="http://sourceforge.net/projects/cbp2make/"
license=('GPL')
depends=('gcc-libs')
makedepends=('doxygen')
source=(http://downloads.sourceforge.net/${pkgname}/${pkgname}-stl-${pkgver}-all.tar.7z)
sha256sums=('1b211abb8de00dc3048fccad6ebd076ab03dcb9f672cdff379de33a1346ed129')

build() {
  cd "${srcdir}/${pkgname}-stl-${pkgver}-all"
  mv cbp2make.cbp.mak.unix Makefile
  make
}

package() {
  mkdir -p "${pkgdir}/usr/bin/"
  install -Dm755 "${srcdir}/${pkgname}-stl-${pkgver}-all/bin/Release/cbp2make" "${pkgdir}/usr/bin/"
}
