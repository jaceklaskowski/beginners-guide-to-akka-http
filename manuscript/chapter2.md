# Building the docs

The page describes how to build the latest documentation of Akka HTTP from the sources.

It assumes that you're on **MacOS X Yosemite** and have [sbt](http://www.scala-sbt.org/) installed.

* Install [The MacTeX-2014 Distribution](http://www.tug.org/mactex/).
* Add `/usr/local/texlive/2014/bin/x86_64-darwin` to `PATH`
* Clone [Akka sources](https://github.com/akka/akka) and switch to `release-2.3-dev` branch

		$ git clone https://github.com/akka/akka.git
		$ cd akka
		$ git checkout release-2.3-dev

* Execute `sphinx:generateHtml` task

		➜  akka git:(release-2.3-dev) ✗ sbt clean sphinx:generateHtml
		[info] Loading global plugins from /Users/jacek/.sbt/0.13/plugins
		[info] Loading project definition from /Users/jacek/dev/oss/akka/project
		[info] Set current project to akka (in build file:/Users/jacek/dev/oss/akka/)
		[info] Preprocessing directory /Users/jacek/dev/oss/akka/akka-docs/rst...
		[info] Directory preprocessed: /Users/jacek/dev/oss/akka/akka-docs/rst_preprocessed
		[info] Preprocessing directory /Users/jacek/dev/oss/akka/akka-contrib/docs...
		[info] Directory preprocessed: /Users/jacek/dev/oss/akka/akka-docs/rst_preprocessed/contrib
		[info] Generating Sphinx html (online) documentation...
		...
		[info] Sphinx html (online) documentation generated: /Users/jacek/dev/oss/akka/akka-stream-and-http/target/sphinx/html
		[info] Generating Sphinx html (online) documentation...
		[info] Sphinx html (online) documentation generated: /Users/jacek/dev/oss/akka/target/sphinx/html
		[success] Total time: 19 s, completed Feb 2, 2015 11:36:07 PM

* Open `akka-stream-and-http/target/sphinx/html/index.html`
