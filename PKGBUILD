
pkgname=conky-manager
pkgver=2.0.3
_ubuntu=~102~ubuntu14.10.1
pkgrel=1
pkgdesc="Simple tool for managing conky scripts. (stable version)"
arch=('x86_64')
url="http://teejeetech.blogspot.in/"
license=('GPL2')
depends=('cairo' 'conky' 'desktop-file-utils' 'gtk3' 'imagemagick'
	 'json-glib' 'libgee06' 'libsoup' 'p7zip' 'rsync')
makedepends=('gettext' 'vala')
conflicts=('conky-manager-bzr')
options=(!emptydirs)
install="$pkgname.install"
source=("http://ppa.launchpad.net/teejee2008/ppa/ubuntu/pool/main/c/${pkgname}/${pkgname}_${pkgver}${_ubuntu}.tar.xz")
sha256sums=(' 4e07316c259bf20071510982a2409c9e4e1e9ef7cf3e4b0e1a60f94c0532cc1e')

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
