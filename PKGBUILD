# $Id$
# Maintainer: BlackEagle <ike DOT devolder AT gmail DOT com>

pkgname=container-bash
pkgver=3
pkgrel=1
pkgdesc="busybox linked bash for containers"
arch=('any')
url="http://herecura.eu/"
license=('GPL')
depends=('busybox')
provides=('sh' 'bash')

package() {
    install -dm755 "$pkgdir/usr/bin"
    ln -s busybox "$pkgdir/usr/bin/sh"
    printf "#!/bin/sh\n/bin/sh \"$@\"" > "$pkgdir/usr/bin/bash"
    chmod +x "$pkgdir/usr/bin/bash"
}
