OASIS Universal Business Language
=================================

UBL is designed to provide a universally understood and recognized commercial syntax for legally binding business documents and to operate within a standard business framework such as ISO 15000 (ebXML) to provide a complete, standards-based infrastructure that can extend the benefits of existing EDI systems to businesses of all sizes. UBL is freely available to everyone without legal encumbrance or licensing fees.

Please refer to the official [open-oasis.org](http://oasis-open.org/) site for the full documentation for [UBL v2.0](http://docs.oasis-open.org/ubl/os-UBL-2.0/UBL-2.0.html), [UBL v2.1](http://docs.oasis-open.org/ubl/os-UBL-2.1/UBL-2.1.html) and [UBL v2.2](https://docs.oasis-open.org/ubl/cs01-UBL-2.2/UBL-2.2.html)

## Why this backports project?

This is due to limitations in maven that prevents you from depending on multiple versions of the same artifact, this project support backports of previous versions.

This enables including multiple versions of the UBL XML schemas in your project, you can use this project for earlier versions and then [tradeshift-ubl-xsd](https://github.com/Tradeshift/tradeshift-ubl-xsd) for the latest version

Do not use this project if you only need one version of the schemas.

## Getting started

### Using the UBL XML Schemas with Maven

```xml
  <dependency>
    <groupId>com.tradeshift</groupId>
    <artifactId>tradeshift-ubl-xsd</artifactId> <!-- Main UBL 2.2 release -->
    <version>2.2.0</version>
  </dependency>
  <dependency>
    <groupId>com.tradeshift</groupId>
    <artifactId>tradeshift-ubl-xsd-2_1</artifactId> <!-- UBL 2.1 backports -->
    <version>2.2.0</version>
  </dependency>
  <dependency>
    <groupId>com.tradeshift</groupId>
    <artifactId>tradeshift-ubl-xsd-2_0</artifactId> <!-- UBL 2.0 backports -->
    <version>2.2.0</version>
  </dependency>
```

### Using the UBL XML Schemas with SBT
```sbt
libraryDependencies +=
  "com.tradeshift" %% "tradeshift-ubl-xsd" % "2.2.0"
libraryDependencies +=
  "com.tradeshift" %% "tradeshift-ubl-xsd-2_1" % "2.2.0"
libraryDependencies +=
  "com.tradeshift" %% "tradeshift-ubl-xsd-2_2" % "2.2.0"
```

### Using the UBL XML Schemas with Gradle
```gradle
dependencies {
  compile 'com.tradeshift:tradeshift-ubl-xsd:2.2.0'
  compile 'com.tradeshift:tradeshift-ubl-xsd-2_1:2.2.0'
  compile 'com.tradeshift:tradeshift-ubl-xsd-2_0:2.2.0'
}
```


## What is included?
The artifact only contains the XML Schemas (XSD) of the Universal Business Language standard. This repository contains an amount of [examples](src/test/resources/org/oasis-open/ubl/examples) that can be a starting point for your learning of UBL.

If you need to depend on the examples for unit tests you can use [tradeshift-ubl-examples](https://github.com/Tradeshift/tradeshift-ubl-examples)

