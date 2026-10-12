# eccenca Fork Notes

This fork of [ontodev/robot](https://github.com/ontodev/robot) only contains the changes needed to fix vulnerabilities in dependencies.
For the changes, see [CHANGELOG.eccenca.md](CHANGELOG.eccenca.md). For general information, see [README.md](README.md).


## Build with SBOM

`bin/robot.jar` is a shaded jar. Some bundled libraries (e.g. `protobuf-java`, `libthrift`) do not ship Maven metadata, so vulnerability scanners like [Trivy](https://trivy.dev) cannot identify them when scanning the jar itself.
To make all bundled libraries visible, build the jar together with a [CycloneDX](https://cyclonedx.org) SBOM (Software Bill of Materials):

    mvn -B -DskipTests package org.cyclonedx:cyclonedx-maven-plugin:2.9.3:makeBom -pl robot-command -am

This creates:

- `bin/robot.jar`: the self-contained Jar file
- `robot-command/target/bom.json` (and `bom.xml`): the SBOM listing all libraries bundled in `bin/robot.jar`, with the versions resolved by Maven

The SBOM describes the `bin/robot.jar` of the same build, so always keep both files together.
SBOM files are also created in `robot-core/target/` and `target/`; these cover only the respective module and are not needed.

Tests are skipped by `-DskipTests`; run them separately with `mvn clean verify`.


## Scan the SBOM

    trivy sbom robot-command/target/bom.json
