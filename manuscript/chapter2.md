# Building the docs

The page describes how to build the latest documentation of Akka HTTP from the sources.

It assumes that you're on **MacOS X Yosemite** and have [sbt](http://www.scala-sbt.org/) installed.

* Install [The MacTeX-2014 Distribution](http://www.tug.org/mactex/).
* Add `/usr/local/texlive/2014/bin/x86_64-darwin` to `PATH`
* Clone [Akka sources](https://github.com/akka/akka) and switch to `release-2.3-dev` branch

		$ git clone https://github.com/akka/akka.git
		$ cd akka
		$ git checkout release-2.3-dev

* Execute `makeSite` task of sbt

		➜ akka git:(release-2.3-dev) ✗ sbt clean makeSite
		[info] Loading global plugins from /Users/jacek/.sbt/0.13/plugins
		[info] Updating {file:/Users/jacek/.sbt/0.13/plugins/}global-plugins...
		[info] Resolving org.fusesource.jansi#jansi;1.4 ...
		[info] Done updating.
		[info] Loading project definition from /Users/jacek/dev/oss/akka/project
		[info] Set current project to akka (in build file:/Users/jacek/dev/oss/akka/)
		[success] Total time: 2 s, completed Feb 2, 2015 9:10:48 PM
		[info] Installing Sphinx custom package 'pygments'...
		[info] Sphinx custom package installed: /Users/jacek/dev/oss/akka/akka-docs-dev/target/sphinx/packages/pygments
		[info] Preprocessing directory /Users/jacek/dev/oss/akka/akka-docs-dev/rst...
		[info] Directory preprocessed: /Users/jacek/dev/oss/akka/akka-docs-dev/rst_preprocessed
		[info] Generating Sphinx latex documentation...
		...
		[info] Sphinx epub documentation generated: /Users/jacek/dev/oss/akka/akka-docs-dev/target/sphinx/epub
		[info] Sphinx documentation generated: /Users/jacek/dev/oss/akka/akka-docs-dev/target/sphinx/docs
		[success] Total time: 34 s, completed Feb 2, 2015 9:11:22 PM

* Open `akka-docs-dev/target/sphinx/docs/index.html`
