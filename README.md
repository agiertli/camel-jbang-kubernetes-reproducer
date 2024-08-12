Camel JBang reproducer:


```bash
jbang alias add -Dcamel.jbang.version=4.8.0-SNAPSHOT --name camel-snapshot camel@apache/camel
jbang camel-snapshot
alias camel-snapshot="jbang camel-snapshot"
camel-snapshot  plugin add kubernetes
camel-snapshot plugin get
camel-snapshot init demo.yaml
camel-snapshot kubernetes run demo.yaml --image-builder=s2i --cluster-type=openshift 
```


Quarkus Reproducer:
```bash
mvn clean install -Dquarkus.openshift.deploy=true -Dquarkus.kubernetes-client.trust-certs=true
```
