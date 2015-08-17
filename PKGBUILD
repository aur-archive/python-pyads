# Maintainer: Christoph Wiedemann <chwiede@gmail.com>
pkgname=python-pyads
pkgver=0.1
pkgrel=1
pkgdesc="Python implemented ADS-library"
arch=('any')
url="https://github.com/chwiede/pyads"
license=('MIT')
groups=()
depends=('python')
makedepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
changelog=


_gitroot="git://github.com/chwiede/pyads.git"

build() {

	### go into sources
	cd "$srcdir"
	msg "Connecting to GIT server..."

	### get sources
	if [[ -d "$pkgname-$pkgver" ]]; then
		cd "$pkgname-$pkgver"
		git pull origin
		msg "GIT update done!"
	else
		git clone "$_gitroot" "$pkgname-$pkgver"
		msg "GIT clone done!"
	fi

}


package() {
	cd "$srcdir/$pkgname-$pkgver"
	python setup.py install --root="$pkgdir/" --optimize=1
}
