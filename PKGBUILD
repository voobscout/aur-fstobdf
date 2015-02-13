# Maintainer: Voobscout <voobscout+aur@gmail.com>
pkgname=xorg-xfs-fstobdf
pkgver=1.0.6
pkgrel=1
pkgdesc="X Font Server - fstobdf"
arch=('i686' 'x86_64')
license=('GPL2')
makedepends=('git' 'pkg-config' 'autoconf' 'automake' 'gettext' 'xproto' 'xtrans' 'wget')
url="http://xorg.freedesktop.org/archive/individual/app"
provides=('xorg-xfs-fstobdf')
optdepends=('xorg-xfs' 'xorg-xfstt')
source=("http://xorg.freedesktop.org/archive/individual/app/fstobdf-$pkgver.tar.gz")
sha256sums=('bb903ae76cbcb0a08a71f06762b64db7d5c2064f6e88e8dc3a604e76d0bcb93d')
options=(!strip)

build() {
  cd ${srcdir}/fstobdf-${pkgver}
  msg "Configuring fstobdf..."
  ./configure --prefix=/usr
  msg "Compiling fstobdf... "
  make
}

package() {
  msg "Installing fstobdf"
  cd ${srcdir}/fstobdf-${pkgver}
  make DESTDIR=${pkgdir} install
}

# vim:set ts=2 sw=2 et:
