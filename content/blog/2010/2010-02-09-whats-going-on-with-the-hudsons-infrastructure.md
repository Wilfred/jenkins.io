---
:layout: post
:title: What's going on with the Hudson's infrastructure
:nodeid: 149
:created: 1265724000
:tags:
- development
- core
- feedback
- just for fun
:author: rtyler
---
A lot has changed in the Hudson development and distribution infrastructure since last summer - we've made a distinct effort to get the quality of our infrastructure to match the quality of Hudson itself. We owe a special thanks to the wonderful folks over at <a href="http://atlassian.com/">Atlassian</a> - we're taking advantage of their generous <a href="http://www.atlassian.com/opensource/">open source license</a> for our bug tracking (<a href="http://www.atlassian.com/software/jira/">JIRA</a>), wiki (<a href="http://www.atlassian.com/software/confluence/">Confluence<a>), and source repository browser (<a href="http://www.atlassian.com/software/fisheye/">FishEye</a>). Obviously, there's a lot more we can improve going forward - I'll have another post up soon, looking at some of the ideas we're kicking around. But for now, take a look at what we've already done, below the fold.
<!--break-->
<li>The Hudson war and plugin downloads have all moved off of the unreliable java.net to our own [hudson-ci.org](http://hudson-ci.org) with the downloads being powered by the same system used for distributing Java, OpenSolaris, and NetBeans. Downloading Hudson and/or plugins is now easier and more reliable.</li>
<li>We've moved issue tracking from java.net's system to our own JIRA instance, at [issues.hudson-ci.org](http://issues.hudson-ci.org). As with moving downloads off java.net, we've made reporting and browsing Hudson's issues much faster, easier and more reliable, while still using the same authentication on the back-end as our Subversion and Maven repositories. We're still working out some kinks in the system but since we're running our own issue tracker now, rather than using one we didn't have control over, we've got the flexibility we need to adapt our tools to best serve the developer and user communities.</li>
<li>Speaking of tools we now run ourselves, we've put up our own FishEye instance at [fisheye.hudson-ci.org](http://fisheye.hudson-ci.org) - until that was in place, we'd been relying on Atlassian's public FishEye instance, which has many other open source projects' repositories available. Getting our own server up means we don't have to bug the generous folks over at Atlassian every time the java.net SVN server confuses FishEye into failing to update. It also opens the door for us to use <a href="http://www.atlassian.com/software/crucible/">Crucible</a> for code review in the future.</li>
<li>Hudson's moved onto Twitter more and more over the last 6-9 months - we've got the always fabulous <a href="http://twitter.com/hudsonci">@hudsonci</a>, tweeting new releases, Hudson-related tweets, and more, as well as the <a  class="apturenoenhance" href="http://twitter.com/search?q=%23hudsonci">#hudsonci</a> hashtag.
<li>This may not strictly be infrastructure but it's worth mentioning that we've now got native packages and distribution for Hudson for <a href="http://hudson-ci.org/debian/">Ubuntu/Debian</a>, <a href="http://hudson-ci.org/redhat/">Red Hat/Fedora/CentOS</a>, <a href="http://hudson-ci.org/opensuse/">openSUSE</a>, <a href="http://pkg.hudson-ci.org/">OpenSolaris/Nevada</a>, and <a href="http://www.freshports.org/www/hudson/">FreeBSD</a>.</li>
<li>This is all in addition to key parts of our infrastructure that haven't changed: our <a href="http://wiki.hudson-ci.org/display/HUDSON/Home">official wiki</a>, our <a href="http://wiki.hudson-ci.org/display/HUDSON/Mailing+List">user and developer mailing lists</a>, our <a href="https://hudson.dev.java.net/svn/hudson/trunk/hudson/">Subversion repository</a> (and a <a href="http://github.com/kohsuke/hudson/">Git mirror</a> on GitHub) and our <a href="http://wiki.hudson-ci.org/display/HUDSON/IRC+Channel">IRC channel over on Freenode</a>.</li>

Oh, and I hear there's a blog now too.

----
**Editor's Note:** Andrew Bayer (`abayer`) has been a contributor to Hudson since early 2009, contributing to the ClearCase plugin, Hudson's core and a small number of other plugins. Andrew also helps Kohsuke with a lot of Hudson's project infrastructure, most notably the migration from Bugzilla on Java.net to JIRA running at [issues.hudson-ci.org](http://issues.hudson-ci.org).
