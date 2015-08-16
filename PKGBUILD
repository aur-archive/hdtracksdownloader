# Maintainer: Brandon Hetman <bhetman AT SYMBOL gmail DOT SYMBOL com>
pkgname=hdtracksdownloader
pkgver=20.0.103
pkgrel=1
pkgdesc="Download client for hdtracks.com purchases"
arch=('i686' 'x86_64')
url="http://yabb.jriver.com/interact/index.php?topic=92748.0"
license=('custom:JRiver')
source=("http://files.jriver.com/partners/hdtracks/HDtracksDownloader-$pkgver.deb")
md5sums=('73072ce58c7b62e11ba12d8b7c763fb9')

package() {
	if [[ "${CARCH}" == 'x86_64' ]]; then
		depends+=('lib32-alsa-lib' 'lib32-gtk2')
	fi
	cd "${pkgdir}"
	tar xf "${srcdir}"/data.tar.xz
	mkdir -p usr/share/licenses/"${pkgname}"
	iconv -f UTF-16LE -t UTF-8 usr/lib/HDtracksDownloader/License.txt -o usr/share/licenses/"${pkgname}"/LICENSE
	rm usr/lib/HDtracksDownloader/License.txt
}
