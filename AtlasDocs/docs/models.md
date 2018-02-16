# Models

Coming soon.

## Introduction

Atlas supports adding 3D models to your scene, using the following formats:

- `.dae`
- `.scn`

To add a model you can either add it to a CDN and ensure that it is publicly available, or
you add it to the Atlas Cloud - which makes it private by default.

Models are specified in `HTML` using the following syntax:

```
<div -data-atlas-mymodelid></div>
```

with the following information specified in your `atlas-style.json` file:

```
{
  "mymodelid": {
    "url": "<cloud-storage-url>"
    "filename": "<filename>"
  }
}
```

Only one of `url` or `filename` needs to be specified, depending on where your model
is hosted. If your model, e.g. called _aeroplane.dae_ is hosted on the Atlas Cloud, then `atlas-style.json` would
include:


```
{
  "mymodelid": {
    "filename": "aeroplane.dae"
  }
}
```

As always, `mymodelid` can be set to anything you choose, just remember to include `-data-atlas-`.
All of the existing API properties are available to style the components that models are attached to.
This means that models can be used as links, for example using `<a href="google.co.nz" -data-atlas-mymodelid></a>`

## Positioning

By default, any models will be positioned in the scene according to where they would
be if it was a regular element on your webpage. This makes it easy to attach models to any
HTML tag, and have it behave as if it was an ordinary element.

<!-- The easiest way to position a model in the scene is to attach it to an existing HTML component,
and then adjust its `position` value.

Consider the following scene:

```
// index.html

<html>
  <head>
    <atlas id="atlas-style"></atlas>
  </head>

  <body>

    <h1>This heading will be the same on the web and in Atlas</h1>

    <p -data-atlas-mycomponent>
      This paragraph will be normal on the web, but styled in Atlas!
    </p>

  </body>
</html>
```

In `atlas-style.json` we would include the following specifications:

```
// atlas-style.json

{
  "mycomponent": {

       "rotation": "(0, 0.7854, 0)",
       "background-color": "(73, 91, 73)",
       "scale": "(4.0, 4.0, 1.0)"
       "filename":"aeroplane.dae"
  }
}
``` -->















<!-- END -->
