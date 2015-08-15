# Contributor: Tom Newsom <Jeepster@gmx.co.uk>
# Maintainer: Jason Chu <jason@archlinux.org>
# Contributor: Joker-jar <joker-jar@yandex.ru>


pkgname=dgen-sdl
pkgver=1.31
pkgrel=1
pkgdesc="An emulator for Sega Genesis/Mega Drive systems ported to SDL"
arch=('i686' 'x86_64')
url="http://dgen.sourceforge.net/"
license=('BSD')
depends=('sdl' 'libgl' 'libarchive')
makedepends=('nasm')
source=("http://downloads.sourceforge.net/dgen/${pkgname}-${pkgver}.tar.gz")
md5sums=('3f297010cc17c471c8c66652d9dee905')


build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr --with-extra-opt
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}/" install

  install -D -m644 COPYING "${pkgdir}/usr/share/licenses/${pkgname}/COPYING"
}

# vim:set ts=2 sw=2 et:
