# Spinnaker Plugin Demo

This repo is intended to be a playground to test changes to the Spinnaker Gradle Project extensions.

## How to use

Projects have been created with different gradle project structures. This allows for testing changes that may affect how
a gradle project is viewed by the Spinnaker gradle plugins.

1. Make changes to the spinnaker-gradle-project
2. Build and publish locally with version `local-SNAPSHOT` - `cd <spinnaker-gradle-plugin project> && ./gradlew publishToMavenLocal -Pversion=local-SNAPSHOT`
3. To test your changes you can run `./gradlew releaseBundle` and `./gradlew -Dorg.gradle.project.spinnakerGradleVersion=local-SNAPSHOT releaseBundle`
from each of the below project directories.
   1. the first will run with the version defined in `gradle.properties` the second will reference your locally released version.
   2. If you want to compare the contents of the bundles, rename the `build` directory `tmpBuild` in the respective projects 
this directory is ignored by git.

## Projects

- Classic
  - This project is structured like a traditional spinnaker plugin project. Where the root module contains the bundle extension
- Monorepo
  - This project is structured in a monorepo fashion where it has two subprojects that are separate plugins, but are shared
under one umbrella monorepo.
