# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Alireza Savand <alireza.savand@gmail.com>

_gemname=pundit
pkgname=ruby-$_gemname
pkgver=0.2.3
pkgrel=1
pkgdesc='OO authorization for Rails'
arch=(any)
url='https://github.com/elabs/pundit'
license=(MIT)
depends=(ruby ruby-activesupport)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('127e1707c6f6c8113c27594cbf8f724d37de6c59')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/LICENSE.txt" "$pkgdir/usr/share/licenses/$pkgname/LICENSE.txt"
}
