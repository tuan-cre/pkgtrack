# Maintainer: Tuan <youremail@example.com>

pkgname=pkgtrack
pkgver=1.0
pkgrel=1
pkgdesc="Simple pacman package snapshot and rollback tracker"
arch=('any')
url="https://github.com/yourusername/pkgtrack"
license=('MIT')
depends=('pacman' 'bash')
source=('pkgtrack')
sha256sums=('SKIP')

package() {
  install -Dm755 "$srcdir/pkgtrack" "$pkgdir/usr/bin/pkgtrack"
  install -d "$pkgdir/usr/share/pkgtrack/snaps"
}
