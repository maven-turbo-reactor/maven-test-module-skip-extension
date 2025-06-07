# maven-test-module-skip Extension

This extension skips building all test modules (having `test-` prefix or suffix `-test`), removes all dependencies
in the `<scope>test</scope>`. As the result, it's faster than traditional `-Dmaven.test.skip=true`, especially for a
large scale projects.

To set up the extension
```xml
<extensions>
    <extension>
        <!-- https://github.com/maven-turbo-reactor/maven-test-module-skip-extension -->
        <groupId>com.github.seregamorph</groupId>
        <artifactId>maven-test-module-skip-extension</artifactId>
        <version>0.5</version>
    </extension>
</extensions>
```

Sample usage
```shell
./mvn clean install -Dmaven.test.skip=true -DtestModuleSkip=true
```
