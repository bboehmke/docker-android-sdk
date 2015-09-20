Android SDK
===========

Usage
-----

For example if you have an Android Project (Gradle based) at 
```~/AndroidStudioProjects/Project/``` you can build the project with:

```
docker run --rm \
    -v "$PWD":/src/ \
    bboehmke/android-sdk \
    gradle build
```

If the gradle cache should be kept between builds use:
```
docker run --rm \
    -v /docker/data/androidGradle:/root/ \
    -v "$PWD":/src/ \
    bboehmke/android-sdk \
    gradle build
```
