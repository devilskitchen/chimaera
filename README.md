Chimaera Framework
==================

My standard files for building websites, incorporating HTML5 boilerplate, and my own LESS starting framework.

Do we need another framework?
-----------------------------

Well, that's up to you. I just wanted somewhere to put my own constantly re-used files, rather than my file system or a rather clunky Subversion respository.

Why not just use _[insert framework of your choice here]_?
-----------------------------------

Once again, feel free to do so.

Personally, I feel that some frameworks are constricting: it's not simply that they can lead to an inclination to build sites that look similar, it's that some frameworks embrace a number of concepts that I think are wrong for web design.

### The web is not print

One of the unwelcome design methodologies that print designers have brought to the web is this whole concept of over-riding _columns_, a discipline that is fine when you are actually dealing with multi-column print publications.

The trouble is that this method was designed for just that&mdash;multi-columned print publications _where you have a defined page size_. On the web, you have no defined page size, and talking about fixed columns is just as inappropriate as trying to put stuff _"above the fold"_.

### Media queries are not universal

Some frameworks try to compensate for a lack of fluidity by using <code>@media queries</code> and a large number of break-points. Not only does this increase the workload (since you need to accommodate multiple view states) but it also runs into problems with older browsers.

I come from a background of designing for large corporate, governmental and quasi-governmental organisations&mdash;many of whom are, alas, still using IE7 (and some still use IE6). Even where upgrades are happening, many of these organisations are only upgrading to IE8 (where XP is often the limiting factor).

For all that <code>respond.js</code>, and similar polyfills, do a good job of trying to backfill capabilities, we just have to accept that many of our customers are not going to get the best experience at work.

And whilst we would all love to imagine that everyone at least uses a better browser at home, I can tell you&mdash;from first-hand experience&mdash;that this is simply not the case.

### Design in a fluid way from the start


The web is a fluid medium, with many different ways of viewing websites and web applications: dealing in fixed units just doesn't make any sense. And I include, by the way, pixel measurements in this.

As far as I am concerned, pixel measurements are only appropriate when dealing with elements that are inherently pixel-constrained, i.e. bitmap images. So, if you are using a 16px x 16px bitmap image as an icon, and you want to bump the text in, then using <code>padding-left: 20px;</code> is fine.

In almost any other situation, you are just going to run into trouble.

### So, what units should we use?

Any measurements that are based on the size of text, essentially. The main structural language of the web is Hyper _Text_ Markup Language (HTML), and it is still the amount of text that mostly defines the size of a web page (flexbox, etc. notwithstanding).

Further, when designing Accessible sites, you must allow users to increase the text size of pages, and so sizing everything by text makes sense.

All of which is a long-winded way of saying that we should use <code>em</code>s, <code>rem</code>s and other proportional units. And <code>vh</code> and <code>vw</code> are shaping up to be particularly exciting.

### But this framework is a bit thin

Sure, but I am going to add to it substantially.