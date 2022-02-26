# Sample Maven Application


Releasing to the Maven Central -

1. Add OSSRH server credentials to settings.xml

```
<server>
    <id>ossrh</id>
    <username>ossrh_jira_id</username>
    <password>ossrh_jira_pwd</password>
</server>
```

2. Export GPG Passphrase to build environment - `export GPG_PASSPHRASE=<Your Passphrase>`

3. Trigger deployment - `./mvnw deploy -Drelease=true`. Setting `release=true` will activate all profiles required for releasing to Maven Central.


Synchronizing to Maven Central note from [Releasing to Central](https://central.sonatype.org/publish/publish-guide/#releasing-to-central) doc:
> Upon release, your component will be published to Central: this typically occurs within 30 minutes, though updates to search can take up to four hours.