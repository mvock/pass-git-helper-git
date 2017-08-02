# Maintainer: Markus Arians
pkgname=pass-git-helper
pkgver=0.1.r15.gb93f19c
pkgrel=1
epoch=
pkgdesc="A git credential helper interfacing with pass, the standard unix password manager."
arch=('any')
url="https://github.com/languitar/pass-git-helper"
license=('LGPLv3')
groups=()
depends=('python' 'python-xdg')
makedepends=('python')
checkdepends=()
optdepends=()
provides=('pass-git-helper')
conflicts=('pass-git-helper')
replaces=()
backup=()
options=()
install=
changelog=
source=("pass-git-helper::git+https://github.com/languitar/pass-git-helper.git")
noextract=()
md5sums=('SKIP')
validpgpkeys=()

pkgver() {
    cd "$pkgname"
    git describe --long --tags | sed 's/\([^-]*-g\)/r\1/;s/-/./g;s/^release\.//g'
}

build() {
	cd "$pkgname"
    python setup.py build
}

package() {
	cd "$pkgname"
    python setup.py install --root="${pkgdir}"
}
