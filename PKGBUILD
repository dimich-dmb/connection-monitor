# Maintainer: Dmytro Bagrii <dimich.dmb@gmail.com>

pkgname=connection-monitor
pkgdesc="Connection Monitor displays connection on / off notifications"
pkgver=0.1
pkgrel=1
arch=(any)
license=('MIT')
depends=(bash iputils libnotify systemd)
backup=('etc/connection-monitor.conf')
source=(connection-monitor
        connection-monitor.conf
        connection-monitor.service
        LICENSE)
sha256sums=('458bc91b6dd54b306a09453c7c7bfc12d9166b6addbf10a982faa1ff2b5cc430'
            '740d6fb51ed685b45a2fe710218cbdf407db8b8d852337e6f203ceefac809342'
            'fcaf35356ef1880f08451ae643ee6f1dfa952821316d1bd2170390f62546a892'
            '90ea803b5ee3cb1b33430d5c16df59821b7560ff49030740c6ab763f1326171a')

package() {
    cd $srcdir
    install -Dm755 $pkgname "$pkgdir"/usr/lib/$pkgname/$pkgname
    install -Dm644 $pkgname.conf "$pkgdir"/etc/$pkgname.conf
    install -Dm644 $pkgname.service "$pkgdir"/usr/lib/systemd/system/$pkgname.service
    install -Dm644 LICENSE "$pkgdir"/usr/share/licenses/$pkgname/LICENSE
}
