# Models

Coming soon.

## Introduction

Atlas supports adding 3D models to your scene, using the following formats:

- `.dae`
- `.scn`

To use a model in your scene it needs to be uploaded to the Atlas Cloud.

Models are specified in your HTML using the usual Atlas syntax:

```
<div -data-atlas-mymodelid></div>
```

with the following information specified in your `atlas-style.json` file:

```
{
  "mymodelid": {
    "filename": "<filename>"
  }
}
```

If your model, e.g. called _aeroplane.dae_ is hosted on the Atlas Cloud, then `atlas-style.json` would
include:

```
{
  "mymodelid": {
    "filename": "aeroplane"
  }
}
```

As always, `mymodelid` can be set to anything you choose, just remember to include `-data-atlas-`.
All of the existing API properties are available to style the components that models are attached to.
This means that models can be used as links, for example using `<a href="google.co.nz" -data-atlas-mymodelid></a>`

Note that the file extension does not need to be specified in your `atlas-style.json` file - since all the
assets that are necessary for a specific model (such as textures and geometry files) will be placed
into a folder. All the files in this folder will be retrieved when the scene is loaded.

## Positioning

By default, any models will be positioned in the scene according to where they would
be if it was a regular element on your webpage. This makes it easy to attach models to any
HTML tag, and have it behave as if it was an ordinary element.

If your model is not attached to any existing components then you can add it to an empty
`div`. This will create a component of size 1284 pixels (millimetres) wide, and one pixel (1mm) high.

Your model will be positioned in the centre of this component - however you can move it using the `position`
attribute in its specification. As a simple example, the left hand edge of the models bounding box can be
positioned at the pseudo left hand edge of the page by setting its `x` value to: `<model-width> - 624`, based
on the actual width of your model.

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
