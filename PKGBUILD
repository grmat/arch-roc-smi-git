# Maintainer: grmat <grmat@sub.red>

pkgname=roc-smi-git
_pkgname=ROC-smi
pkgdesc='ROC System Management Interface'
pkgver=1.5.0.r0.g0470494
pkgrel=1
arch=('x86_64')
license=('MIT')
makedepends=('git')
depends=('python')

source=("git+https://github.com/RadeonOpenCompute/${_pkgname}.git")
sha256sums=('SKIP')

pkgver() {
  cd $srcdir/${_pkgname}
  git describe --long | sed 's/^roc-//;s/\([^-]*-g\)/r\1/;s/-/./g'
}

package() {
  mkdir -p "${pkgdir}/usr/bin"
  cp "${srcdir}/${_pkgname}/rocm-smi" "${pkgdir}/usr/bin/"
}
