# JCenter Publish Script

## Usage

In gradle files.

```gradle
buildscript {
    ......
    dependencies {
        ......
        classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.7.1'
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

[Gradle Bintray Plugin](https://github.com/bintray/gradle-bintray-plugin)
[Gradle Android Maven plugin](https://github.com/dcendents/android-maven-gradle-plugin)

## License
