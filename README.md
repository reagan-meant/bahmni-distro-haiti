<img src="readme/flag_of_Haiti.png" alt="Haiti Flag" width="500"/>

# Bahmni distribution for Haiti

_Bahmni distribution for Haiti to bring common configuration and metadata to child distributions._

-----

This repository maintains the 'distro POM' for the _Bahmni distribution for Haiti_.

It downloads and brings in one place all artifacts needed by the distribution, simply run:
```
mvn clean package
```

This distribution should be used to inherit configuration and metadata that is common across Bahmni implementations in Haiti, such as a the Address Hierarchy, Registration screens, Concept Dictionary...

To use it, simply refer to it as a `<parent>` in the child distribution **pom.xml** file:
```xml
<parent>
  <groupId>net.mekomsolutions</groupId>
  <artifactId>bahmni-distro-haiti</artifactId>
  <version>1.0.0</version>
</parent>
```

### Target inventory:

* `bahmni_emr/`
<br/>The target version of the front-end apps that makes 'Bahmni EMR'.
* `bahmni_config/`
<br/>The bespoke Bahmni configuration (more [here](https://github.com/mekomsolutions/bahmni-config-jib)) to be consumed by Bahmni Apps.
* `openmrs_modules/`
<br/>The required set of OpenMRS modules.
* `openmrs_config/`
<br/>The OpenMRS bespoke configuration (more [here](https://github.com/mekomsolutions/openmrs-config-jib)) to be processed by the [Initializer module](https://github.com/mekomsolutions/openmrs-module-initializer).
* `openmrs_core/`
The target version of OpenMRS Core.
