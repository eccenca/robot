<!-- markdownlint-disable MD012 MD013 MD024 MD033 -->
# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/) and this project adheres to [Semantic Versioning](https://semver.org/)

This changelog covers the changes of the [eccenca fork](https://github.com/eccenca/robot) on top of upstream [ontodev/robot](https://github.com/ontodev/robot). For upstream changes, see [CHANGELOG.md](CHANGELOG.md).

## [Unreleased]

### Fixed

- Fix vulnerabilities CVE-2020-8908, CVE-2020-13949, CVE-2020-36518, CVE-2021-39239, CVE-2021-46877, CVE-2022-1471, CVE-2022-38752, CVE-2022-41854, CVE-2022-42003, CVE-2022-42004, CVE-2022-42889, CVE-2023-2976, CVE-2024-12798, CVE-2024-12801, CVE-2024-21742, CVE-2025-11226, CVE-2025-48734, CVE-2025-48924, CVE-2025-49128, CVE-2025-52999, CVE-2026-1225.

### Changed

- Based on upstream ROBOT v1.9.8.
- Update com.google.guava:guava from 31.1-jre to 33.5.0-jre.
- Update ch.qos.logback:logback-classic from 1.5.6 to 1.5.25.
- Update org.apache.jena:jena-arq and org.apache.jena:jena-tdb from 3.17.0 to 4.10.0.
- Update org.apache.poi:poi and org.apache.poi:poi-ooxml from 5.4.1 to 5.5.1.
- Update org.yaml:snakeyaml from 1.31 to 2.5.
- Update com.opencsv:opencsv from 5.3 to 5.12.0.
- Update com.fasterxml.jackson.core:jackson-core from 2.12.2 to 2.20.1.
- Update com.fasterxml.jackson.dataformat:jackson-dataformat-yaml from 2.12.2 to 2.20.1.
- Update com.fasterxml.jackson.core:jackson-annotations from 2.12.2 to 2.20.
- Update org.geneontology:relation-graph_2.13 from 2.3.2 to 2.3.3.
- Add explicit versions for transitive dependencies org.apache.james:apache-mime4j-core 0.8.13 and org.apache.commons:commons-lang3 3.20.0.
- Exclude commons-lang:commons-lang from the robot-core dependency in robot-command.
- Use `ResultSetLang.RS_TSV` and `ResultSetLang.RS_XML` in `QueryOperation`, required by the Jena 4 update.
- Run the Java CI workflow only on manual trigger (`workflow_dispatch`) instead of on push and pull request to master.
