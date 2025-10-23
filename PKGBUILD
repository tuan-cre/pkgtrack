# Maintainer: Tuan <lhtuan7924@gmail.com>
pkgname=pkgtrack
pkgver=1.0.0
pkgrel=1
pkgdesc="A lightweight pacman package snapshot and rollback tracker"
arch=('any')
url="https://github.com/tuan-cre/pkgtrack"  # use your actual GitHub username
license=('MIT')
depends=('pacman' 'bash')

# Git source
source=("$pkgname::git+$url.git")
sha256sums=('SKIP')

package() {
  # The binary script is at the root of the cloned repo
  install -Dm755 "$srcdir/pkgtrack" "$pkgdir/usr/bin/pkgtrack"

  # Create folder for snapshots
  install -d "$pkgdir/usr/share/pkgtrack/snaps"
}
