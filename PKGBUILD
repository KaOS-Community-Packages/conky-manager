
pkgname=conky-manager
pkgver=2.1
_ubuntu=~105~ubuntu14.10.1
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
sha256sums=('d9ad0b27fbf548c5a5c2f85e51609e1aee9149c3ded62fe2533f9ea5d013742c')

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
