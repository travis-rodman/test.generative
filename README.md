clojure.test.generative
========================================

Generative test runner.

Releases and Dependency Information
========================================

Latest stable release: 0.4.0

* [All Released Versions](http://search.maven.org/#search%7Cgav%7C1%7Cg%3A%22org.clojure%22%20AND%20a%3A%22test.generative%22)

* [Development Snapshot Versions](https://oss.sonatype.org/index.html#nexus-search;gav~org.clojure~test.generative~~~)

[Leiningen](https://github.com/technomancy/leiningen) dependency information:

    [org.clojure/test.generative "0.4.0"]

[Maven](http://maven.apache.org/) dependency information:

    <dependency>
      <groupId>org.clojure</groupId>
      <artifactId>test.generative</artifactId>
      <version>0.4.0</version>
    </dependency>


Example Usages
========================================

A defspec consists of a name, a function to be tested, an input spec,
and a validator:

    (defspec integers-closed-over-addition
      (fn [a b] (+' a b))                    ;; input fn
      [^long a ^long b]                     ;; input spec
      (assert (integer? %)))                ;; 0 or more validator forms

To generate test data, see the fns in the generators namespace. Note
that these functions shadow a bunch of clojure.core names.

You can configure the runner with Java system properties:

<table>
  <tr>
    <th>Java Property</th><th>Interpretation</th>
  </tr>
  <tr>
    <td>clojure.test.generative.threads</td><td>Number of concurrent threads</td>
  </tr>
  <tr>
    <td>clojure.test.generative.msec</td><td>Desired test run duration</td>
  </tr>
</table>

Developer Information
========================================

* [GitHub project](https://github.com/clojure/test.generative)

* [Bug Tracker](http://dev.clojure.org/jira/browse/TGEN)

* [Continuous Integration](http://build.clojure.org/job/test.generative/)

* [Compatibility Test Matrix](http://build.clojure.org/job/test.generative-test-matrix/)

Copyright and License
========================================

Copyright (c) 2012 Rich Hickey. All rights reserved.  The use and distribution terms for this software are covered by the Eclipse Public License 1.0 (http://opensource.org/licenses/eclipse-1.0.php) which can be found in the file epl-v10.html at the root of this distribution. By using this software in any fashion, you are agreeing to be bound bythe terms of this license.  You must not remove this notice, or any other, from this software.
