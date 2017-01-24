> [Editor's note: how do you feel about the way adding this awesome list to the "master" awesome list has been handled? Am I wrong? Please comment here: https://github.com/sindresorhus/awesome/pull/812. Thanks!]

----

# Awesome Java 8  [![Build Status](https://travis-ci.org/tedyoung/awesome-java8.svg?branch=master)](https://travis-ci.org/tedyoung/awesome-java8) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

A curated list of useful, if not amazingly awesome, tools, libraries, frameworks, and other resources that take advantage of (or even require) Java 8 features, such as Lambdas, or have a more modern approach to writing Java code. Those that **require** Java 8 are marked with an :8ball: emoji (for "eight ball" or sometimes "billiards").

If you want a larger list of Java resources not specific to Java 8, check out [Awesome Java](https://github.com/akullpp/awesome-java).

----

# Contents

- [Libraries and Frameworks](#libraries-and-frameworks)
    - [Caching libraries](#caching-libraries)
    - [Distributed Systems libraries](#distributed-systems-libraries)
    - [Functional libraries](#functional-libraries)
    - [General-purpose libraries](#general-purpose-libraries)
    - [Interoperability libraries](#interoperability-libraries)
    - [Microservices](#microservices)
    - [Networking libraries](#networking-libraries)
    - [Persistence libraries](#persistence-libraries)
    - [Reactive libraries](#reactive-libraries)
    - [Streams libraries](#streams-libraries)
    - [Testing](#testing)
    - [Web App/API frameworks](#web-appapi-frameworks)
- [Tools](#tools)
- [Books](#books)


----

# Libraries and Frameworks

Libraries and frameworks become part of your runtime artifact. Libraries consist of code that you call, whereas frameworks require that you inherit from classes or implement interfaces defined in that framework. *Modern Java* prefers the delegation model of Libraries vs. the inheritance model of frameworks, however in some cases, frameworks might be worth the inheritance cost, e.g., web frameworks.

## Caching Libraries

* [Caffeine](https://github.com/ben-manes/caffeine) - High performance Java 8-based in-memory caching library providing a near optimal "hit rate". Well-documented and flexible. :8ball:

## Distributed Systems libraries

Libraries that support distributed systems, e.g., queues, key-value stores, and quorum/consensus.

* [Atomix](http://atomix.io/atomix/) - Event-driven framework for coordinating fault-tolerant distributed systems built on the Raft consensus algorithm. :8ball:

## Functional libraries

Libraries that make Java 8 more functional, especially filling in the gaps in streams.

* [Derive4J](https://github.com/derive4j/derive4j) - Code generator for user-defined algebraic data types (aka sum types) based on an enhanced "visitor" pattern. Provides structural pattern matching, laziness, functional setters (return a copy of an object with one field modified) & more. :8ball:
* [Javaslang](http://www.javaslang.io/) - Adds the notion of Tuples, along with immutable Values and Pattern Matching, to make it easier to write more functional Java code. :8ball:
* [jOOλ](https://github.com/jOOQ/jOOL) - Part of the jOOQ series of libraries, provides more Functions, Tuples, and `Seq` that provides methods like `crossJoin()`, `join()`, and `groupBy()`. :8ball:
* [ProtonPack](https://github.com/poetix/protonpack) - Offers about a dozen utilities for `Stream`, e.g., `takeWhile`, `zip`, `aggregate`, and a `unique` collector. :8ball:

## General-purpose libraries

For libraries with many features that don't fit in a single category. _Honestly, this section was just created so that it can hold Guava, which as of [Release 21](https://github.com/google/guava/wiki/Release21) requires Java 8+._

* [Guava](https://github.com/google/guava) - One of the most widely used and well-written general-purpose Java libraries. As of Release 21, only works with Java 8 (or later). :8ball:

## Interoperability libraries

Not sure what to call these other than interoperability libraries, i.e., libraries that make it easier to work with existing libraries that Java 8 provides. I could be convinced to put this under Functional libraries...

* [Cyclops](https://github.com/aol/cyclops) - Very modular, so only include what you need. From function exception handling (`try`), to generic monad operations, to pattern matching. Specific integrations to Javaslang, functionaljava, and Guava. :8ball:

## Microservices

While the term can sometimes be ambiguous, hopefully it'll become more clear as new libraries and frameworks become available. This section may include entire frameworks, or libraries that help with coordinating and connecting separately deployed services (aka microservices).
For HTTP-based services, see [Web App/API frameworks](#web-appapi-frameworks).

* [Apollo](http://spotify.github.io/apollo/) - A library for writing HTTP microservices that focuses on composability and simplicity, with high performance using modern Java idioms and features. :8ball:
* [SnoopEE](https://github.com/ivargrimstad/snoop) - While this is "experimental", it's worth looking at if you're coming to microservices from a "slimmed down" Java EE point of view and need something to handle service discovery. This was shown in a JavaOne 2015 conference talk [here](https://www.youtube.com/watch?v=REuBLPTeFDg). :8ball:

## Networking libraries

* [Javaslang-CircuitBreaker](https://github.com/RobWin/javaslang-circuitbreaker) - A lightweight, easy-to-use CircuitBreaker library (inspired by Netflix's Hystrix designed for Java8 and functional programming based on Javaslang and supports RxJava. :8ball:

## Persistence libraries

* [Speedment](https://github.com/speedment/speedment) - A fluent database access library that looks just like Java 8 code, using the Stream API for querying. Supports MySQL, MariaDB, and PostgreSQL. :8ball:

## Reactive libraries

Focused on "pulling" items from a stream. There may be overlap between these libraries and the Functional ones (above), but the ones here are primarily/exclusively focused on the [Reactive](http://www.reactive-streams.org/) way of thinking about streams.

* [Cyclops React](https://github.com/aol/cyclops-react) - A library that focuses on users needing async and lazy streams (formerly Simple React). Very well documented with lots of diagrams (yay!). :8ball:

* [Project Reactor](http://projectreactor.io/) - Reactor is a second-generation Reactive library for building non-blocking applications on
the JVM based on the Reactive Streams Specification. It directly interacts with Java 8 functional API, Completable Future, Stream and Duration. :8ball:

## Streams libraries

These are libraries that enhance existing Java 8 Streams, but aren't trying to define a completely new API.
I could be convinced to put these under the [Functional](#functional-libraries) libraries, but until then...

* [StreamEx](https://github.com/amaembo/streamex) - Does what it says: enhances the Java 8 streams. The ["cheat sheet"](https://github.com/amaembo/streamex/blob/master/CHEATSHEET.md) is really nice: if you know what you want (e.g., swap keys and values coming from entries in a map), it tells you how to get it. :8ball:

## Testing

* [AssertJ](http://joel-costigliola.github.io/assertj/index.html) - Fluent assertions for Java unit testing, with the 3.0 release requiring Java 8. :8ball:
* [Lambda Behave](http://richardwarburton.github.io/lambda-behave/) - BDD-oriented framework that leverages lambdas to make tests more "behavioral". If you've seen Jasmine or Spock, this will be familiar. :8ball:
* [Mockito](https://github.com/szpak/mockito-java8) - The Java 8-specific version of the wonderful mocking library, Mockito. Works great with *AssertJ*. :8ball:

## Web App/API frameworks

Frameworks (and micro-frameworks) that make it easy to create services that provide Web APIs (aka REST), and/or full web sites without a "full-blown" JAX-RS implementation.

* [Bootique](http://bootique.io/) - A "minimally opinionated" web framework that leverages Google's Guice dependency-injection library to include modules such as JOOQ, Curator, Jersey, Kafka, Metrics, and more. :8ball:
* [Jooby Project](https://github.com/jooby-project/jooby) - A modular web framework that supports multiple servers (Netty, Jetty, and Undertow), Websockets, etc., and can be used in many different ways by including a wide variety of modules, e.g., provide a full MVC web site, or just provide APIs. :8ball:
* [Play Framework](https://www.playframework.com/documentation/2.4.x/Installing) - The popular Play Framework, from Typesafe, is "reactive" and built on Akka (the Actor framework) and supports non-blocking I/O, and is stateless. :8ball:
* [Ratpack](https://ratpack.io) - Reactive framework built on the [Netty](http://netty.io/) engine for non-blocking I/O. Also supports Groovy. :8ball:
* [Spark Java](http://sparkjava.com/) - Concise (micro-) framework for quickly creating Web APIs or web pages. Does not use annotations. Embeds the [Jetty](http://www.eclipse.org/jetty/) web server. :8ball:


# Tools

Tools to help upgrade your code to Java 8, generate code, or other utilities that don't become part of your codebase.

* [FreeBuilder](https://github.com/google/FreeBuilder) - Writes builder-pattern builders for your code. Very well documented and supports all major IDEs and build tools. Supports Java 8 [mapper methods](https://github.com/google/FreeBuilder#accessor-methods).
* [Modernizer](https://github.com/andrewgaul/modernizer-maven-plugin) - Use this Maven plugin to find out what libraries you can get rid of and replace with Java 8 (and 7) built-in classes.


# Books

I hesitated to add this, but with the restriction that these be real books and videos (as in, not a promotion or tied to a specific vendor of products), then let's see how this goes.

* [Java 8 in Action](https://www.manning.com/books/java-8-in-action) - One of the earlier Java 8 books, but has lots of good diagrams and pictures to help one learn about things like internal vs. external iteration in streams.
* [Java 8 Lambdas](http://shop.oreilly.com/product/0636920030713.do) - Written by the author of the Lambda Behave testing framework, clearly Richard Warburton knows his lambdas. Concise, yet covers testing & debugging, design, and concurrency.
* [Java SE 8 for the Really Impatient](http://www.informit.com/store/java-se8-for-the-really-impatient-a-short-course-on-9780321927767) - Cay S. Horstmann has been writing Java books forever. This book is right on target and includes even some of the "minor" new features in Java 8, such as using a lambda to do "compare-and-set" operations on atomic variables.
* [What's New in Java 8](https://leanpub.com/whatsnewinjava8) - Free to read online, and includes lots of examples. Includes lambdas, streams, Nashorn (JavaScript engine), and the new Date/Time API.
