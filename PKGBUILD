# Maintainer: Bardia Moshiri <fakeshell@bardia.tech>

pkgname=halium11-post-install
pkgver=1$(date +%y%m%d)
pkgrel=2
pkgdesc="Manjaro libhybris Halium 11 post install script"
arch=('any')
url="https://github.com/manjaro-libhybris/halium11-post-install"
license=('GPL')
depends=('gzip' 'glibc-locales' 'wget' 'systemd')
source=("halium11-post-install"
        "halium11-post-install.service"
        "android.conf"
        "ril_subscription.conf"
        "90_manjaro.gschema.override")
install=$pkgname.install
sha256sums=('20f02f487c542962528e4103688f6a1b6fe2b68bfc556a8caf2f973a09cb575d'
            '6a1454bf151c760c2369551701cf7e46d2134ffa06e7750696bf1d777347979b'
            '5571610e4cee293e8776b33ec225ca24af05197cfd7c3ebd3c2e8d830efd55b0'
            'f032810ea128d4cf9377d144cded32cbf1a2ed18087403fe706a1f9707fd0d7f'
            '6f4e716d6e3585cb60b21c64ea75eebdc537238e5a5a065c21ae4ac05e7c3a53')

package() {
    install -Dm755 "${srcdir}/halium11-post-install" -t "${pkgdir}/usr/bin/"
    install -Dm644 "${srcdir}/halium11-post-install.service" -t "${pkgdir}/usr/lib/systemd/system/"
    install -Dm644 "${srcdir}/android.conf" -t "${pkgdir}/usr/lib/sysusers.d/"
    install -Dm644 "${srcdir}/ril_subscription.conf" "${pkgdir}/etc/ofono/ril_subscription.conf"
    install -Dm644 "${srcdir}/90_manjaro.gschema.override" -t "${pkgdir}/usr/share/glib-2.0/schemas/"
}
