# Maintainer: Victor Sosa <victorsosadev@gmail.com>

pkgname=vshyprland-manager
pkgver=1.0.0
pkgrel=1
pkgdesc="Visual configuration editor for Hyprland — edit window manager settings with live preview"
arch=('any')
url="https://github.com/victorsosaMx/vsHyprland-Manager"
license=('MIT')
depends=(
    'python'
    'python-gobject'
    'python-cairo'
    'hyprland'
)
optdepends=(
    'hyprexpo: overview plugin configuration support'
    'hyprfocus: focus animation plugin configuration support'
)
source=("$pkgname-$pkgver.tar.gz::https://github.com/victorsosaMx/vsHyprland-Manager/archive/refs/tags/v$pkgver.tar.gz")
sha256sums=('SKIP')

package() {
    cd "vsHyprland-Manager-$pkgver"

    # main executable
    install -Dm755 vshyprland-manager \
        "$pkgdir/usr/bin/vshyprland-manager"

    # desktop entry
    install -Dm644 vshyprland-manager.desktop \
        "$pkgdir/usr/share/applications/vshyprland-manager.desktop"

    # icon
    install -Dm644 vshyprland-manager.png \
        "$pkgdir/usr/share/icons/hicolor/1024x1024/apps/vshyprland-manager.png"

    # license
    install -Dm644 LICENSE \
        "$pkgdir/usr/share/licenses/$pkgname/LICENSE"

    # docs
    install -Dm644 README.md    "$pkgdir/usr/share/doc/$pkgname/README.md"
    install -Dm644 CHANGELOG.md "$pkgdir/usr/share/doc/$pkgname/CHANGELOG.md"
}
