# Maintainer: ZeStig <zestig@duck.com>
pkgname=stratos-calamares-config
pkgver=1.0
pkgrel=9
pkgdesc="StratOS Calamares config"
arch=('x86_64')
url="https://github.com/StratOS-Linux/StratOS-calamares-config"
license=('GPL')
depends=(
	'bash'
	'libpwquality'
)
conflicts=(
  'stratos-calamares-config-next'
)
source=()
install=stratos-calamares-config.install

prepare() {
    cp -r "$startdir/branding" "$srcdir/"
    cp -r "$startdir/modules" "$srcdir/"
    install -m 644 "$startdir/settings.conf" "$srcdir/"
}
package() {
    install -d "$pkgdir/etc/calamares"
    cp -r "$srcdir/branding" "$pkgdir/etc/calamares/"
    cp -r "$srcdir/modules" "$pkgdir/etc/calamares/"
    install -m 644 "$srcdir/settings.conf" "$pkgdir/etc/calamares/"
}
