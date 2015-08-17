# Contributor: Anonymous
# Generator  : CPANPLUS::Dist::Arch 1.23

pkgname='perl-mime-base64-alt'
pkgver='3.13'
pkgrel='2'
pkgdesc="The RFC 2045 encodings; base64 and quoted-printable"
arch=('i686' 'x86_64')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl>=5.006')
makedepends=()
url='http://search.cpan.org/dist/MIME-Base64'
source=('http://search.cpan.org/CPAN/authors/id/G/GA/GAAS/MIME-Base64-3.13.tar.gz')
md5sums=('a555d807b328aee871c686a6b6bae5b4')
sha512sums=('0d43a94d7b2b1112d47be3ead197603302185091f8b7ab7f50dac74724f1b53dc8a21ec0be257ba13081d872734fc7ec137cb4380f17d216c1f047febe5e993c')
_distdir="${srcdir}/MIME-Base64-3.13"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
