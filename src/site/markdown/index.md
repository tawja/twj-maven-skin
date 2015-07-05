#### [Bootstrap themes from Bootswatch][themes]

[![Bootswatch themes](images/carousel-themes.png)][themes]

Select a free theme for your website from an excellent gallery at [Bootswatch][bootswatch].
Out of the box support for these and other custom [Bootstrap][bootstrap] themes.


#### [Page layouts][twj-layouts]

[![Page layouts](images/carousel-layouts.jpg)][twj-layouts]

Write plain text in Markdown or APT, then set different layouts to your page sections.


#### [Modern skin][twj-misc]

[![Modern skin](images/carousel-components.jpg)][twj-misc]

Tawja Maven Skin uses modern components from Bootstrap and other libraries, upgrades Maven generated
site and provides further enhancements.


#### [New Velocity tools][twj-tools]

[![Velocity tools](images/carousel-tools.png)][twj-tools]

The skin adds a library of new Velocity tools to use in your own Maven template: rewrite HTML code,
support per-page configurations and more!


[bootswatch]: http://bootswatch.com
[bootstrap]: http://getbootstrap.com
[themes]: skin/themes/
[twj-layouts]: skin/layouts.html
[twj-misc]: skin/misc.html
[twj-tools]: tools/


---


## Get it now

To use Tawja Maven Skin in your Maven site, [add it to site.xml][twj-usage]:

```xml
<skin>
  <groupId>org.tawja.maven.skin</groupId>
  <artifactId>twj-maven-skin-base</artifactId>
  <version>1.0.0-SNAPSHOT</version>
</skin>
```

Furthermore, the skin requires accompanying [Tawja Maven Site Tools][twj-tools] (Velocity, ...) as a dependency
as well as Apache Velocity 1.7.
[Add them as dependencies][twj-usage] to `maven-site-plugin`.

[Full usage instructions &raquo;][twj-usage]

[twj-usage]: skin/


## Responsive layouts

Write your pages in [APT or Markdown][doxia-formats], then restructure them using Tawja Maven Skin
[layouts][twj-layouts]:

-   **Carousel** - spinning image slideshow
-   **Thumbnails** - showcase your image gallery
-   **Columns** - multi-column text
-   **Sidebar** - wrap into a sidebar
-   **Body** - text as it has been written

Partition the page into sections using `<hr/>` elements, and define preferred layouts for each section in `site.xml`. Tawja Maven Skin is responsive thanks to [Bootstrap][bootstrap], so the layouts
will be rearranged automatically for readability on small screens.

[Read more about layouts in the documentation &raquo;][twj-layouts]

[doxia-formats]: http://maven.apache.org/doxia/references/index.html


## Themes

The skin theme can be [switched easily][themes]: just select a Bootstrap theme
to give an easy makeover for your Maven site.

-   **Default** - use the default [Bootstrap][bootstrap] theme
-   **Bootswatch** - select an excellent free theme from [Bootswatch][bootswatch]
-   **Custom** - create your own Bootstrap theme with [existing tools][bootstrap-custom]

**Need to change something?** Extend the skin with custom `site.css` file in your project, and
[reuse it for multi-module site][twj-multi].

[How to select a theme &raquo;][themes]

[bootstrap-custom]: http://twitter.github.com/bootstrap/customize.html
[twj-multi]: skin/multi-module.html


## Configure

Tawja is very configurable: many features and components can be disabled, and optional
enhancements enabled using [configuration in `site.xml`][twj-config]:

-   **Table of contents** - display ToC for each page: top bar or sidebar
-   **Menus** - filter Maven menus and select what to display in top or bottom navigation
-   **Code highlight** - syntax colouring for code snippets
-   **Image preview** - display images in pop-ups
-   ... [and more][twj-config]

Check out the [documentation][twj-config] for all the features. Every configuration option
can be applied on a _per-page_ basis!

[twj-config]: skin/config.html


---


## Tawja Maven Skin Tools

Tawja Maven Skin provides custom tools library (especially Velocity) to be used in Maven site template:

-   **`SkinConfigTool`** - convenient access to custom configuration options (global and per-page)
-   **`HtmlTool`** - query and modify HTML text
-   **`URITool`** - use Java URIs in the template

To enable these tools for any skin, add `twj-velocity-tools` dependency to
`maven-site-plugin` in the POM.

[Read more about usage and browse the Javadoc &raquo;][twj-tools]


---


### About

Tawja Maven skin is an [Apache Maven site][mvn-site] skin built on [Bootstrap 3.3][bootstrap].

The code is [open source][twj-github] and licensed under [Apache license][apache-license].
The skin can be used freely for your Maven projects.

[Contribute][contribute] by reporting issues, suggesting new features, or forking the
Git repository on GitHub and adding some good code!

<!--
In the end, if you _really really_ like the skin and want to support the author, I will
be glad to [accept a small donation][donate].
-->

[mvn-site]: http://maven.apache.org/guides/mini/guide-site.html
[apache-license]: http://www.apache.org/licenses/LICENSE-2.0
[contribute]: contribute.html
[twj-github]: http://github.com/tawja/twj-maven-skin/
<!--
[donate]: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&amp;hosted_button_id=?????
-->