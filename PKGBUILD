# Maintainer: DUCRETTET Philippe <ecolinux@gmx.fr>

pkgname=leptonica-up
pkgver=1.69
pkgrel=1
pkgdesc="Software that is broadly useful for image processing and image analysis applications"
arch=('i686' 'x86_64')
url="http://www.leptonica.com/"
license=('custom')
options=(!libtool)
provides=('leptonica')
conflicts=('leptonica')
depends=('giflib' 'libjpeg' 'libpng' 'libtiff' 'zlib' 'libwebp>=0.2.1')
source=(http://www.leptonica.com/source/leptonica-${pkgver}.tar.gz)
md5sums=('d4085c302cbcab7f9af9d3d6f004ab22')

build() {
  cd ${srcdir}/leptonica-${pkgver}
  ./configure --prefix=/usr
  make
}

package() {
  cd ${srcdir}/leptonica-${pkgver}
  make DESTDIR=${pkgdir} install
  install -D leptonica-license.txt ${pkgdir}/usr/share/licenses/leptonica/leptonica-license.txt
}
