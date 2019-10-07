# mvn
Namespace for Maven registry

In theory, once I've published one or more artifacts into this namespace, you should be able to access them like this:

## Gradle:
```
repositories {
  maven {
    url 'https://maven.pkg.github.com/ph120ph37/mvn'
  }
}

dependencies {
  implementation 'com.ameriwether:foo:1.2.3';
}
```

## Maven:
```
<project>
  ...
  <repositories>
    ...
    <repository>
      <id>github-p120ph37</id>
      <name>GitHub OWNER Apache Maven Packages</name>
      <url>https://maven.pkg.github.com/ph120ph37/mvn</url>
    </repository>
  </repositories>
  ...
  <dependencies>
    <dependency>
      <groupId>com.ameriwether</groupId>
      <artifactId>foo</artifactId>
      <version>1.2.3</version>
      <scope>compile</scope>
    </dependency>
  </dependencies>
  ...
</project>
```
