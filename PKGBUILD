pkgname=julia
pkgver=1.5.4
pkgrel=1
arch=('x86_64')
pkgdesc='High-level, high-performance, dynamic programming language - official binaries'
url='https://julialang.org/'
license=('MIT')
source=("https://julialang-s3.julialang.org/bin/linux/x64/${pkgver:0:3}/julia-${pkgver}-linux-x86_64.tar.gz")
sha256sums=('80dec351d1a593e8ad152636971a48d0c81bfcfab92c87f3604663616f1e8bc5')
options=(!strip)

package() {
  mkdir -p ${pkgdir}/usr/share/licenses/julia
  cp -r julia-${pkgver}/{bin,etc,include,lib,share} ${pkgdir}/usr/
  install -Dm644 julia-${pkgver}/LICENSE.md \
      ${pkgdir}/usr/share/licenses/julia/LICENSE.md
}
