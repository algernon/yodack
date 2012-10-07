The Y.O.D.A.C.K. test suite
===========================

The `yodack` test suite is built upon [shunit2][1], one needs to have
that installed, along with every other dependency `yodack` itself has.

By default, the test suite will set up an appropriate environment,
including two GPG keys generated on the fly (one to sign with, another
to use as a fake debian maintainer key). This is fairly costy, so
there's a loophole: if one sets the `YODACK_GNUPGHOME` variable, then
the tests will skip generating keys, and use that value instead. The
directory there must already contain the generated keys, which can
easily be placed there by following these steps:

```sh
$ export YODACK_GNUPGHOME=/tmp/yodack.tmp.gpg
$ export GNUPGHOME=$YODACK_GNUPGHOME
$ install -d -m 0700 $GNUPGHOME
$ gpg --quiet --batch --gen-key data/gpg.batch
```

 [1]: http://code.google.com/p/shunit2/
 
