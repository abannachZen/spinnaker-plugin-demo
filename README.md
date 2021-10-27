# Spinnaker Plugin Demo

This repo is intended to be a playground to test changes to the Spinnaker Gradle Project extensions.

## How to use

Projects have been created with different gradle project structures. This allows for testing changes that may affect how
a gradle project is viewed by the Spinnaker gradle plugins.

1. Make changes to the spinnaker-gradle-project
2. Build and publish locally with version `local-SNAPSHOT` - `cd <spinnaker-gradle-plugin project> && ./gradlew publishToMavenLocal -Pversion=local-SNAPSHOT`
3. run `./bundle-and-compare.sh`

## Projects

- Classic

  - `classic-ui` - only a UI extension
  - `classic-service` - only a Service extension
  - `classic-ui-service` - both UI and Service extensions

- Monorepo
  - `monorepo-ui` - only a UI extension
  - `monorepo-service` - only a Service extension
  - `monorepo-ui-service` - both UI and Service extensions
