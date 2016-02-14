# kgs-data

A public API to request data from the KGS archives, using S3 to store
already-requested records.

The [KGS](https://www.gokgs.com/) archives
(http://www.gokgs.com/archives.jsp) contain Go games for all KGS
players.  If you wish to do analysis of Go games, KGS provides
archives you can download containing complete games records in SGF
format.  You ccan download each game individually or in bundles by
month.

Sounds great, right?  The problem is that these downloads are
rate-limited to prevent overuse from affecting KGS's performance.
Hence the need for the KGS-Data service - you can download data at any
rate from KGS-Data and if you request data not yet copied to S3 it
will be fetched from KGS at a rate that respects the speed limits that
are in place.

This code and service are not affiliated with KGS in any way.
