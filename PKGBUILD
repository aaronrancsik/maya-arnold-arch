# Maintainer: William Tang <galaxyking0419@gmail.com>

pkgname=maya-arnold
pkgver=7.0.0
pkgrel=1
pkgdesc='Autodesk Maya Arnold Renderer Plugin'
arch=('x86_64')
url='https://www.arnoldrenderer.com/arnold/arnold-for-maya/'
license=('custom')
depends=('maya>=2022.0' 'maya<2023.0' 'smbclient' 'tbb')
optdepends=('maya-usd: Universal Scene Discription Support')

DLAGENTS+=('manual::/usr/bin/echo \ \ Note: Please download the package manually from the official website')
source=('manual://package.zip')
sha256sums=('d78dda37f92d11ea63dc6df372ac621c3d9435a70c15621c10e92e26a0617202')

options=(!strip)

prepare() {
    sed -i 's|/home/go-agent/pipelines/MtoA-RC/material/mtoa/MTOA_DEPLOY|/usr/autodesk/maya2022/plug-ins/arnold|g' mtoa.mod
}

package() {
    unlink package.zip
    mkdir -p $pkgdir/usr/autodesk/maya2022/{modules,plug-ins/arnold}

    mv mtoa.mod $pkgdir/usr/autodesk/maya2022/modules/
    mv * $pkgdir/usr/autodesk/maya2022/plug-ins/arnold/
}
