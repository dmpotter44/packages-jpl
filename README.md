# *JPL 3.x* documentation home page

## Introduction

**JPL 3.x** is a dynamic, bidirectional interface between *SWI-Prolog 5.2.0* or later and *Java 2* runtimes (see **[*JPL 3.x* Objectives](docs/objectives.html)**). It offers two APIs:

* **Java API** *(Java-calls-Prolog)*: this interface comprises public Java classes which support:
    * constructing Java representations of Prolog terms and queries
    * calling queries within *SWI-Prolog* engines
    * retrieving (as Java representations of Prolog terms) any bindings created by a call
* **Prolog API** *(Prolog-calls-Java)*: this interface comprises Prolog library predicates which support:
    * creating instances (objects) of Java classes (built-in and user-defined)
    * calling methods of Java objects (and static methods of classes), perhaps returning values or object references
    * getting and setting the values of fields of Java objects and classes

Calls to the two APIs can be nested, e.g. Java code can call Prolog predicates which call Java methods which call Prolog predicates etc.

## Prerequisites

**JPL 3.x** currently requires *SWI-Prolog 5.2.0* or later (it uses multi-threading FLI calls not available in older versions). If you are using *SWI-Prolog 5.1.X*, then you should probably upgrade to the latest stable *5.2.X* release. Support for earlier versions may be added in the future.

***JPL 3.x*** currently requires a *Java 2* runtime (or development kit), and has been tested with Sun's `jdk1.3.1_01`.

***JPL 3.x*** contains a native library (`jpl.c`) written in *ANSI/ISO C* and designed to be portable to many operating system platforms for which suitable compilers are available. It has, however, only been tested with *Microsoft Visual C/C++ 5* under *Windows NT 4.0 (SP6a)*. I shall be grateful if anyone can (show me how to) tidily adapt the source and makefiles to build for other platforms.

## Documentation

This alpha release of ***JPL&nbsp;3.x*** contains a hotch-potch of documentation, some left over from Fred Dushin's (Java-calls-Prolog) *JPL 1.0.1* and now obsolete or misleading, some rewritten for *JPL 2.0.2* and still mostly applicable, and some written for the first release of my Prolog-calls-Java interface, now part of ***JPL***, and also mostly still relevant.

In addition to this document (index.html in jpl's root folder) there are:

* **[Release Notes](docs/release_notes.html) for 3.0.3, 3.0.2, 3.0.0 and 2.0.2**
* **[Installation](docs/installation.html)**
* **Java API:**
    * **[Reference (Javadoc)](docs/java_api/javadoc/index.html)**
    * **[Overview](docs/java_api/high-level_interface.html)**
    * **[Gotchas](docs/java_api/gotchas.html)**
    * **[Getting Started](docs/java_api/getting_started.html)**
* **Prolog API:**
    * **[Reference](docs/prolog_api/api.html)**
    * **[Overview](docs/prolog_api/overview/index.html)**
    * **[Gotchas](docs/prolog_api/gotchas.html)**

## Installation

Put the three library files (*jpl.dll*, *jpl.jar* and *jpl.pl*) where they can be found by your OS, by your Java apps and by SWI-Prolog respectively; for details, see **[*JPL
3.x* Installation](docs/installation.html)**.

## Testing

Each of the folders within `jpl\examples\java` contains a simple *Java* application which tests some aspect of **JPL**. These applications are already compiled, and each folder contains a (*DOS/Windows*) script `run.bat` which announces and runs the demo.

Each of the Prolog source files within `jpl/examples/prolog` contains a self-contained Prolog application which exercises JPL from within Prolog; start an interactive SWI-Prolog session as usual, and then consult and run these files.

[Paul Singleton](mailto:paul.singleton@bcs.org.uk)<br>
February 2004
