# Java SDK

## Using the Client Library

In gradle:

```
implementation group: 'io.argoproj.workflow', name: 'argo-client-java', version: 'v3.4.18'
```

In maven:

```xml
<dependency>
    <groupId>io.argoproj.workflow</groupId>
    <artifactId>argo-client-java</artifactId>
    <version>v3.4.18</version>
</dependency>
```

## Building and deploying for Nexus

You will need your `~/.m2/settings.xml` file set up with a nexus credential
that has write access.

```bash
cd sdks/java
make generate
cp -f pom.xml client
cd client
mvn deploy -Dmaven.test.skip=true -Psonatype_deploy -DskipStaging=true
```

## Docs

* [Event service](client/docs/EventServiceApi.md)
* [Sensor service](client/docs/SensorServiceApi.md)
* [Event source service](client/docs/EventSourceServiceApi.md)
* [Info service](client/docs/InfoServiceApi.md )
* [Pipeline service](client/docs/PipelineServiceApi.md)
* [Workflow service](client/docs/WorkflowServiceApi.md)
