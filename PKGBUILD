# Maintainer: DarkXero <info@techxero.com>

pkgname=grub-hooks
pkgdesc="Fixes, additions and enhancements to grub and os-prober."
pkgver=1.0.0
arch=('any')
license=('GPL')
depends=(grub lsb-release)
optdepends=(os-prober)

url=https://github.com/xerolinux/$pkgname
_url="https://raw.githubusercontent.com/xerolinux/$pkgname/main"

source=(
  $_url/install-grub
  $_url/grub-btrfs.hook
  $_url/grub-install.hook
  $_url/grub-kernel.hook
  $_url/grub-microcode.hook
  $_url/grub-mkconfig.hook
)

package() {
  cd $srcdir

  install -d $pkgdir/usr/share/libalpm/hooks
  install -Dm644 install-grub          $pkgdir/usr/bin/install-grub
  install -Dm644 grub-btrfs.hook       $pkgdir/usr/share/libalpm/hooks/grub-btrfs.hook
  install -Dm644 grub-install.hook     $pkgdir/usr/share/libalpm/hooks/grub-install.hook
  install -Dm644 grub-kernel.hook      $pkgdir/usr/share/libalpm/hooks/grub-kernel.hook
  install -Dm644 grub-microcode.hook   $pkgdir/usr/share/libalpm/hooks/grub-microcode.hook
  install -Dm644 grub-mkconfig.hook    $pkgdir/usr/share/libalpm/hooks/grub-mkconfig.hook

}
