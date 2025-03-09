# Maintainer: Alexander Courtis <alex@courtis.org>
pkgname=way-displays
pkgver=1.12.1
pkgrel=1
pkgdesc="way-displays: Auto Manage Your Wayland Displays"
arch=('x86_64' 'aarch64')
url="https://github.com/alex-courtis/way-displays"
license=('MIT')
depends=('wayland' 'wlroots' 'libinput' 'yaml-cpp')
makedepends=('git' 'make' 'gcc')
source=("https://github.com/alex-courtis/${pkgname}/archive/refs/tags/${pkgver}.tar.gz")
sha256sums=('a53edddde0aa61c9683bf54673bbfcd913f47eb1605cf013cffd2787ea9093a0')
install=way-displays.install

build() {
	cd "$pkgname-$pkgver"
	make CC=gcc CXX=g++ way-displays
}

package() {
	cd "$pkgname-$pkgver"
	make PREFIX="/usr" PREFIX_ETC="" DESTDIR="$pkgdir" install
}

