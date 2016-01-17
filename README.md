# Awesome Java 8  [![Build Status](https://travis-ci.org/tedyoung/awesome-java8.svg?branch=master)](https://travis-ci.org/tedyoung/awesome-java8)

A curated list of useful, if not amazingly awesome, tools, libraries, frameworks, and other resources that take advantage of (or even require) Java 8 features, such as Lambdas, or have a more modern approach to writing Java code. Those that **require** Java 8 are marked with an :8ball: emoji (for "eight ball" or sometimes "billiards").

If you want a larger list of Java resources not specific to Java 8, check out [Awesome Java](https://github.com/akullpp/awesome-java).

----

# Table of Contents

- [Libraries and Frameworks](#libraries-and-frameworks)
    - [Functional libraries](#functional-libraries)
    - [Interoperability libraries](#interoperability-libraries)
    - [Microservices](#microservices)
    - [Networking libraries](#networking-libraries)
    - [Reactive libraries](#reactive-libraries)
    - [Testing](#testing)
    - [Web App/API frameworks](#web-appapi-frameworks)
- [Tools](#tools)
- [Books & Videos](#books--videos)


----

# Libraries and Frameworks

## Functional libraries

Libraries that make Java 8 more functional, especially filling in the gaps in streams.

* [Derive4J](https://github.com/derive4j/derive4j) - Code generator for user-defined algebraic data types (aka sum types) based on an enhanced "visitor" pattern. Provides structural pattern matching, laziness, functional setters (return a copy of an object with one field modified) & more. :8ball:
* [Javaslang](http://javaslang.com/) - Adds the notion of Tuples, along with immutable Values and Pattern Matching, to make it easier to write more functional Java code. :8ball:
* [jOOλ](https://github.com/jOOQ/jOOL) - Part of the jOOQ series of libraries, provides more Functions, Tuples, and `Seq` that provides methods like `crossJoin()`, `join()`, and `groupBy()`. :8ball:
* [ProtonPack](https://github.com/poetix/protonpack) - Offers about a dozen utilities for `Stream`, e.g., `takeWhile`, `zip`, `aggregate`, and a `unique` collector. :8ball: 

## Interoperability libraries

Not sure what to call these other than interoperability libraries, i.e., libraries that make it easier to work with existing libraries that Java 8 provides. I could be convinced to put this under Functional libraries...

* [Cyclops](https://github.com/aol/cyclops) - Very modular, so only include what you need. From function exception handling (`try`), to generic monad operations, to pattern matching. Specific integrations to Javaslang, functionaljava, and Guava. :8ball:

## Microservices

While the term can sometimes be ambiguous, hopefully it'll become more clear as new libraries and frameworks become available. This section may include entire frameworks, or libraries that help with coordinating and connecting separately deployed services (aka microservices).

* [Apollo](http://spotify.github.io/apollo/) - A library for writing HTTP microservices that focuses on composability and simplicity, with high performance using modern Java idioms and features. :8ball:
* [SnoopEE](https://github.com/ivargrimstad/snoop) - While this is "experimental", it's worth looking at if you're coming to microservices from a "slimmed down" Java EE point of view and need something to handle service discovery. This was shown in a JavaOne 2015 conference talk [here](https://youtu.be/REuBLPTeFDg). :8ball:

## Networking libraries

* [Javaslang-CircuitBreaker](https://github.com/javaslang/javaslang-circuitbreaker) - A lightweight, easy-to-use CircuitBreaker library designed for Java8 and functional programming based on Javaslang. :8ball:

## Reactive libraries

Focused on "pulling" items from a stream. There may be overlap between these libraries and the Functional ones (above), but the ones here are primarily/exclusively focused on the [Reactive](http://www.reactive-streams.org/) way of thinking about streams.

* [Simple React](https://github.com/aol/simple-react) - A library that focuses on users needing async and lazy streams. A helpful table comparing the included implementations with Java 8 is [here](https://github.com/aol/simple-react#stream-type-overview). Very well documented with lots of diagrams (yay!). :8ball:

## Testing

* [AssertJ](http://joel-costigliola.github.io/assertj/index.html) - Fluent assertions for Java unit testing, with the 3.0 release requiring Java 8. :8ball:
* [Lambda Behave](http://richardwarburton.github.io/lambda-behave/) - BDD-oriented framework that leverages lambdas to make tests more "behavioral". If you've seen Jasmine or Spock, this will be familiar. :8ball:
* [Mockito](https://github.com/szpak/mockito-java8) - The Java 8-specific version of the wonderful mocking library, Mockito. Works great with *AssertJ*. :8ball:

## Web App/API frameworks

Frameworks (and micro-frameworks) that make it easy to create services that provide Web APIs (aka REST), and/or full web sites without a "full-blown" JAX-RS implementation.

* [Play Framework](https://www.playframework.com/documentation/2.4.x/Installing) - The popular Play Framework, from Typesafe, is "reactive" and built on Akka (the Actor framework) and supports non-blocking I/O, and is stateless. :8ball:
* [Ratpack](https://ratpack.io) - Reactive framework built on the [Netty](http://netty.io/) engine for non-blocking I/O. Also supports Groovy. :8ball:
* [Spark Java](http://sparkjava.com/) - Concise  (micro-) framework for quickly creating Web APIs or web pages. Does not use annotations. Embeds the [Jetty](http://www.eclipse.org/jetty/) web server. :8ball:


# Tools

Tools to help upgrade your code to Java 8, or other utilities that don't become part of your codebase.

* [Modernizer](https://github.com/andrewgaul/modernizer-maven-plugin) - Use this Maven plugin to find out what libraries you can get rid of and replace with Java 8 (and 7) built-in classes.


# Books & Videos

I hesitated to add this, but with the restriction that these be real books and videos (as in, not a promotion or tied to a specific vendor of products), then let's see how this goes.

* [Java 8 in Action](https://www.manning.com/books/java-8-in-action) - One of the earlier Java 8 books, but has lots of good diagrams and pictures to help one learn about things like internal vs. external iteration in streams.
* [Java 8 Lambdas](http://shop.oreilly.com/product/0636920030713.do) - Written by the author of the Lambda Behave testing framework, clearly Richard Warburton knows his lambdas. Concise, yet covers testing & debugging, design, and concurrency.
* [Java SE 8 for the Really Impatient](http://www.informit.com/store/java-se8-for-the-really-impatient-a-short-course-on-9780321927767) - Cay S. Horstmann has been writing Java books forever. This book is right on target and includes even some of the "minor" new features in Java 8, such as using a lambda to do "compare-and-set" operations on atomic variables.
* [What's New in Java 8](https://leanpub.com/whatsnewinjava8) - Free to read online, and includes lots of examples. Includes lambdas, streams, Nashorn (JavaScript engine), and the new Date/Time API.
