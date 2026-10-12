<!-- markdownlint-disable MD012 MD013 MD024 MD033 -->
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/) and this project adheres to [Semantic Versioning](https://semver.org/)

This changelog covers the changes of the [eccenca fork](https://github.com/eccenca/robot) on top of upstream [ontodev/robot](https://github.com/ontodev/robot). For upstream changes, see [CHANGELOG.md](CHANGELOG.md).

## [1.9.11] 2026-10-12

### Fixed

- Fix vulnerabilities CVE-2026-1225, CVE-2026-9828, CVE-2026-19032, CVE-2026-49844, CVE-2026-54512, CVE-2026-54513, CVE-2026-54514, CVE-2026-54515, CVE-2026-59888, CVE-2026-68497, CVE-2026-77310, CVE-2026-83557, CVE-2026-91776, CVE-2026-91777, GHSA-72hv-8253-57qq.

### Changed

- Based on upstream ROBOT v1.9.11.
- Update com.google.guava:guava from 31.1-jre to 33.5.0-jre.
- Update ch.qos.logback:logback-classic from 1.5.6 to 1.5.37.
- Update org.apache.jena:jena-arq and org.apache.jena:jena-tdb from 3.17.0 to 4.10.0.
- Update org.apache.poi:poi and org.apache.poi:poi-ooxml from 5.4.1 to 5.5.1.
- Update org.yaml:snakeyaml from 1.31 to 2.5.
- Update com.opencsv:opencsv from 5.3 to 5.12.0.
- Update com.fasterxml.jackson.core:jackson-core from 2.18.8 to 2.22.3.
- Update com.fasterxml.jackson.dataformat:jackson-dataformat-yaml from 2.12.2 to 2.22.3.
- Update com.fasterxml.jackson.core:jackson-annotations from 2.12.2 to 2.22.
- Add explicit versions for transitive dependencies org.apache.logging.log4j:log4j-api 2.26.1, com.fasterxml.jackson.core:jackson-databind 2.22.3, org.apache.james:apache-mime4j-core 0.8.13 and org.apache.commons:commons-lang3 3.20.0.
- Exclude commons-lang:commons-lang from the robot-core dependency in robot-command.
- Use `ResultSetLang.RS_TSV` and `ResultSetLang.RS_XML` in `QueryOperation`, required by the Jena 4 update.
