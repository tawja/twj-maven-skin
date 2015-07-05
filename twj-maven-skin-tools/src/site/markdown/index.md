# Tawja Maven Skin Tools (Velocity, ...)

Tawja Maven Skin provides custom tools for [Apache Velocity][velocity] to be used in Maven site
template. These objects are contributed to Velocity context and can be used within the template.
Refer to [Javadoc][javadoc-all] for each tool for more information.

-   **[`SkinConfigTool`][javadoc-config]** (key **$config**)

    Provides a uniform access to Maven site custom configuration options. Supports global and
    per-page configuration. See info on [_per-page configuration_][per-page-info] in Tawja Maven Skin
    for an example of features it brings.
-   **[`HtmlTool`][javadoc-html]** (key **$htmlTool**)

    Provides methods to modify and query HTML text using [jsoup][jsoup] library.
-   **[`URITool`][javadoc-uri]** (key **$uriTool**)

    Provides URI utilities that expose URIs to the template.

[velocity]: http://velocity.apache.org/
[per-page-info]: ../skin/config.html#Per-page_configuration
[jsoup]: http://jsoup.org/

[javadoc-all]: apidocs/
[javadoc-config]: apidocs/org/tawja/maven/skins/twj/SkinConfigTool.html
[javadoc-html]: apidocs/org/tawja/maven/skins/twj/HtmlTool.html
[javadoc-uri]: apidocs/org/tawja/maven/skins/twj/URITool.html


## Usage

To enable these tools, add `twj-velocity-tools` dependency to `maven-site-plugin` in the POM
file:

```xml
<build>
  <plugins>
    ...
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-site-plugin</artifactId>
      <version>3.3</version>
      <dependencies>
        ...
        <dependency>
            <groupId>org.tawja.maven.skin</groupId>
            <artifactId>twj-maven-skins-tools</artifactId>
            <version>1.0.0</version>
        </dependency>
        ...
      </dependencies>
      ...
    </plugin>
    ...
  </plugins>
</build>
```
