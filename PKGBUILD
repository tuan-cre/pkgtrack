# Maintainer: Tuan <lhtuan7924@gmail.com>
pkgname=pkgtrack
pkgver=1.0.0
pkgrel=1
pkgdesc="A lightweight pacman package snapshot and rollback tracker"
arch=('any')
url="https://github.com/<yourusername>/pkgtrack"
license=('MIT')
depends=('pacman' 'bash')
source=("$pkgname::git+$url.git")
sha256sums=('SKIP')

package() {
  install -Dm755 "$srcdir/$pkgname/pkgtrack" "$pkgdir/usr/bin/pkgtrack"
  install -d "$pkgdir/usr/share/pkgtrack/snaps"
}
