pkgname=vrms-arch
pkgver=20130302
pkgrel=1
pkgdesc="vrms for ArchLinux"
arch=('x86_64')
url="https://github.com/orospakr/${pkgname}"
license=('custom:BSD3')
depends=('python3' 'pyalpm')
source=("git+https://github.com/orospakr/${pkgname}.git")
md5sums=('SKIP')

build() {
  cd "$srcdir/${pkgname}"
  python3 setup.py build
}

package() {
  cd "$srcdir/${pkgname}"
  python3 setup.py install --root=${pkgdir}
  install -Dm 644 COPYING "${pkgdir}/usr/share/license/${pkgname}/LICENSE"
}
