# Maintainer: Loren Copeland <thisisquitealongname@gmail.com>

pkgname=python2-sqlalchemy-0.5
pkgver=0.5.8
pkgrel=1
pkgdesc="Python SQL toolkit and Object Relational Mapper"
arch=('any')
url="http://www.sqlalchemy.org"
license=('MIT')
depends=('python2' 'setuptools')
conflicts=('python-sqlalchemy' 'python2-sqlalchemy')
provides=('python-sqlalchemy' 'python2-sqlalchemy')
source=(http://downloads.sourceforge.net/sourceforge/sqlalchemy/SQLAlchemy-$pkgver.tar.gz)
md5sums=('716f6666b691d8a0ebafece9a3da31cd')

build()
{
  cd ${srcdir}/SQLAlchemy-${pkgver}
  python2 setup.py install --root=${pkgdir} || return 1

  install -D -m644 LICENSE \
	${pkgdir}/usr/share/licenses/${pkgname}/LICENSE || return 1
}
