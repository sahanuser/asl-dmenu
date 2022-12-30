# Maintainer: Derek Taylor <derek@distrotube.com>
pkgname=asl-dmenu
pkgver=1
pkgrel=3
epoch=
pkgdesc="A build of dmenu patched for centering, borders, grids, numbers, line height, mouse support, fuzzy matching and highlighting."
arch=(x86_64)
url="https://github.com/asterlinux/asl-dmenu.git"
license=('MIT')
groups=()
depends=(ttf-hack ttf-joypixels)
makedepends=(git)
checkdepends=()
optdepends=()
provides=(dmenu)
conflicts=(dmenu)
replaces=()
backup=()
options=()
install=
changelog=
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

build() {
	cd asl-dmenu
	make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
    cd asl-dmenu  
    mkdir -p ${pkgdir}/opt/${pkgname}
    cp -rf * ${pkgdir}/opt/${pkgname}
    make PREFIX=/usr DESTDIR="${pkgdir}" install
}
