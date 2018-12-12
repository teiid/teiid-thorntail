# Thorntail Teiid

[![Build Status](https://travis-ci.org/teiid/teiid-thorntail.svg?branch=master)](https://travis-ci.org/teiid/teiid-thorntail)

This project contains the source code and examples for Teiid Runtime Engine based on Thorntail. Using these modules you can build a executable uber jar that is equivalent to having a single vdb based WildFly Server.

Thorntail based Teiid is ideal to be executed in Docker environments or Cloud environments like OpenShift. 

Start with `$mvn clean install` to build everything, including the examples.  Then checkout the `examples` folder for various examples you can start with.

## Migration from older Teiid Thorntail

To migrate from an older version of Teiid Thorntail which was using aftifacts from io.thorntail, you will need to update you pom(s).

- Update to an appropriate version of thorntail
- Update io.thorntail:bom-all to the org.teiid:thorntail-bom
- Update io.thorntail:teiid to org.teiid:thorntail-runtime
- Update source/translator dependencies from io.thorntail:teiid-XXX to org.teiid:thorntail-XXX
- If applicible update the odata fraction from io.thorntail:odata to org.teiid:thorntail-odata-api

# Releasing

Snapshots can be created with `$mvn clean deploy` - but this has also been enabled automatically for every non-tagged commit in the .travis.yml file.

A full release should still use the maven release logic.  `$mvn release:prepare`, then `$mvn release:perform`.  The examples will be revisioned, but will not be pushed to a repository.


 
