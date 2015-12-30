# Awesome Java 8

A curated list of useful, if not amazingly awesome, tools, libraries, frameworks, and other resources that take advantage of (or even require) Java 8 features, such as Lambdas, or have a more modern approach to writing Java code. Those that **require** Java 8 are marked with an :8ball: emoji (for "eight ball" or sometimes "billiards").

If you want a larger list of Java resources not specific to Java 8, check out [Awesome Java](https://github.com/akullpp/awesome-java).

----

# Libraries and Frameworks

## Functional libraries

Libraries that make Java more functional, filling in the gaps in streams.

* [Javaslang](http://javaslang.com/) - Adds the notion of Tuples, along with immutable Values and Pattern Matching, to make it easier to write more functional Java code. :8ball:
* [jOOλ](https://github.com/jOOQ/jOOL) - Part of the jOOQ series of libraries, provides more Functions, Tuples, and `Seq` that provides methods like `crossJoin()`, `join()`, and `groupBy()`. :8ball:
* [ProtonPack](https://github.com/poetix/protonpack) - Offers about a dozen utilities for `Stream`, e.g., `takeWhile`, `zip`, `aggregate`, and a `unique` collector. :8ball: 

## Testing

* [AssertJ](http://joel-costigliola.github.io/assertj/index.html) - Fluent assertions for Java unit testing, with the 3.0 release requiring Java 8. :8ball:
* [Mockito](https://github.com/szpak/mockito-java8) - The Java 8-specific version of the wonderful mocking library, Mockito. Works great with *AssertJ*. :8ball:

## Web App/API frameworks

Frameworks (and micro-frameworks) that make it easy to create services that provide Web APIs (aka REST), and/or full web sites without a "full-blown" JAX-RS implementation.

*  [Spark Java](http://sparkjava.com/) - Concise  (micro-) framework for quickly creating Web APIs or web pages. Does not use annotations. Embeds the [Jetty](http://eclipse.org/jetty/) web server. :8ball:
*  [Ratpack](https://ratpack.io) - Reactive framework built on the [Netty](http://netty.io/) engine for non-blocking I/O. Also supports Groovy. :8ball:


# Tools

Tools to help upgrade your code to Java 8, or other utilities that don't become part of your codebase.

* [Modernizer](https://github.com/andrewgaul/modernizer-maven-plugin) - Use this Maven plugin to find out what libraries you can get rid of and replace with Java 8 (and 7) built-in classes.

