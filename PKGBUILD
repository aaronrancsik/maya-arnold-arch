# Maintainer: William Tang <galaxyking0419@gmail.com>

pkgname=maya-arnold
pkgver=4.2.3
pkgrel=1
pkgdesc='Autodesk Maya Arnold Renderer Plugin'
arch=('x86_64')
url='https://www.arnoldrenderer.com/arnold/arnold-for-maya/'
license=('custom')
depends=('maya>=2022.0' 'maya<2023.0' 'smbclient' 'tbb')
optdepends=('maya-usd: Universal Scene Discription Support')

DLAGENTS+=('manual::/usr/bin/echo \ \ Note: Please download the package manually from the official website')
source=('manual://package.zip')
sha256sums=('73cd879af2db55f424fce7ce80f958c026acb45a6be081818f4182bd79d12e2a')

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
