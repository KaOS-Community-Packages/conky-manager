pkgname=conky-manager
pkgver=2.4
_ubuntu=~136~ubuntu15.10.1
pkgrel=1
pkgdesc="GUI for managing Conky config files with options to browse and edit themes"
url="https://launchpad.net/conky-manager"
arch=('x86_64')
license=('GPL3')
depends=('cairo' 'conky' 'desktop-file-utils' 'gtk3' 'imagemagick' 'json-glib' 'libgee' 'p7zip' 'rsync')
makedepends=('vala')
options=('!emptydirs')
install=conky-manager.install
source=(${pkgname}-${pkgver}.tar.xz::https://launchpad.net/~teejee2008/+archive/ubuntu/ppa/+files/${pkgname}_${pkgver}${_ubuntu}.tar.xz
        makefile-roundup.patch)
sha512sums=('f691f067d0a921f19bb83118e3c845845582f7caaa76db4458e02e3897e0bc40ac6d62fb84b05d9061f8381fca7ab8470843a7d7b25dacf95fb363def29789d2'
            '3ce1bdcabfd9ee4713ed45a5d7b0dd913b69a0623f96c3aa4a49737ee685330aa7b4a9a369f7e4bd584e41d7eacbbaa9be6fff36db39186026c73bfb672ffc25')

prepare() {
  cd ${pkgname}-${pkgver}${_ubuntu}
  patch -Np0 < "${srcdir}/makefile-roundup.patch"
}

build() {
  cd ${pkgname}-${pkgver}${_ubuntu}
  make
}

package() {
  cd ${pkgname}-${pkgver}${_ubuntu}
  make DESTDIR="${pkgdir}" install
}

# vim: ts=2 sw=2 et:
