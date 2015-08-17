# Contributor: Timo Lindemann <coffeeprocessor@gmail.com> 
# Adapted from: Benjamin Hedrich <phpogo@gmx.net> (plone-beta package)
# Category: network

pkgname=plone4
pkgver=4.1.4
pkgrel=2
pkgdesc="A powerful, flexible Content Management solution that is easy to install, use and extend"
arch=('i686' 'x86_64')
license=('GPL2')
url="http://www.plone.org/"
depends=('gcc' 'patch')
conflicts=('plone')
provides=('plone')

install=plone.install

backup=('opt/Plone/Plone/zinstance/filestorage/Data.fs' 
        'opt/Plone/Plone/zinstance/buildout.cfg')

source=(http://launchpad.net/plone/4.1/$pkgver/+download/Plone-$pkgver-UnifiedInstaller.tgz
        plone.daemon
        plone.install)
				  
md5sums=('597cd780cb4ac1575ede6b995b552a77'
         'dbd30acc21b00e8c3c2b47658735163b'
         '1f63b3bdad2d394ec80cfeb19db32441')
build() {

    mkdir -p $pkgdir/opt/Plone/
    mkdir -p $pkgdir/etc/rc.d/

    cp $srcdir/Plone-$pkgver-UnifiedInstaller $pkgdir/opt/Plone/ -R
    cp $srcdir/plone.daemon $pkgdir/etc/rc.d/plone
    
}
