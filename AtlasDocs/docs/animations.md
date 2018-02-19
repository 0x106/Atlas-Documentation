# Animations

With Atlas it's easy to add animations to components. Simply define the animation parameters
in your `atlas-style.json` file, alongside any other property definitions.

Atlas currently only supports animations that affect the basic layout and appearance
of components. We will be adding support for more complex behaviour through scripting
in future releases. We are also working on adding support for scenes created in Unity.

## Getting Started with Animations

The following example rotates the component about its y-axis (the vertical axis) by
approximately pi radians, over a period of four seconds. This animation is triggered
if the user taps on the component.

```
// atlas-style.json

"mycomponent" : {
  "onTap": {
    "property": "rotation",
    "command": "changeBy",
    "value": "(0, 3.14, 0)",
    "duration": "4.0"
  }
}
```

Different properties are animated according to the choice of the `property` value, with
the `value` field following the same syntax as the API counterpart.

In this example the key `onTap` indicates that the animation should be triggered when the
user taps the component. Animations can be triggered using one of the following choices:

### onTap

Triggered when the user taps the appropriate component.

### onHover

Triggered when the centre of the users screen intersects with the given component. This
is used to animate components that the user is "looking at".

By default every `text` component has an `onHover` animation attached - which scales the
component by a small amount and temporarily moves it closer to the user.

### onLoad

An animation that is triggered when the scene has finished loading.

### wait <time>

Trigger an animation after a specified time has elapsed. For example:

```
// atlas-style.json

"mycomponent" : {
  "wait 3000": {
    "property": "rotation",
    "command": "changeBy",
    "value": "(0, 3.14, 0)",
    "duration": "4.0"
  }
}
```

This will wait for 30 seconds after the scene has finished loading and then rotate
this component by pi radians about its vertical axis. The `<time>` value is specified
in milliseconds.

## Absolute vs. Relative Animations

The animation `command` field can be either `changeBy` or `setTo`, which define either
a relative animation or an absolute animation, respectively.

Keep in mind that animations which affect the color will linearly interpolate through the
color values between the current and target value.

In the example above the component will rotate by approximately pi radians from its starting position, which
means that if the component is tapped twice, then the component will rotate through
approximately `2 * pi` radians. In contrast, if this animation was specified with
`"command": "setTo"` then the component would perform an initial animation after the
first tap, however any subsequent taps would leave it unchanged.

The duration of the animation is specified in seconds.

<!-- (Coming soon.) By default the animation will be applied to the component that it is
defined within. It is possible however to define an animation relative to a set of nodes,
by listing their key values in an array in the `component` field, like so:

```
"onTap": {
  "component": "[p01, p02, p03]"
``` -->

## Defaults

By default all animations use `"command": "setTo"` with `"duration": "0.0"` (animation is
  instantaneous).

The default `properties` are the same as those specified in the API.


## Scaling

Animations which scale a component apply the same scaling factor in each dimension. This
means that only a single value must be provided. If a vector of values is provided then
the first value will be used for all dimensions.













<!-- END -->
