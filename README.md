# Kotlin Notes

These are my notes on my journey of learning Kotlin. I hope to share bite-sized pieces of how to do things in Kotlin.

There's already a lot of great information (listed below), so I'll try to cover what's not covered (i.e. what I learned through opening 20-30 tabs and intensive stackoverflowing :p)

PRs welcome :-)

## Resources

* [awesome-kotlin](https://github.com/KotlinBy/awesome-kotlin) - a first stop for anything kotlin-related
* [baeldung](https://www.baeldung.com/?s=kotlin) - lots of blogposts with useful nuggets of information

## TOCs / what I learned the hard way

* Initializing Kotlin projects
    - Using gradle
* dependency management (gradle)
    - finding out dependency versions
    - installing dependencies
* Language constructs
    - generics / reified functions
    - data classes
    - [Kotlin idioms](https://kotlinlang.org/docs/reference/idioms.html)
* Functional programming
    - basics (map, filter, fold)
    - Arrow constructs (e.g. Either, Option, etc.)
* unit testing
    - JUnit
    - kotest
    - Mocking with mockk
* Making http requests
    - HTTP request clients
    - JSON encoding/decoding
    - coroutines / async stuff
* Passing environment variables or system properties to application
* Dockerising gradle project (is it worth waiting minutes for gradle daemon cold starts though?)

## Initializing Kotlin projects (using gradle)

``` sh
mkdir my-project
cd my-project

# install gradle if it's not installed
which gradle || brew install gradle

# create scaffold kotlin project
gradle init # Select “application” > “Kotlin” > "Kotlin DSL". Selecting “application” helps to bootstrap a test 

# run tests
./gradlew test # (or run tests from IDE)
```

This [short video](https://www.youtube.com/watch?v=dldzAi-XRFI) explains how to configure [IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=mac) to know about the newly created gradle project
