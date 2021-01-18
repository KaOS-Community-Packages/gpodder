
pkgname=gpodder
pkgver=3.10.17
pkgrel=1
pkgdesc='Podcast client written in Python using GTK+'
arch=('x86_64')
url='https://gpodder.github.io/'
license=(GPL3)
depends=(gtk3 python3-cairo dbus-python3 python3-gobject3 python-mygpoclient python-podcastparser)
makedepends=(intltool)
source=($pkgname-$pkgver.tar.gz::http://github.com/gpodder/$pkgname/archive/$pkgver.tar.gz)
sha256sums=('36a04e4d6a81f50b50d1f7691955d4f460e72f71b9519dad42b805a987434210')

build() {
  cd $pkgname-$pkgver
  make messages
}

package() {
  cd $pkgname-$pkgver
  make DESTDIR="$pkgdir" install
}
