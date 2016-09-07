#sbt-microsites

## Prerequisites

* [Jekyll](https://jekyllrb.com/):

```bash
gem install jekyll
```

## Install:

Add plugin in `project/plugins.sbt`:
```
addSbtPlugin("com.fortysevendeg"  % "sbt-microsites" % "1.0.1-SNAPSHOT")
```

Enable the plugin in `build.sbt`:
```
enablePlugins(MicrositesPlugin)
```

## Create the microsite

Write markdown documents called `index.md` in `src/tut` like [this one](https://gist.github.com/rafaparadela/9ccfcf1f52c5282c9a5e894b0ddf6508).

Create microsite
```
sbt> microsite
```

Compile:

```
sbt> tut
```

Make site:
```
sbt> makeSite
```

Preview site:
```
sbt> previewSite
```

## Microsite settings

- The name of the microsite is taken from the sbt setting `name`, but you can override it:
```
micrositeName := "Dummy"
```

- The description of the microsite is taken from the sbt setting `description`, but you can override it:
```
micrositeDescription := "This is my Dummy description"
```

- The author of the microsite is taken from the sbt setting `organizationName`, but you can override it:
```
micrositeAuthor := "Rafa Paradela"
```

- The homepage of the microsite is taken from the sbt setting `homepage`, but you can override it:
```
micrositeHomepage := "http://www.mywebpage.com"
```

- In order to add links to GitHub repo, `micrositeGithubOwner` and `micrositeGithubRepo` are required:
```
micrositeGithubOwner := "47deg"
micrositeGithubRepo := "sbt-microsites"
```

- The theme of Highlight.js is [tomorrow](https://highlightjs.org/static/demo/) by default, however you set other theme:
```
micrositeHighlightTheme := "monokai"
```
[Available themes: https://cdnjs.com/libraries/highlight.js/](https://cdnjs.com/libraries/highlight.js/)

- Style uses essentially 8 colors which palette can be set through the setting `micrositePalette` as below:
```
micrositePalette := Map(
        "brand-primary"     -> "#E05236",
        "brand-secondary"   -> "#3F3242",
        "brand-tertiary"    -> "#2D232F",
        "gray-dark"         -> "#453E46",
        "gray"              -> "#837F84",
        "gray-light"        -> "#E3E2E3",
        "gray-lighter"      -> "#F4F3F4",
        "white-color"       -> "#FFFFFF")
```

## Images



