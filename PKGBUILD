pkgname=ring-kde
pkgver=2.1.0
pkgrel=1
pkgdesc="distributed and secured communications"
license=('GPL')
arch=('i686' 'x86_64')
url="http://www.ring.cx/"
depends=('libringclient' 'kio' 'hicolor-icon-theme')
makedepends=('cmake' 'extra-cmake-modules')
source=("git+git://anongit.kde.org/ring-kde#tag=${pkgver}")
md5sums=('SKIP')

prepare() {
  cd "${srcdir}/ring-kde"

}

build() {
  cd "${srcdir}/ring-kde"
  cmake -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=/usr .
  make
}

package() {
  cd "${srcdir}/ring-kde"
  make DESTDIR="$pkgdir" install
}

