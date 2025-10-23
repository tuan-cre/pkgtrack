# Maintainer: Tuan <lhtuan7924@gmail.com>
pkgname=pkgtrack
pkgver=1.0.0
pkgrel=1
pkgdesc="A lightweight pacman package snapshot and rollback tracker"
arch=('any')
url="https://github.com/tuan-cre/pkgtrack"
license=('MIT')
depends=('pacman' 'bash')

# If the repo is already cloned in the current folder, use it; otherwise, clone
if [ -d "$pkgname" ]; then
    source=("$pkgname::.")
else
    source=("$pkgname::git+$url.git")
fi

sha256sums=('SKIP')

package() {
    # If building from git, the script is in $srcdir/pkgtrack
    # If building from local, the script is in $srcdir (current folder)
    if [ -f "$srcdir/pkgtrack" ]; then
        install -Dm755 "$srcdir/pkgtrack" "$pkgdir/usr/bin/pkgtrack"
    else
        install -Dm755 "$srcdir/$pkgname/pkgtrack" "$pkgdir/usr/bin/pkgtrack"
    fi

    # Create folder for snapshots
    install -d "$pkgdir/usr/share/pkgtrack/snaps"
}
