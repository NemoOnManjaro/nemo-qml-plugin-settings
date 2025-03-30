# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=nemo-qml-plugin-settings
pkgver=0.1.3
pkgrel=1
pkgdesc="Nemomobile QML wrapper for QSettings class"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/nemo-qml-plugin-settings"
license=('LGPL-2.0-or-later')
depends=('qt6-declarative')
makedepends=('cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('b870fb470c43aaef20fe1f40779c28dd5f86f3b2e5f1e085881392a9f7f4ea98')

build() {
    cd $pkgname-$pkgver
    cmake -DCMAKE_INSTALL_PREFIX:PATH='/usr' .
    make all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}
