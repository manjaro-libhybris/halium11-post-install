# Maintainer: Bardia Moshiri <fakeshell@bardia.tech>

pkgname=halium11-post-install
pkgver=1$(date +%y%m%d)
pkgrel=4
pkgdesc="Manjaro libhybris Halium 11 post install script"
arch=('any')
url="https://github.com/manjaro-libhybris/halium11-post-install"
license=('GPL')
depends=('gzip' 'wget' 'systemd')
source=("halium11-post-install"
        "halium11-post-install.service"
        "android.conf"
        "vndservicemanager")
install=$pkgname.install
sha256sums=('e5bc39ff45ad1d29cfa389bc1417df2625e5cd28a863cc45a8db701dc1d96943'
            '6a1454bf151c760c2369551701cf7e46d2134ffa06e7750696bf1d777347979b'
            '5571610e4cee293e8776b33ec225ca24af05197cfd7c3ebd3c2e8d830efd55b0'
            '0b884bd2c085fefbcc945f7494cf792847b276b2844f643d56e7492e228621f1')

package() {
    install -Dm755 "${srcdir}/halium11-post-install" -t "${pkgdir}/usr/bin/"
    install -Dm644 "${srcdir}/halium11-post-install.service" -t "${pkgdir}/usr/lib/systemd/system/"
    install -Dm644 "${srcdir}/android.conf" -t "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm755 "${srcdir}/vndservicemanager" -t "${pkgdir}/usr/lib/droid-vendor-overlay/bin/"
}
