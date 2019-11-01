pkgname=brscan4-skey
pkgver=0.2.4_1
pkgrel=1
pkg="brscan-skey-${pkgver/_/-}.x86_64.rpm"
pkgdesc="Brother brscan4 skey"
url="http://support.brother.com/g/s/id/linux/en"
license=('GPL' 'custom:Brother')
depends=('brscan4')
arch=('x86_64')
install=brscan4-skey.install
backup=(opt/brother/scanner/brscan-skey/brscan-skey-0.2.4-0.cfg)
source=("http://www.brother.com/pub/bsc/linux/dlf/$pkg" "http://www.brother.com/agreement/English_sane/agree.html")
md5sums=('9ad29a0ef9f8f4d6f742fb4293ee08a6' 'ccffb9a6f6d436b21be25b0241068981')

package() {
  mv $srcdir/opt/brother/scanner/brscan-skey/brscan-skey-0.2.4-1.sh $srcdir/opt/brother/scanner/brscan-skey/brscan-skey-0.2.4-0.sh
  cp -r $srcdir/opt $pkgdir
  mkdir -p $pkgdir/usr/bin
  ln -s /opt/brother/scanner/brscan-skey/brscan-skey $pkgdir/usr/bin/
  install -D -m644 $srcdir/agree.html $pkgdir/usr/share/licenses/$pkgname/LICENSE.html
}
