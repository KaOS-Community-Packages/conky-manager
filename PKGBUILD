
pkgname=conky-manager
pkgver=2.0.2
_ubuntu=~98~ubuntu14.10.1
pkgrel=1
pkgdesc="Simple tool for managing conky scripts. (stable version)"
arch=('x86_64')
url="http://teejeetech.blogspot.in/"
license=('GPL2')
depends=('cairo' 'conky' 'desktop-file-utils' 'gtk3' 'imagemagick'
	 'json-glib' 'libgee06' 'libsoup' 'p7zip' 'rsync')
makedepends=('vala')
conflicts=('conky-manager-bzr')
options=(!emptydirs)
install="$pkgname.install"
source=("http://ppa.launchpad.net/teejee2008/ppa/ubuntu/pool/main/c/${pkgname}/${pkgname}_${pkgver}${_ubuntu}.tar.xz")
sha256sums=('959e2d13c669f1caa3fbd32d3f79c29b5b47753eb1faffc30a4e9ab9b7749bdb')

build() {
  #cd "$srcdir/$pkgname-$pkgver"
  cd "$srcdir"/recipe*

  make
}

package() {
  #cd "$srcdir/$pkgname-$pkgver"
  cd "$srcdir"/recipe*

  make DESTDIR="$pkgdir" install
}
