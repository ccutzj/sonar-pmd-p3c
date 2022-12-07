# SonarQube PMD Plugin [![Maven Central](https://maven-badges.herokuapp.com/maven-central/org.sonarsource.pmd/sonar-pmd-plugin/badge.svg)](https://maven-badges.herokuapp.com/maven-central/org.sonarsource.pmd/sonar-pmd-plugin) [![Build Status](https://api.travis-ci.org/jborgers/sonar-pmd.svg?branch=master)](https://travis-ci.org/jborgers/sonar-pmd) [![SonarStatus](https://sonarcloud.io/api/project_badges/measure?project=org.sonarsource.pmd%3Asonar-pmd&metric=alert_status)](https://sonarcloud.io/dashboard?id=org.sonarsource.pmd%3Asonar-pmd) [![SonarStatus](https://sonarcloud.io/api/project_badges/measure?project=org.sonarsource.pmd%3Asonar-pmd&metric=coverage)](https://sonarcloud.io/dashboard?id=org.sonarsource.pmd%3Asonar-pmd)
Sonar-PMD is a plugin that provides coding rules from [PMD](https://pmd.github.io/) for use in SonarQube.

reference: [jborgers/sonar-pmd](https://github.com/jborgers/sonar-pmd)

For a list of all rules and their status, see: [RULES.md](https://github.com/ccutzj/sonar-pmd-p3c/blob/main/docs/RULES.md)
## 说明
此项目基于[jborgers/sonar-pmd](https://github.com/jborgers/sonar-pmd) 3.4.1版本 开发, 修改了<sonar-plugin-api.version>
和<java.frontend.version>版本, 增加阿里巴巴p3c规则, 基于阿里巴巴[p3c-pmd](https://github.com/alibaba/p3c) 2.1.1版本规则并翻译规则标题为中文.

sonarQube版本:Community Edition版本 9.3
## Installation
Download source code, `mvn package`, open this folder`/sonar-pmd-p3c/sonar-pmd-plugin/target`, 
`sonar-pmd-plugin-1.0.0-SNAPSHOT.jar`,
Alternatively, download the [latest JAR file](https://github.com/ccutzj/sonar-pmd-p3c/releases/tag/latest).

put it into the plugin directory (`./extensions/plugins`) and restart SonarQube.

### 以下信息摘自:[jborgers/sonar-pmd](https://github.com/jborgers/sonar-pmd)

## Usage
Usage should be straight forward:
1. Activate some PMD rules in your quality profile.
2. Run an analysis.

### Java version
Sonar-PMD analyzes the given source code with the Java source version defined in your Gradle or Maven project.
In case you are not using one of these build tools, or if that does not match the version you are using, set the `sonar.java.source` property to tell PMD which version of Java your source code complies to. 

Possible values : 1.4 to 1.8/8 to 18

## Table of supported versions
| PMD Plugin                  |2.5|2.6|3.0.0|3.1.x|3.2.x|3.3.x| 3.4.0          |
|-----------------------------|---|---|---|---|---|---|----------------|
| PMD                         |5.4.0|5.4.2|5.4.2|6.9.0|6.10.0|6.30.0| 6.45.0         |
| Max. supported Java Version | 1.7 | 1.8 | 1.8 | 11 | | 15| 18             |
|  Min. SonarQube Version     | 4.5.4 | 4.5.4 | 6.6 | | | 6.7| _8.9(*)_ / 9.3 |

(*) Note: Plugin version 3.4.x runs in SonarQube 8.9, however, Java 17+ is only fully supported in SonarQube 9.3+.

A majority of the PMD rules have been rewritten in the Java plugin. Rewritten rules are marked "Deprecated" in the PMD plugin, but a [concise summary of replaced rules](http://dist.sonarsource.com/reports/coverage/pmd.html) is available.


## Rules on test
PMD tool provides some rules that can check the code of JUnit tests. Please note that these rules (and only these rules) will be applied only on the test files of your project.

## License
Sonar-PMD is licensed under the [GNU Lesser General Public License, Version 3.0](https://github.com/jborgers/sonar-pmd/blob/master/LICENSE.md).

Parts of the rule descriptions displayed in SonarQube have been extracted from [PMD](https://pmd.github.io/) and are licensed under a [BSD-style license](https://github.com/pmd/pmd/blob/master/LICENSE).  

## Build and test the plugin
To build the plugin and run the integration tests:

    ./mvnw clean verify
   
