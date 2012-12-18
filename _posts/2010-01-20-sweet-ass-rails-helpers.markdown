---
layout: post
title: !binary |-
  U3dlZXQgQXNzIFJhaWxzIEhlbHBlcnM=
wordpress_id: 4
wordpress_url: !binary |-
  aHR0cDovL3d3dy5jaHJpc2JhY2xpZy5jb20vP3A9NA==
date: 2010-01-20 23:01:00.000000000 -08:00
---
These are probably the most useful Rails helpers I've ever come across.  I stumbled upon them today trying to figure out why one would pass a binding to the concat method.  As it turns out, that <a href="http://74.125.155.132/search?q=cache:cp4abCmPsh0J:www.justinball.com/2008/12/20/the-binding-argument-of-concat-is-no-longer-needed/+concat+binding&amp;cd=2&amp;hl=en&amp;ct=clnk&amp;gl=us&amp;client=firefox-a">method is outdated</a>.<br /><br />Good to know...<br /><br />Luckily, it led me to these little gems.  Some highlights include:<br /><ul><li>pluralize - no explanation needed</li><li>auto_link - turns all URL in a block of text into links</li><li>word_wrap - inserts line breaks so that no line is greater than a given character length</li><li>truncate - link word_wrap, but once the limit is reached, ellipsis are used</li></ul>All of which can be customized to fit your own needs.<br /><br />I &lt;3 Rails.<br /><br /><a href="http://api.rubyonrails.org/classes/ActionView/Helpers/TextHelper.html#M001752">See the Rails API docs for more info.</a>
