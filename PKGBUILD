# Maintainer: Hooregi <hooregi@halo.fm>
pkgname=st-hooregi-git
pkgver=0.8.5.r1150.06cb235
pkgrel=1
epoch=
pkgdesc="Hooregi's build of suckless' simple terminal (st)"
arch=(x86_64)
url="https://gitlab.com/Hooregi/st.git"
license=('MIT')
groups=()
depends=('libxft')
makedepends=('git')
checkdepends=()
optdepends=('dmenu')
provides=('st')
conflicts=('st')
replaces=()
backup=()
options=()
install=
changelog=
source=("git+$url")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
	cd "${_pkgname}"
  printf "0.8.5.r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

build() {
	cd st
  make X11INC=/usr/include/X11 X11LIB=/usr/lib/X11
}

package() {
  cd st
  mkdir -p ${pkgdir}/opt/${pkgname}
  cp -rf * ${pkgdir}/opt/${pkgname}
  make PREFIX=/usr DESTDIR="${pkgdir}" install
  install -Dm644 LICENSE "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
  install -Dm644 README "${pkgdir}/usr/share/doc/${pkgname}/README"
}
