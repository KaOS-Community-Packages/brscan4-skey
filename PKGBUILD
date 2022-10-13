pkgname=brscan4-skey
pkgver=0.3.1_2
pkgrel=0
pkg="brscan-skey-${pkgver/_/-}.x86_64.rpm"
pkgdesc="Brother brscan4 skey"
url="https://support.brother.com/g/b/downloadlist.aspx?c=fr&lang=fr&prod=dcp7065dn_all&os=127&flang=English"
license=('GPL' 'custom:Brother')
depends=('brscan4')
arch=('x86_64')
install=brscan4-skey.install
backup=(opt/brother/scanner/brscan-skey/brscan-skey-0.3.1-2.cfg)
source=("https://download.brother.com/welcome/dlf006650/$pkg" "https://support.brother.com/g/s/agreement/English_lpr/agree.html")
md5sums=('88523ce704a5d746c0570610237a2d85' '5a4a3172f6278922062aa6e1f43b0d92')

package() {
  cp -r $srcdir/opt $pkgdir
  mkdir -p $pkgdir/usr/bin
  ln -s /opt/brother/scanner/brscan-skey/brscan-skey $pkgdir/usr/bin/
  install -D -m644 $srcdir/agree.html $pkgdir/usr/share/licenses/$pkgname/LICENSE.html
}
