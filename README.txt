clojure-archetype

by Stuart Sierra


This is a Maven 2 archetype for Clojure projects.  It will generate a
new project pre-configured to use Clojure and the Clojure Maven
plugin.


INSTALLATION AND USAGE

To install:

   git clone git://github.com/stuartsierra/clojure-archetype.git
   cd clojure-archetype
   mvn install

To use (all one line):

   mvn archetype:create \
     -DgroupId=your.group.name \
     -DartifactId=your-new-project-name \
     -DarchetypeGroupId=com.stuartsierra \
     -DarchetypeArtifactId=clojure-archetype \
     -DarchetypeVersion=1.0-SNAPSHOT


SOURCES

The generated project has source code in src/main/clojure and test
code in src/test/clojure.  The example file src/main/clojure/app.clj
demonstrates how to create a "main" Java class that can be executed at
the command line.


GOALS

In addition to the standard Maven goals, you have several
Clojure-specific goals available through clojure-maven-plugin:

 * clojure:compile will ahead-of-time compile your Clojure source code
   to Java .class files

 * clojure:test will run the script at src/scripts/runtests.clj

 * clojure:repl will run a Clojure REPL

 * clojure:swank will run a SWANK server for connecting to Emacs SLIME
   (requires SWANK as a dependency)

The clojure:compile goal is bound to the Maven "compile" lifecycle,
and the clojure:test goal is bound to the Maven "test" lifecycle.

To see more available goals, run (one line):

  mvn help:describe -DgroupId=com.theoryinpractise \
                    -DartifactId=clojure-maven-plugin 


DEPENDENCIES

By default, the generated project has dependencies on Clojure 1.0.
For dependencies on other Clojure versions, or on clojure-contrib,
uncomment the indicated sections in the generated pom.xml.



LICENSE

Copyright (c) 2009 Stuart Sierra. All rights reserved.  The use and
distribution terms for this software are covered by the Eclipse Public
License 1.0 (http://opensource.org/licenses/eclipse-1.0.php) which can
be found in the file epl-v10.html at the root of this distribution.
By using this software in any fashion, you are agreeing to be bound by
the terms of this license.  You must not remove this notice, or any
other, from this software.
