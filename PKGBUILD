
pkgname=gpodder
pkgver=3.10.7
pkgrel=2
pkgdesc='Podcast client written in Python using GTK+'
arch=('x86_64')
url='https://gpodder.github.io/'
license=(GPL3)
depends=(gtk3 python-cairo python-dbus python-gobject python-mygpoclient python-podcastparser)
makedepends=(intltool)
source=($pkgname-$pkgver.tar.gz::http://github.com/gpodder/$pkgname/archive/$pkgver.tar.gz)
sha256sums=('85a7beec3f63c6768c811482ad6e934b0527c29f03e903ca0f82d2e764cdad76')

build() {
  cd $pkgname-$pkgver
  make messages
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir" install
}
