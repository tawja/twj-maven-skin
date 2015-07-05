# [Tawja Maven skin]( http://www.tawja.org/project/doc/maven/skins/ )

[![Build Status](https://travis-ci.org/tawja/twj-maven-skin.svg?branch=master)](https://travis-ci.org/tawja/twj-maven-skin)

Tawja Maven Skin is an Apache Maven site skin built on [Bootstrap 3.3][bootstrap]. It allows various structural
and stylistic customizations to create a modern-looking Maven-generated website.

To get started and see how the skin looks by default, check out
http://www.tawja.org/project/doc/maven/skins/!

[bootstrap]: http://getbootstrap.com

## Status : WORK IN PROGESS - Stable and functionnal, but issues to resolve before 1.0.0

## Usage

To use this Maven skin, include it in your `site.xml` file:

```xml
<project>
  ...
  <skin>
    <groupId>org.tawja.maven.skin</groupId>
    <artifactId>twj-maven-skin-base</artifactId>
    <version>1.0.0</version>
  </skin>
  ...
</project>
```

The skin requires accompanying Tawja Maven Skin Tools Velocity (`twj-velocity-tools`) to be available when
generating Maven site. Add them as a dependency to `maven-site-plugin` in your POM file:

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
            <artifactId>twj-maven-skin-base</artifactId>
            <version>1.0.0</version>
        </dependency>
        <!-- Tawja Maven Skin requires Velocity >= 1.7  -->
        <dependency>
          <groupId>org.apache.velocity</groupId>
          <artifactId>velocity</artifactId>
          <version>1.7</version>
        </dependency>
        ...
      </dependencies>
      ...
    </plugin>
    ...
  </plugins>
</build>
```

Note that _Apache Velocity 1.7_ is also required by the template.

The skin is provided on the "works on my computer" basis at the moment. I am using the newest
versions of `maven-site-plugin` and other components and at the moment do not have any feedback
on using the skin with Maven 2 site or other configurations.


### Configuration

The skin is configurable using the `<custom><twjSkin>` element in your `site.xml` file.
Refer to [documentation][twj-config] for all configuration options.

[twj-config]: http://www.tawja.org/project/doc/maven/skins/config.html

A sample configuration file is given below:

```xml
<project>
  ...
  <custom>
    <twjSkin>
      <theme>bootswatch-spacelab</theme>
      <brand>
        <name>My Project</name>
        <href>http://www.tawja.org/project/doc/maven/skins/</href>
      </brand>
      <slogan>Super interesting project doing good things.</slogan>
      <titleTemplate>%2$s | %1$s</titleTemplate>
      <toc>top</toc>
      <topNav>Download|reports</topNav>
      <bottomNav>
        <column>Main|Download</column>
        <column>Documentation</column>
        <column>reports|modules</column>
      </bottomNav>
      <bottomDescription>This is a very good project doing interesting
        and valuable things.</bottomDescription>
      <pages>
        <index project="project-id">
          <shortTitle>Welcome</shortTitle>
          <breadcrumbs>false</breadcrumbs>
          <toc>false</toc>
          <sections>
            <carousel />
            <body />
            <sidebar />
            <thumbs>2</thumbs>
            <columns>3</columns>
          </sections>
        </index>
        <developer-info>
          <toc>sidebar</toc>
        </developer-info>
      </pages>
    </twjSkin>
  </custom>
  ...
</project>
```



## Bug tracker

Have a bug or a feature request? Please create an issue here on GitHub that conforms with
[necolas's guidelines](http://github.com/necolas/issue-guidelines).

http://github.com/tawja/twj-maven-skins/issues


## Contributing

Fork the repository and submit pull requests.


## Authors

**Jaafar BENNANI-SMIRES**

+ http://www.tawja.org
+ http://github.com/tawja

**Marek ROMANOWSKI (previous repository)**

+ http://blog.matsuo.pl
+ http://github.com/tunguski

**Andrius VELYKIS(previous repository)**

+ http://andrius.velykis.lt
+ http://github.com/andriusvelykis

## Copyright and license

Copyright 2015 Tawja

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this work except in compliance with the License.
You may obtain a copy of the License in the LICENSE file, or at:

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
