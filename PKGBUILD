# Maintainer: Beerstorm <beerstorm.emberbeard@gmail.com>
pkgname=soundtouch4c
pkgver=0.5b
pkgrel=2
pkgdesc="A wrapper for soundtouch so you can use it in C programs"
arch=('i686' 'x86_64')
url="https://bitbucket.org/jart/soundtouch4c"
license=('GPL2')
depends=('soundtouch')
makedepends=('hgsvn' 'autoconf')
source=("hg+http://bitbucket.org/jart/soundtouch4c")
md5sums=('SKIP')

prepare() {
	cd "$srcdir/$pkgname"
	autoreconf -vif
}

build() {
	cd "$srcdir/$pkgname"
	./configure --prefix=/usr
	make || return 1
}

package() {
	cd "$srcdir/$pkgname"
	make DESTDIR="$pkgdir/" install
}

