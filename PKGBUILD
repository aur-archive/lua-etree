# Contributor: Anders Bergh <anders1@gmail.com>
# Maintainer: uzsolt <udvzsolt gmail com>
pkgname=lua-etree
pkgver=0.1.1
pkgrel=3
pkgdesc="A library that enables manipulation of XML documents in Lua"
arch=(i686 x86_64)
url="http://etree.luaforge.net"
license=('MIT')
depends=('lua-expat')
# LuaForge URLs are stupid, so $pkgver is not enough here
source=(http://luaforge.net/frs/download.php/2152/etree-0.1.1.tar.gz)
md5sums=('848d6f4a4aadbaba6470a879bfc46094')

build() {
  cd "$srcdir/etree-$pkgver"

  install -Dm644 LICENSE "$pkgdir/usr/share/licenses/$pkgname/LICENSE" || return 1

  make prefix="$pkgdir/usr" libdir="$pkgdir/usr/lib/lua/5.2" || return 1
  make prefix="$pkgdir/usr" libdir="$pkgdir/usr/lib/lua/5.2" install || return 1
}
