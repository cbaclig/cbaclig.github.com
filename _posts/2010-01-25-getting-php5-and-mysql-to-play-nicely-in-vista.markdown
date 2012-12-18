---
layout: post
title: !binary |-
  R2V0dGluZyBQSFA1IGFuZCBNeVNRTCB0byBwbGF5IG5pY2VseSBpbiBWaXN0
  YQ==
wordpress_id: 5
wordpress_url: !binary |-
  aHR0cDovL3d3dy5jaHJpc2JhY2xpZy5jb20vP3A9NQ==
date: 2010-01-25 01:21:00.000000000 -08:00
---
I've been struggling with installing CakePHP on my local machine for the past few days, and just solved this extremely annoying issue.  I thought I'd share since it took me the better part of 4 hours to figure out what the hell was going on.<br /><br />I installed CakePHP according to the installation instructions on the CakePHP site (which are VERY helpful) but for some reason CakePHP could not connect to my local MySQL Database.  No errors were being thrown.  The connection was just timing out.<br /><br />I double checked all the configurations in app/config/database.php and settings and everything seemed to be in order.  After sprinkling debug comments throughout the code, I determined that  the problem was in CORE/cake/libs/model/datasources/dbo/dbo_mysql.php in the connect function.<br /><br />As it turns out, it wasn't me, it was Vista...<br /><br />The second comment on the official doc for mysql_connect holds the answer (http://php.net/manual/en/function.mysql-connect.php)<br /><br /><br />I haven't been able to figure out why (yet,) but apparently having the<br /><code><br />    ::1     localhost</code><br />entry in your Windows host file makes mysql_connect timeout and never connect to the database.<br /><br />Lame.<br /><br />After spending the past couple days trying to get cakePHP up and running on my own machine, I might post a how-to guide once I've finally finished.
