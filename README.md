# SHF4J
The Simple HTTP Client Facade for Java (SHF4J) serves as a simple facade or abstraction for various HTTP client frameworks (e.g. java.net.HttpURLConnection, Apache HttpClient, etc.) allowing the end user to plug in the desired HTTP client framework at deployment time. This library idea originated from the Simple Logging Facade for Java [(SLF4J)](http://www.slf4j.org) progect. While SLF4J provides ready to use Logger instances, SHF4J provides HTTP client builders that used for actual client creation and abstracts under the hood the entire creation and adoption to underlying implementation.

## Motivation
A large number of HTTP client libraries exists in the java community, while using more than one in the same project adds more completixy to the code. In Addition to learning curve that is prerequisite for each library. The SHF4J provides an abstraction layer for various libraries, that can be desided upon deployment.

In addition, SHF4J enables cleaner code by declaring all possible exceptions as runtime ones, so its up to the developer decidions whether to handle them.

## Dependencies
* JDK 8+

## Use Cases
* As standard for internal libraries that used across different microservice and perform HTTP calls.
* Correct resource management for open HTTP connections. A content can be consumed only by provided callback - no easy way to expose an input stream.
* Unified configuration for outgoing HTTPS requests like: the used protocol (TLSv1, TLSv1.1, etc.) & the used ciphers list. Can be very useful in applications that must have varios security compliancy.

## Supported Providers
- Okhttp3 3.14.9+ 
- Apache Http Client 4.5+
- Apache Http Client 5.0+
- JDK HTTP Client
- Spring RestTemplate

## Installation
Binaries are deployed on both Maven central & JCenter repositories.

## Version

SHC4J doesn't use SEMVER, and won't. Given a version number **MAJOR.MINOR.FIX**:

* MAJOR = Huge refactoring
* MINOR = New features and minor API changes, upgrading should require ~1 hour of work to adapt sources
* FIX = No API change, just bug fixes, only those are source and binary compatible with same minor version
