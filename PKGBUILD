# Maintainer: Sial <NAME at cpan dot org>

_gitname='powerline-fonts'
pkgname='otf-source-code-pro-powerline-git'
pkgver=1.017
pkgrel=3
pkgdesc='Pre-patched and adjusted version for usage with the new Powerline plugin'
arch=('any')
url="https://github.com/Lokaltog/${_gitname}/tree/master/SourceCodePro"
license=('custom:OFL')
depends=('fontconfig' 'xorg-font-utils')
makedepends=('git')
optdepends=('python-powerline-git: The ultimate statusline/prompt utility'
	'python2-powerline-git: The ultimate statusline/prompt utility')
install=${pkgname}.install
source=("git+https://github.com/Lokaltog/${_gitname}")
md5sums=('SKIP')

pkgver() {
	cd "${srcdir}/${_gitname}/SourceCodePro"
 cat README.rst | grep '^:Version:' | sed -n 's/^.*: \(.*[0-9]\).*$/\1/p'
}

package() {
	cd "${srcdir}/${_gitname}/SourceCodePro"
	
	install -d "${pkgdir}/usr/share/fonts/OTF"
	install -m644 *.otf "${pkgdir}/usr/share/fonts/OTF/"
	install -Dm644 LICENSE.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE.txt"
}
