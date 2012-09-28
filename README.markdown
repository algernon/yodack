Ye Olde Debian Archive Control Kit
==================================
  "The only *Kit that does not suck"

Concieved under the influence of black tea, born on a train 4am in the
morning, Y.O.D.A.C.K. is not your average tool. It has a distinct
personality, and its purpose is to teach, not to do your job. At
least, that is what it likes to think - how that works in practice, we
shall see.

But alas, since the story teller who was there when Yodack was born is
terribly tired, documentation - for now - will have to wait.

Let it suffice, that the following command does the right thing:

```sh
$ yodack ftp-master dm algernon@madhouse allow dh-exec yodack deny eglibc
```

Or, if one prefers writing verbose, overly polite commands:

```sh
$ yodack on ftp-master.debian.org, for dm algernon@madhouse, \
         please allow uploading dh-exec, yodack, \
         but disallow uploading eglibc.
```
