# Maintainer: Tuan <lhtuan7924@gmail.com>

pkgname=pkgtrack
pkgver=1.0
pkgrel=1
pkgdesc="Simple pacman package snapshot and rollback tracker"
arch=('any')
url="https://github.com/tuan-cre/pkgtrack"
license=('MIT')
depends=('pacman' 'bash')

# Build from local folder named 'pkgtrack'
source=('pkgtrack')
sha256sums=('SKIP')

package() {
    # Install the main script
    install -Dm755 "$srcdir/pkgtrack" "$pkgdir/usr/bin/pkgtrack"
    
    # Create folder for snapshots
    install -d "$pkgdir/usr/share/pkgtrack/snaps"
}
