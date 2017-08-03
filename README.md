# JCenter Publish Script

[![License](https://img.shields.io/badge/license-GPL-green.svg?style=flat-square)](https://github.com/pexcn/jcenter-publish-script/blob/master/LICENSE)

## Usage

In gradle files.

```gradle
buildscript {
    ......
    dependencies {
        ......
        classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7.3'
        classpath 'com.github.dcendents:android-maven-gradle-plugin:1.5'
    }
}

ext {
    libraryName = 'Library Name'
    libraryDescription = 'Library Description'
    libraryVersionName = 'Library Version Name'
    libraryVersionCode = Library Version Code

    groupId = 'Group Id'
    artifactId = 'Artifact Id'

    siteUrl = "Website Url"
    gitUrl = "Git Url"

    licenseName = 'The GNU General Public License v3.0'
    licenseUrl = 'https://www.gnu.org/licenses/gpl-3.0.txt'
    licenses = ["GPL-3.0"]

    developerId = 'Developer Id'
    developerName = 'Developer Name'
    developerEmail = 'Developer E-mail'
}

apply plugin: 'com.android.library'
......
apply from: 'https://github.com/pexcn/jcenter-publish-script/raw/master/install.gradle'
apply from: 'https://github.com/pexcn/jcenter-publish-script/raw/master/bintray.gradle'
```

In `local.properties`.
```
bintray.user=yourusername
bintray.apikey=yourapikey
```

## Publish
```
gradle bintrayUpload
```

## Dependencies

* [Gradle Bintray Plugin](https://github.com/bintray/gradle-bintray-plugin)
* [Gradle Android Maven plugin](https://github.com/dcendents/android-maven-gradle-plugin)

## License

![GPL v3](https://www.gnu.org/graphics/gplv3-127x51.png)

```
Copyright (C) 2016 Xingyu Chen <pexcn97@gmail.com>

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
```
