# Maintainer: Oliver Gatti <gatti.oliver@gmail.com>
pkgname=uget-gtk2
_pkgname=uget
pkgver=1.8.2
pkgrel=1
pkgdesc="uget-1.8.2 is the old version of uGet, a download manager. 
This version depends only gtk2 and not gtk3, you can install the last 
stable version directly with pacman, as it is in community repository."
arch=('i686' 'x86_64')
url="http://uget.visuex.com/"
license=('LGPL')
depends=('curl>=7.17' 'gtk2>=2.14' 'hicolor-icon-theme' 'gstreamer0.10-base' 'libnotify')
makedepends=('intltool' 'pkgconfig>=0.9.0')
conflicts=('uget')
replaces=('uget') 
install=$pkgname.install
source=(http://sourceforge.net/projects/urlget/files/uget%20%28stable%29/$pkgver/$_pkgname-$pkgver.tar.gz/download)
md5sums=(42be57f08f41ffe4f5c4b60a4e8aa079)

build() {
  cd "$srcdir/$_pkgname-$pkgver"
  ./configure --prefix=/usr
  make || return 1
}

package() {
  cd "$srcdir/$_pkgname-$pkgver"
  make DESTDIR="$pkgdir" install
}


