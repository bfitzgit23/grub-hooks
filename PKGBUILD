# Maintainer: StormOS-Dev

pkgname=grub-hooks
pkgdesc="Fixes, additions and enhancements to grub and os-prober."
pkgver=1.0.0
pkgrel=4
arch=('any')
license=('GPL')
depends=(grub lsb-release xero-hooks)
optdepends=(os-prober)
replaces=("grub-tools")

url=https://github.com/bfitzgit23/$pkgname
_url="https://raw.githubusercontent.com/bfitzgit23/$pkgname/main"

source=(
  $_url/install-grub
  $_url/grub-install.hook
  $_url/grub-kernel.hook
  $_url/grub-update.hook
)

package() {
  cd $srcdir

  install -d $pkgdir/usr/share/libalpm/hooks
  install -Dm755 install-grub          $pkgdir/usr/bin/install-grub
  install -Dm644 grub-install.hook     $pkgdir/usr/share/libalpm/hooks/grub-install.hook
  install -Dm644 grub-kernel.hook      $pkgdir/usr/share/libalpm/hooks/grub-kernel.hook
  install -Dm644 grub-update.hook    $pkgdir/usr/share/libalpm/hooks/grub-update.hook

}
