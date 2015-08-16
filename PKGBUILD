# Maintainer: Colin Woodbury <colingw@gmail.com>
_hkgname=nanq
pkgname=nanq
pkgver=0.1.1.2
pkgrel=1
pkgdesc="Performs 漢字検定 (National Kanji Exam) level analysis on given Kanji."
url="https://github.com/fosskers/nanq"
license=('GPL-3')
arch=('i686' 'x86_64')
makedepends=('ghc' 'haskell-containers>=0.4.0.0')
depends=('gmp')
options=('strip')
source=(https://github.com/downloads/fosskers/nanq/${_hkgname}-${pkgver}.tar.gz)
md5sums=('1f9c994875ee06e3c7d706e149ae2690')
build() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup configure --prefix=/usr --docdir=/usr/share/doc/${pkgname} -O
    runhaskell Setup build
}
package() {
    cd ${srcdir}/${_hkgname}-${pkgver}
    runhaskell Setup copy --destdir=${pkgdir}
}
