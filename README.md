# Moqui Atomikos Tool Component

[![license](http://img.shields.io/badge/license-CC0%201.0%20Universal-blue.svg)](https://github.com/moqui/moqui-atomikos/blob/master/LICENSE.md)
[![release](http://img.shields.io/github/release/moqui/moqui-atomikos.svg)](https://github.com/moqui/moqui-atomikos/releases)

Moqui tool component for Atomikos Transactions Essentials for JTA and connection pool. This replaces the default 
Bitronix transaction manager in Moqui Framework.

To install run (with moqui-framework):

    $ ./gradlew getComponent -Pcomponent=moqui-atomikos

This will add the component to the Moqui runtime/component directory. 

The Atomikos and dependent JAR files are added to the lib directory when the build is run for this component, which is
designed to be done from the Moqui build (ie from the moqui root directory) along with all other component builds. 

To use just install this component. The configuration for the TransactionInternal implementation is already in place in 
the MoquiConf.xml included in this component (with a transaction-facade.transaction-internal elements) and will be 
merged with the main configuration at runtime. 
