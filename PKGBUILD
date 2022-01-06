# Maintainer: Lance WIcks <lw@judocoach.com>
pkgname=manyverse
pkgver=0.2201.5_beta
pkgrel=1
epoch=
pkgdesc="A social network without the bad stuff, built on the peer-to-peer SSB protocol."
arch=('x86_64')
url="https://www.manyver.se/"
license=('MPL')
groups=()
depends=()
makedepends=()
checkdepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/staltz/manyverse/releases/download/v${pkgver/_/-}/$pkgname-${pkgver/_/-}.tar.gz")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

package() {
  mkdir -p "${pkgdir}/usr/bin/manyverse"
  mkdir -p "${pkgdir}/usr/share/applications/"
  cp -r "${srcdir}/$pkgname-${pkgver//_/-}" "${pkgdir}/usr/bin"
  mv "${pkgdir}/usr/bin/$pkgname-${pkgver//_/-}" "${pkgdir}/usr/bin/manyverse_bin"
  rm -rf "${pkgdir}/usr/bin/manyverse"
  echo '/usr/bin/manyverse_bin/manyverse' > "${srcdir}/manyverse.sh"
  cp "${srcdir}/manyverse.sh" "${pkgdir}/usr/bin/manyverse"
  chmod +x "${pkgdir}/usr/bin/manyverse"
  echo "
[Desktop Entry]
Type=Application
Name=manyverse
Comment=A social network without the bad stuff, built on the peer-to-peer SSB protocol
Path=/usr/bin
Exec=manyverse
Icon=manyverse
Terminal=false
Categories=Internet
" > "${srcdir}/manyverse.desktop"

  cp "${srcdir}/manyverse.desktop" "${pkgdir}/usr/share/applications/"
}
