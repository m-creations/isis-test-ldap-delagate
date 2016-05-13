# isis-test-ldap-delagate
=========================
This is a generated ISIS simple test application which has been generated with Archetype as follows:
```
mvn archetype:generate \
  -D archetypeGroupId=org.apache.isis.archetype \
  -D archetypeArtifactId=simpleapp-archetype \
  -D archetypeVersion=1.12.1 \
  -D groupId=com.mcreations.isis.ldap.delegate \
  -D artifactId=isis-test-ldap-delegate \
  -D version=1.0-SNAPSHOT \
  -B
```

Then some dependencies and some parts of shiro.ini and source have been modified base on the following instruction to enabling module security and LDAP delegation in it:
https://github.com/isisaddons/isis-module-security#how-to-configureuse

The testing this application needs a running docker for ldap as follows:
```
docker run --name tmp-ldap-server -h ldapsrv.weave.local -p 10389:389 -e LDAP_DOMAIN=example.com -e LDAP_ORGANIZATION=com -d mcreations/fusiondirectory-ldap
```