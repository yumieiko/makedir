pkgname="makedir"
pkgver="1.0.0"
pkgrel="1"
pkgdesc="Rewrite mkdir unix command with std::filesystem"
arch=("any")
url="https://github.com/yumieiko/makedir"
depends=("clang")
source=("main.cpp")
sha512sums=("SKIP")

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  cmake .
  make

}
package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  cmake --install . --prefix "${pkgdir}/usr"
  # clang++ "${srcdir}/main.cpp" -o "${pkgdir}/makedir"
}
