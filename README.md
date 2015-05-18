[![Coverage Status](https://coveralls.io/repos/lukashinsch/spring-boot-actuator-logview/badge.svg?branch=master)](https://coveralls.io/r/lukashinsch/spring-boot-actuator-logview?branch=master)
[![Build Status](https://travis-ci.org/lukashinsch/spring-boot-actuator-logview.svg?branch=master)](https://travis-ci.org/lukashinsch/spring-boot-actuator-logview)
[![Maven Central](https://maven-badges.herokuapp.com/maven-central/eu.hinsch/spring-boot-actuator-logview/badge.svg)](https://maven-badges.herokuapp.com/maven-central/eu.hinsch/spring-boot-actuator-logview/)

# spring-boot-actuator-logview

[![Join the chat at https://gitter.im/lukashinsch/spring-boot-actuator-logview](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/lukashinsch/spring-boot-actuator-logview?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)
Simple logfile viewer as spring boot actuator endpoint

Features
* allow quick access to spring-boot web application logfiles
* uses actuator framework to provide management endpoint
* list log folder content
* view individual logfiles
* view content of log archives (*.zip, *.tar.gz)
* browse subdirectories
* search in (non-compressed) files in logging root folder
* tail without reading entire file

Howto use
* include library on classpath of spring-boot app
* configure logging.path in spring environment 
(alternatively - when using custom logging configuration or logging.file - use endpoints.logview.path)
* endpoint will be available under <management-base>/log

Maven
```xml
<dependency>
    <groupId>eu.hinsch</groupId>
    <artifactId>spring-boot-actuator-logview</artifactId>
    <version>0.2.6</version>
</dependency>
```

Gradle
```groovy
compile 'eu.hinsch:spring-boot-actuator-logview:0.2.6'
```
Note
* lib depends on spring-boot-starter-freemarker, so it may currently not work with another templating engine for the main app
