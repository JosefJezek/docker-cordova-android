# Cordova Android Development Environment Docker Image

OpenJDK8 + Gradle + Node.js LTS + Android SDK Command Line Tools + Android SDK Build Tools for Cordova Build

Docker tag is eqivalent to [cordova-android](https://github.com/apache/cordova-android) package major version.

[![Docker Badge](https://dockeri.co/image/josefjezek/cordova-android-dev-env)](https://hub.docker.com/r/josefjezek/cordova-android-dev-env)

## How to use the image with Bitbucket Pipelines

```
pipelines:
  default:
    - step:
        name: Build and test
        image: josefjezek/cordova-android-dev-env:8
        caches:
          - node
        script:
          - npm install
          - npm test
          - npm run build
```
