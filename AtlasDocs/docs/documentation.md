# Documentation

Any `HTML` component can be styled with as many or as few of the following elements. Most follow their
`CSS` counterparts.

## isVisible

`"isVisible": "<true><false>"`

A boolean used to determine whether this component will be rendered in Atlas. Use
this to hide components that you don't want to be visible - or for components that
you want to force to be rendered.

By default the `body` component of any webpage is not rendered in Atlas. If you
would prefer that it is then set the `isVisible` property to `true` on the `body`.

(Coming soon: please see a full list of the default visibility for various `HTML`
  tags.)

## Geometric Properties

### position

`"position": "(<x>, <y>, <z>)"`

- Default: (0,0,0)
<!-- should this be absolute position? -->
- Determines _offset_ from generic position
<!-- should the units be metres or pixels? -->
- Units:
- Can be Int / Float

### rotation

`"rotation": "(<pitch>, <yaw>, <roll>)"`

- Default: (0,0,0)
<!-- should this be absolute position? -->
- Determines _offset_ from generic rotation
- Units: radians

### scale

`"scale ": "(<x>, <y>, <z>)"`

- Default: (1.0,1.0,1.0)
- Determines object scale relative to default render
<!-- what are the units of scale -->
- Units: (Float)

### pivot

Coming soon.

The position of the node that transformations are applied to. By default this aligns with the
origin of the component (in the center?).

Shifting the pivot allows you to rotate (and translate) a component about any arbitrary point.

### geometry

`"geometry": "<type>"`

Specify alternative geometries for this component.

Examples of the `type` available include:

- `sphere`
- `cube`
- `cyclinder`
- `torus`
- `plane` [default]

### geometry-texture

Coming soon.

Specify an image or texture map to be used as the texture for the component.

## Colors

All colors are specified in the format:

`"<color>": "(<r>, <g>, <b>, <a>?)"`

where `<a>`, the alpha (opacity) component, is optional. The `<r>, <g>, <b>` values
are in the range [0 - 255] and the alpha value is in the range [0.0 - 1.0]

Examples of valid colors are:

- (124, 53, 46)
- (0, 255, 0, 0.24)

Hex values are not yet supported (coming soon).

### color

`"color": "(<r>, <g>, <b>, <a>?)"`

Specifies the color of the main element in a component. Typically this is any
text that appears in the component.

### background-color

`"background-color": "(<r>, <g>, <b>, <a>?)"`

Specifies the color of the background of a component. This will also specify the
color of the geomtry a component is attached to.

For instance if a component is rendered to a sphere, with the `geometry` property,
then the sphere color will be determined by the `background-color` property.

### border-top-color

`"border-top-color": "(<r>, <g>, <b>, <a>?)"`

### border-left-color

`"border-left-color": "(<r>, <g>, <b>, <a>?)"`

### border-right-color

`"border-right-color": "(<r>, <g>, <b>, <a>?)"`

### border-bottom-color

`"border-bottom-color": "(<r>, <g>, <b>, <a>?)"`

## Borders

Changing the `border-<id>-width` property affects the absolute size of the relevant border.
By default the border width will grow from the inside edge outwards. This means that if
the border width is _greater_ than that computed from the `HTML` then the total size of the
component will increase, however the white space (padding) inside the component will remain the same.

Similarly, if the border width is _smaller_ than the original, then the border and the total size
of the component will shrink, but the padding region will remain the same size.

Negative border widths will be set to zero.

### border-top-width

`"border-top-width": "<width>"`

### border-left-width

`"border-left-width": "<width>"`

### border-right-width

`"border-right-width": "<width>"`

### border-bottom-width

`"border-bottom-width": "<width>"`

## Fonts

### font

Coming soon.

### font-size

`"font-size": "<size>"`

### font-weight  

Coming soon.
