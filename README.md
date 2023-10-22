## Introduction to Micronaut and Github Actions CICD

[![github-actions-cicd-demo](https://github.com/Michle99/micronaut_cicd/actions/workflows/cicd-workflow.yml/badge.svg)](https://github.com/Michle99/micronaut_cicd/actions/workflows/cicd-workflow.yml)

## Description

Create a simple micronaut project and github actions workflow.

## Getting Started

Create a Micronaut poject using the Micronaut Launch tool to generate your project:
[Micronaut Launch tool](https://micronaut.io/launch)

## Build and Publishing a JAR

Continuing from the Creating a Github Action, the next step is to build and publish a JAR using Github actions.

Carry out the following steps:
To use an action, visit the action’s page in the marketplace and click “Use latest version” (or choose a specific version).
- Visit the github actions marketplace, get the `checkout` action. click “Use latest version”.
- The below YAML is generated:
```
- name: 'Checkout'
  uses: actions/checkout@v4.1.1
```

- From the same marketplace, search for `setup-java-jdk`, and choose `Setup Java JDK` and get the necessary YAML below.

```
 - name: 'Setup Java JDK'
   uses: actions/setup-java@v3.13.0
   with:
     distribution: 'oracle'
     java-version: '17'

```
- Check the Java version. Setup Java JDK supported versions: 8, 11, 16, 17.

```
- name: 'Check Java Version'
  run: |
    java --version
```
- Progress Check

```
git add . && git commit -m "Checkout code and Setup Java 17" && git push -u origin part-2
```

## Resources

- [User Guide](https://docs.micronaut.io/4.1.5/guide/index.html)
- [API Reference](https://docs.micronaut.io/4.1.5/api/index.html)
- [Configuration Reference](https://docs.micronaut.io/4.1.5/guide/configurationreference.html)
- [Micronaut Guides](https://guides.micronaut.io/index.html)

---

- [Shadow Gradle Plugin](https://plugins.gradle.org/plugin/com.github.johnrengelman.shadow)
- [Micronaut Gradle Plugin documentation](https://micronaut-projects.github.io/micronaut-gradle-plugin/latest/)
- [GraalVM Gradle Plugin documentation](https://graalvm.github.io/native-build-tools/latest/gradle-plugin.html)

#### Feature serialization-jackson documentation

- [Micronaut Serialization Jackson Core documentation](https://micronaut-projects.github.io/micronaut-serialization/latest/guide/)

#### Feature micronaut-aot documentation

- [Micronaut AOT documentation](https://micronaut-projects.github.io/micronaut-aot/latest/guide/)
