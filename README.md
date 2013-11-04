pre-info
========

Files containing pre info for nZEDbetter.

datafiles is for the backfill_predb script. Be ssure that mysql has read/write access to the web root. Be sure that your mysql user has the priviliges need to import.

For manual import, you can enter the following two lines from a prompt.  These files have been modified to allow you to import them at any time. The ID column has been nulled so you don't get primary key errors.

```
for a in `la -1`; do echo $a; unzip $a; done;
```

If you do not want to enter your password 14 times, you can modify the -p parameter to inlcude your password.  Be sure that there is NO space between the -p and your password (example -pPa$$w0rd)
```
for a in `la -1 *.sql`; do echo $a;  mysql -u root -p nzedbetter < $a; done;
```
