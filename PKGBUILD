# Maintainer: Ryan Swart <ryanswrt@gmail.com>
pkgname=bibisco
_pkgname=Bibisco
pkgver=1.4.0
pkgrel=1
pkgdesc="Simple novel writing software"
arch=('x86_64')
url="http://www.bibisco.com/"
license=('GPL')
groups=()
depends=("unzip")
makedepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install="$pkgname.install"
changelog=
source=("https://github.com/andreafeccomandi/bibisco/releases/download/v$pkgver/$pkgname-linux64-v$pkgver.tar.gz"
"$_pkgname.desktop"
"$pkgname.install"
)
noextract=()
md5sums=('69db1b3084d2537b1d41bf1c509d2ef5'
         '6408d90893bbc3485d415f99a44d879a'
         '734694d5fa3e132f9af847adc4fd7c1c')


package() {
  cd "$srcdir"
  install -Dm 644 "$srcdir/$_pkgname.desktop" "$pkgdir/usr/share/applications/$pkgname.desktop" 
  cp -ra "$srcdir/$pkgname" "$pkgdir/usr/share/$pkgname"
  chmod -R 0777 "$pkgdir/usr/share/$pkgname/db"
  #chmod -r 777 "$pkgdir/usr/share/$pkgname/config"
  mkdir "$pkgdir/usr/share/$pkgname/log"
  chmod -R 0777 "$pkgdir/usr/share/$pkgname/log"
  mkdir "$pkgdir/usr/share/$pkgname/xulrunner/appdata"
  chmod -R 0777 "$pkgdir/usr/share/$pkgname/xulrunner/appdata"
  unzip "$srcdir/$pkgname/plugins/${pkgname}_$pkgver.jar" "icons/branding/logo128x128.png"
  install -Dm 644 "$srcdir/icons/branding/logo128x128.png" "${pkgdir}/usr/share/icons/128x128/apps/${pkgname}.png"
} 
