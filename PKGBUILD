# $Id$
# Maintainer: keluoinhac <ineedyou.lonley at gmail.com>
 
pkgname=kaffeinety
_pkgname=KaffeineTY
pkgver=0.0.3
pkgrel=1
pkgdesc="A application to temporarily prevents dim screen action of power management and screensaver for KDE environment"
arch=('i686' 'x86_64')
url="http://kde-apps.org/content/show.php?content=159860"
license=('GPL')
depends=('kdebase-workspace')
makedepends=('cmake' 'automoc4')
source=("http://kde-apps.org/CONTENT/content-files/159860-${pkgname}-${pkgver}.tar.gz")
md5sums=('5eeb1cc9e0edf40ccb163a2eb4870064')
 
build() {
  cd "$srcdir/${pkgname}"
 
  mkdir -p build
  cd build
   
  cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DQT_QMAKE_EXECUTABLE=qmake-qt4 ..
  make
}
 
package() {
  cd "$srcdir/${pkgname}/build"
  make DESTDIR="${pkgdir}" install
} 
