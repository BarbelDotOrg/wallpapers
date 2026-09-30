# Maintainer: Barbel <barbel@barbel.org>
pkgname=barbelos-wallpapers
pkgver=2.0.0
pkgrel=1
pkgdesc="Wallpapers for BarbelOS"
arch=('any')
url="https://github.com/barbeldotorg/wallpapers"
license=('CC-BY-4.0')  
optdepends=('cosmic-session: to use as a COSMIC background')
source=()  
sha256sums=()

package() {
    install -d "$pkgdir/usr/share/backgrounds/wallpapers"
    for dir in "$srcdir/pictures"/*/; do
        category=$(basename "$dir")
        for file in "$dir"*; do
            install -m644 "$file" \
                "$pkgdir/usr/share/backgrounds/wallpapers/${category}-$(basename "$file")"
        done
    done
}