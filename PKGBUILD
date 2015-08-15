# Maintainer: archtux <antonio dot arias99999 at gmail dot com>

pkgname=facebook-for-linux
pkgver=6.0
pkgrel=3
pkgdesc="Desktop application to connect to Facebook, Twitter and Google+"
arch=('i686' 'x86_64')
url="https://launchpad.net/facebookwindoof"
license=('GPL3')
depends=('qt5-webkit')
optdepends=('amarok' 'banshee' 'rhythmbox')

# Uncomment source and md5sum for choosing a theme(green, gold or blue)
# For red and pink themes uncomment also line 31 'othertheme'

source=(
        https://launchpad.net/facebookwindoof/trunk/facebookforlinux/+download/fb4linux6-green-src.tar.gz
#        https://launchpad.net/facebookwindoof/trunk/facebookforlinux/+download/fb4linux6-Gold-src.tar.gz
#        https://launchpad.net/facebookwindoof/trunk/facebookforlinux/+download/fb4linux6-blue-src.tar.gz
#        https://launchpad.net/facebookwindoof/trunk/facebookforlinux/+download/fb4linux6-RED-SRC.tar.gz
#        https://launchpad.net/facebookwindoof/trunk/facebookforlinux/+download/fb4linux6-pink-src.tar.gz
        FB4Linux.desktop)
md5sums=(
         'c5aeb30d008f79e0693a8e4d3fd50994'
#         '388655ca320bb8bd4960a01280e97323'
#         '07fcef4c3aae386e2e424f156b5a2b0e'
#         'e8d4de1ffe8b9428ac75eb17cc16ea65'
#         '9b11cedbd8f3999e01c7e3d7ebc2b6d4'
         '0c037d08e4b31b76747a3be345077507')

#othertheme="fb4linux"
         
prepare() {
  cd $srcdir/$othertheme
  qmake-qt5
}

build() {
  cd $srcdir/$othertheme
  make
}

package(){
  cd $srcdir/$othertheme
  
  # Binary
  install -Dm755 fb4linux $pkgdir/usr/bin/fb4linux
  
  # Desktop icon
  install -Dm644 ./FB4Linux.desktop $pkgdir/usr/share/applications/FB4Linux.desktop
  install -Dm644 res/logo/facebook-256x256.png $pkgdir/usr/share/pixmaps/FB4Linux.png
}