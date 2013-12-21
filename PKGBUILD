pkgname=pbar-gh-git
pkgver=1
pkgrel=1
pkgdesc="Progress bar in pacman style"
url="https://github.com/ritze/pbar"
license="GPL"
arch=('any')
makedepends=('git')
depends=('bash')
conflicts=('pbar')
source=("${pkgname}::git+https://github.com/ritze/pbar.git#branch=master")
md5sums=('SKIP')

pkgver() {
  cd "${srcdir}/${pkgname}"
  echo "0.$(git rev-list --count HEAD).$(git describe --always | sed 's|-|.|g')"
}

package() {
  cd "${srcdir}/${pkgname}"
  mkdir -p ${pkgdir}/usr/bin
  install -m 755 pbar ${pkgdir}/usr/bin/pbar
}
