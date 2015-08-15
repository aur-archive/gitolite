# Submitter: Bartłomiej Piotrowski <nospam@bpiotrowski.pl>
# Maintainer: Jon Eyolfson <jon@eyolfson.com>
pkgname=gitolite
pkgver=3.6.3
pkgrel=1
pkgdesc='An access control layer on top of git'
url="https://github.com/sitaramc/gitolite"
arch=('any')
license=('GPL2')
depends=('git' 'perl')
conflicts=('gitolite-git' 'gitolite-g2-git' 'gitolite-g3-git')
source=("https://github.com/sitaramc/${pkgname}/archive/v${pkgver}.tar.gz")
sha256sums=('9b20eb6ae84358c5f063b02da64e49bef4605c9bfc7fb3700a2766dba58b9d99')

build() {
    cd "${srcdir}/${pkgname}-${pkgver}/src"
    echo "v${pkgver}" > VERSION
}

package() {
    install -d "${pkgdir}/usr/lib/gitolite"
    cp -a "${srcdir}/${pkgname}-${pkgver}/src/"* "${pkgdir}/usr/lib/gitolite"
    install -d "${pkgdir}/usr/bin"
    ln -s "/usr/lib/gitolite/gitolite" "${pkgdir}/usr/bin/"
}
