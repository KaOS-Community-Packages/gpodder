
pkgname=gpodder
pkgver=3.9.3
pkgrel=1
pkgdesc='A podcast receiver/catcher'
license=('GPL3')
arch=('x86_64')
url='http://gpodder.org/'
conflicts=('gpodder' 'gpodder2' 'gpodder-git')
depends=('iproute2' 'pygtk' 'python2-dbus' 'python2-podcastparser' 'python2-mygpoclient')
makedepends=('intltool' 'imagemagick' 'help2man')

source=("${pkgname}-${pkgver}.tar.gz::http://${pkgname}.org/source/${pkgver}")
install=gpodder.install

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"

  PYTHON=python2 DESTDIR=${pkgdir} make install || return 1

  sed -i -e 's|#!/usr/bin/python$|#!/usr/bin/python2|' \
         -e 's|#!/usr/bin/env python$|#!/usr/bin/env python2|' \
    $(find $pkgdir/usr/lib/python2.7/site-packages/gpodder/ -name '*.py')
}
md5sums=('56d891649d9ac8a0b9c5e47471a8119f')
sha1sums=('77aa49442fe3abe9aa84f69f5be5319cf5f6cb0b')
