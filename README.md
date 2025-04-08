# ilsos-pom
![Powered by](https://img.shields.io/badge/Powered%20by-Mulesoft-535597.svg) [![Build Status](https://dev.azure.com/ILSOSdevOps/ILSOSMuleSoft/_apis/build/status%2Filsos-pom?branchName=main)](https://dev.azure.com/ILSOSdevOps/ILSOSMuleSoft/_build/latest?definitionId=11&branchName=main)
<br>

Parent POM for Mulesoft applications 

## Table of contents
1. [Description](#description)
1. [Using the parent POM](#usinge-the-parent-pom)
1. [Mulesoft Runtime release notes](#mulesoft-runtime-release-notes)
1. [List of plugins and dependencies](#list-of-plugins-and-dependencies)
1. [Recommended content](#recommended-content)

<br>  

## Description

In Maven, a parent POM is a concept that allows you to define a common configuration and set of dependencies for multiple related projects within an organization or a software development team. It promotes code reuse and consistency across projects.

The parent POM acts as a blueprint or a template for child projects. It defines common configuration elements such as project version, organization details, build settings, and repositories. It also includes dependency management sections where you can define the shared dependencies required by all child projects. This allows you to centrally manage the versions and configurations of shared libraries and frameworks.

When you create a new Maven project, you can specify a parent POM from which the new project inherits its configuration. The child project can then override or extend the configuration inherited from the parent POM as needed. By inheriting from a parent POM, the child projects automatically adopt the common settings defined in the parent, reducing duplication and making it easier to maintain consistency across the project ecosystem.

In addition to configuration inheritance, the parent POM can also define common build plugins, profiles, and other build-related configurations that are shared among multiple projects.

To summarize, a Maven parent POM provides a way to define and share common configuration, dependencies, and build settings across multiple projects, enabling consistency, code reuse, and centralized management of project-related settings.

<br>  

## Using the parent POM
To use the parent POM in any of the child projects, specify the `parent` section in the child `pom.xml` as follows:

```xml
	<parent>
		<groupId>0fa744b1-1284-46c5-b23c-0eb98ea787e3</groupId>
		<artifactId>ilsos-pom</artifactId>
		<version>1.0.17</version>
		<relativePath/>
	</parent>
``` 

Update the element `version` to match the latest release available.

<br> 

## Mulesoft Runtime release notes

Mulesoft Runtime Documentation:

* https://docs.mulesoft.com/release-notes/mule-runtime/mule-esb 
* https://docs.mulesoft.com/release-notes/mule-runtime/mule-4.7.0-release-notes
* https://docs.mulesoft.com/release-notes/mule-runtime/mule-4.6.0-release-notes

Java Support

* https://docs.mulesoft.com/general/java-support

GovCloud Notes:

* https://docs.mulesoft.com/release-notes/gov-cloud/gov-cloud-release-notes

Mule Runtime Patch Update Release Notes for Mule Apps on Runtime Fabric

* https://docs.mulesoft.com/release-notes/runtime-fabric/runtime-fabric-runtimes-release-notes

<br> 

## List of plugins and dependencies
Next are the plugins and dependencies included in the parent POM and the link to check new versions.

**Maven plugins**

| Artifact      | Documentation / Versions available |
| ----------- | ----------- |
| maven-enforcer-plugin | https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-enforcer-plugin | 
| maven-site-plugin | https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-site-plugin | 
| maven-project-info-reports-plugin | https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-project-info-reports-plugin | 
| versions-maven-plugin | https://mvnrepository.com/artifact/org.codehaus.mojo/versions-maven-plugin | 
| maven-resources-plugin | https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-resources-plugin | 
| maven-clean-plugin | https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-clean-plugin | 

**Mulesoft plugins**

| Artifact      | Documentation / Versions available |
| ----------- | ----------- |
| mule-maven-plugin | https://mvnrepository.com/artifact/org.mule.tools.maven/mule-maven-plugin?repo=mulesoft-public | 
| | https://docs.mulesoft.com/release-notes/mule-maven-plugin/mule-maven-plugin-release-notes | 
| | https://help.mulesoft.com/s/article/Issues-with-Maven-3-9-0-when-deploying | 
| exchange-mule-maven-plugin | https://mvnrepository.com/artifact/org.mule.tools.maven/exchange-mule-maven-plugin?repo=mulesoft-releases | 
| munit-maven-plugin | https://mvnrepository.com/artifact/com.mulesoft.munit.tools/munit-maven-plugin?repo=mulesoft-releases | 
| | https://docs.mulesoft.com/release-notes/mule-maven-plugin/mule-maven-plugin-release-notes |
| munit-tools | https://mvnrepository.com/artifact/com.mulesoft.munit/munit-tools?repo=mulesoft-releases | 
| munit-runner | https://mvnrepository.com/artifact/com.mulesoft.munit/munit-runner |

**Common dependencies for all services**

| Artifact      | Documentation / Versions available |
| ----------- | ----------- |
| mule-http-connector | https://mvnrepository.com/artifact/org.mule.connectors/mule-http-connector?repo=mulesoft-releases | 
| mule-apikit-module | https://mvnrepository.com/artifact/org.mule.modules/mule-apikit-module?repo=mulesoft-releases | 
| mule-tracing-module | https://mvnrepository.com/artifact/org.mule.modules/mule-tracing-module?repo=mulesoft-releases | 
| mule-validation-module | https://mvnrepository.com/artifact/org.mule.modules/mule-validation-module?repo=mulesoft-public |
| assertions | https://mvnrepository.com/artifact/org.mule.weave/assertions?repo=mulesoft-releases |

**Dependencies for Mule Metrics Toolkit Application**

| Artifact      | Documentation / Versions available |
| ------------- | ----------- |
| mule-objectstore-connector | https://mvnrepository.com/artifact/org.mule.connectors/mule-objectstore-connector?repo=mulesoft-releases | 
| mule-secure-configuration-property-module | https://mvnrepository.com/artifact/com.mulesoft.modules/mule-secure-configuration-property-module | 
| mule-custom-metrics-extension | https://docs.mulesoft.com/custom-metrics-connector/2.2/custom-metrics-connector-reference | 
|  | https://mvnrepository.com/artifact/org.mule.connectors/mule-custom-metrics-extension | 
| mule-sfdc-analytics-connector | https://www.mulesoft.com/exchange/com.mulesoft.connectors/mule-sfdc-analytics-connector/ | 
|  | https://docs.mulesoft.com/salesforce-analytics-cloud-connector/3.12 | 
| mule-mongodb-connector | https://www.mulesoft.com/exchange/com.mulesoft.connectors/mule-mongodb-connector/ | 
|  | https://mvnrepository.com/artifact/com.mulesoft.connectors/mule-mongodb-connector | 
| mongodb-driver-legacy | https://mvnrepository.com/artifact/org.mongodb/mongodb-driver-legacy | 
| mule-file-connector | https://mvnrepository.com/artifact/org.mule.connectors/mule-file-connector | 

**Spring Framework dependencies**

The spring libraries are dependent on theMulesoft Runtime version, so they shoud not be updated to the latest available version. Spring Module release notes: https://docs.mulesoft.com/release-notes/connector/spring-module-release-notes

| Artifact      | Documentation / Versions available |
| ----------- | ----------- |
| mule-spring-module | https://mvnrepository.com/artifact/org.mule.modules/mule-spring-module?repo=mulesoft-public |
|  | https://www.mulesoft.com/exchange/org.mule.modules/mule-spring-module |
|  | https://docs.mulesoft.com/release-notes/connector/spring-module-release-notes |
| spring-core | https://mvnrepository.com/artifact/org.springframework/spring-core | 
| spring-security-core | https://mvnrepository.com/artifact/org.springframework.security/spring-security-core | 

**Databases**

| Artifact      | Documentation / Versions available |
| ----------- | ----------- |
| derby | https://mvnrepository.com/artifact/org.apache.derby/derby/10.14.2.0 | 
|       | It is dependent on Mule JDK compatibility. This is the last version compatible with jdk8 |
| commons-dbcp2 | https://mvnrepository.com/artifact/org.apache.commons/commons-dbcp2 | 
| mssql-jdbc | https://mvnrepository.com/artifact/com.microsoft.sqlserver/mssql-jdbc | 
| mssql-jdbc_auth | https://mvnrepository.com/artifact/com.microsoft.sqlserver/mssql-jdbc_auth |
|                 | https://repo1.maven.org/maven2/com/microsoft/sqlserver/mssql-jdbc_auth/ |
| mule-db-connector | https://mvnrepository.com/artifact/org.mule.connectors/mule-db-connector?repo=mulesoft-releases | 
| mule4-snowflake-connector | https://anypoint.mulesoft.com/exchange/com.mulesoft.connectors/mule4-snowflake-connector | 
| snowflake-jdbc | https://mvnrepository.com/artifact/net.snowflake/snowflake-jdbc | 
|                | https://docs.snowflake.com/en/developer-guide/jdbc/jdbc | 

**Log Management**

| Artifact      | Documentation / Versions available |
| ----------- | ----------- |
| log4j-core | https://mvnrepository.com/artifact/org.apache.logging.log4j/log4j-core | 
| log4j-api | https://mvnrepository.com/artifact/org.apache.logging.log4j/log4j-api | 
| logzio-log4j2-appender | https://mvnrepository.com/artifact/io.logz.log4j2/logzio-log4j2-appender | 
| logzio-sender | https://mvnrepository.com/artifact/io.logz.sender/logzio-sender | 

<br>

**Salesforce connectors**

* mule-salesforce-connector

    Cloudhub

    Exchange - https://anypoint.mulesoft.com/exchange/com.mulesoft.connectors/mule-salesforce-connector
    
    Releases - https://maven.anypoint.mulesoft.com/api/v3/maven/com/mulesoft/connectors/mule-salesforce-connector/maven-metadata.xml

    GovCloud

    Exchange - https://gov.anypoint.mulesoft.com/exchange/com.mulesoft.connectors/mule-salesforce-connector
    
    Releases - https://maven.gov.anypoint.mulesoft.com/api/v2/maven/com/mulesoft/connectors/mule-salesforce-connector/maven-metadata.xml

* mule-sfdc-analytics-connector

    Cloudhub

    Exchange - https://www.mulesoft.com/exchange/com.mulesoft.connectors/mule-sfdc-analytics-connector/
    
    Releases - https://maven.anypoint.mulesoft.com/api/v3/maven/com/mulesoft/connectors/mule-sfdc-analytics-connector/maven-metadata.xml

    GovCloud
    
    Exchange - https://gov.anypoint.mulesoft.com/exchange/com.mulesoft.connectors/mule-sfdc-analytics-connector
    
    Releases - https://maven.gov.anypoint.mulesoft.com/api/v2/maven/com/mulesoft/connectors/mule-sfdc-analytics-connector/maven-metadata.xml

<br>

**Optional artifacts**

| Artifact      | Documentation / Versions available |
| ----------- | ----------- |
| mule-ftp-connector | https://mvnrepository.com/artifact/org.mule.connectors/mule-ftp-connector | 
| mule-sftp-connector | https://mvnrepository.com/artifact/org.mule.connectors/mule-sftp-connector | 
| mule-email-connector | https://mvnrepository.com/artifact/org.mule.connectors/mule-email-connector?repo=mulesoft-releases | 
| mule-ibm-ctg-connector | https://www.mulesoft.com/exchange/com.mulesoft.connectors/mule-ibm-ctg-connector/ | 


## Recommended content
* [How to work with a parent pom](https://help.mulesoft.com/s/article/How-to-work-with-a-parent-pom)
* [How to deploy mule extension with pom hierarchy to exchange](https://help.mulesoft.com/s/article/How-to-deploy-mule-extension-with-pom-hierarchy-to-exchange)

---
[GIT Commit Message Standard](https://github.com/ahmadawais/Emoji-Log)
[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)