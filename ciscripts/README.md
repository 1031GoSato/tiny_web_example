## JenkinsCI

$B%7%'%k%8%g%V$K2<5-FbMF$rDj5A$7$F2<$5$$!#(B
$B$J$*!"(B`APP_IMAGE_ID`$B$H(B`DB_IMAGE_ID`$B$K$O!"$=$l$>$l?75,:n@.$7$?%^%7%s%$%a!<%8(BID$B$GCV$-49$($F2<$5$$!#(B

```
#!/bin/bash
#
#
set -e
set -o pipefail
set -u
set -x

cd ciscripts
ls -l

ipaddr="$(< /metadata/meta-data/local-ipv4)"

APP_IMAGE_ID="wmi-********" \
 DB_IMAGE_ID="wmi-********" \
    YUM_HOST="${ipaddr}" \
 ./web3layers-ci.sh
```
