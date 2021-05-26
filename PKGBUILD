# Maintainer: uttarayan21 <uttarayan21@disroot.org>

pkgname=windows10ame-git
_pkgname=windows10ame
pkgver=git
pkgrel=1
pkgdesc="Windows 10 amelioration script"

arch=('x86_64')
url="https://github.com/uttarayan21/windows10ame"
license=('MIT')

depends=('7z' 'git' 'curl')
provides=("windows10ame=${pkgver}")
conflicts=("windows10ame")
makedepends=('git')
source=("$pkgname::git+${url}.git")
md5sums=('SKIP')


pkgver() {
    cd "$pkgname"
    echo "$(git rev-parse --short HEAD)"
}

package() {
    cd "$pkgname"
    install -Dm755 "ame.sh" "$pkgdir/usr/bin/ame"
    install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/$_pkgname/LICENSE"
}

