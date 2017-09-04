pkgname=desktime
pkgver=1.46
pkgrel=0
pkgdesc="Desktime client for Linux (beta)"
arch=('i686' 'x86_64')
url="http://desktime.com"
license=(custom)
depends=(desktop-file-utils hicolor-icon-theme libappindicator-gtk2 libxss)
install=$pkgname.install

if [[ $CARCH == 'i686' ]]; then
    source=("https://desktime.com/storage/updates/linux/beta/desktime-linux_1.46_i386.deb")
    md5sums=('54f131beff04f96390c6466dc5c5cd3f')
else
    source=("https://desktime.com/storage/updates/linux/beta/desktime-linux_1.46_x64.deb")
    md5sums=('9dd753e04151436068275fc93512712e')
fi

prepare()
{
    echo
}

package()
{
    cd "$srcdir"
    bsdtar -xf data.tar.xz -C "$srcdir/"

    install -Dm755 "$srcdir/"usr/bin/desktime-linux "$pkgdir/"usr/bin/desktime-linux
    install -Dm644 "$srcdir/"usr/share/applications/desktime.desktop "$pkgdir/"usr/share/applications/desktime.desktop
    install -Dm644 "$srcdir/"usr/share/doc/desktime-linux/changelog.gz "$pkgdir/"usr/share/doc/desktime-linux/changelog.gz
    install -Dm644 "$srcdir/"usr/share/doc/desktime-linux/copyright "$pkgdir/"usr/share/doc/desktime-linux/copyright
    install -Dm644 "$srcdir/"usr/share/icons/desktime.png "$pkgdir/"usr/share/icons/desktime.png

}

# vim:et:sw=4:sts=4
