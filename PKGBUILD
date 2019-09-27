# Maintainer: Maximilian Luz <luzmaximilian@gmail.com>

pkgname="linux-surface-secureboot-mok"
pkgver=1.0.0
pkgrel=1
pkgdesc='Secure-boot machine owner key for linux-surface kernels'
url='https://github.com/qzed/linux-surface'
license=('MIT')
arch=('any')
depends=('mokutil-git')
install="${pkgname}.install"

_commit="f01b6e6ad3cfb495964ebab88ed0be8ced53d9dd"
source=(
    "https://raw.githubusercontent.com/qzed/linux-surface/${_commit}/keys/MOK.cer"
)

sha256sums=('f999c276132af368b25f046e15a4e5d96f0f0924ec892e3328cec04bc2fad16b')


package() {
    install -D -m400 "${srcdir}/MOK.cer" "${pkgdir}/usr/share/linux-surface-secureboot/qzed.mok"
}
