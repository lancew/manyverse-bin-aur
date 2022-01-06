# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

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
# https://github.com/staltz/manyverse/releases/download/v0.2201.5-beta/manyverse-0.2201.5-beta.tar.gz
source=("https://github.com/staltz/manyverse/releases/download/v${pkgver/_/-}/$pkgname-${pkgver/_/-}.tar.gz")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

#prepare() {
#	cd "$pkgname-$pkgver"
#	patch -p1 -i "$srcdir/$pkgname-$pkgver.patch"
#}

#build() {
#	cd "$pkgname-$pkgver"
#	./configure --prefix=/usr
#	make
#}

#check() {
#	cd "$pkgname-$pkgver"
#	make -k check
#}

package() {
  mkdir -p "${pkgdir}/usr/bin/manyverse"
  cp -r "${srcdir}/$pkgname-${pkgver//_/-}" "${pkgdir}/usr/bin"
  mv "${pkgdir}/usr/bin/$pkgname-${pkgver//_/-}" "${pkgdir}/usr/bin/manyverse_bin"
  rm -rf "${pkgdir}/usr/bin/manyverse"
  echo '/usr/bin/manyverse_bin/manyverse' > "${srcdir}/manyverse.sh"
  cp "${srcdir}/manyverse.sh" "${pkgdir}/usr/bin/manyverse"
  chmod +x "${pkgdir}/usr/bin/manyverse"
}
