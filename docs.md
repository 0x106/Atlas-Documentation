# Atlas Documentation

```
<!DOCTYPE html>
<html>

  <head>
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>

    <h1>This heading will be the same on the web and in Atlas</h1>

    <div -data-atlas-myfirstdiv>
      <p>This paragraph will be normal on the web, but styled in Atlas!</p>
    </div>

    <!-- A-Frame components are rendered by default -->
    <a-scene>
      <a-box position="1 -1.5 0" color="#682D63"></a-box>
    </a-scene>

  </body>
</html>
```

```
{
  "-myfirstdiv": {
      "isVisible": "true",
       "position": "(100, 0, 0)",
       "rotation": "(0, 0.7854, 0)",
       "scale": "(0.1, 1, 1.5)",
       "background-color": "(73, 91, 73)",
       "border-top-color": "(34, 73, 73)",
       "border-left-color": "(82, 34, 34, 0.5)",
       "border-right-color": "(41, 82, 82)",
       "border-bottom-color": "(85, 41, 85)",
       "color": "(245, 93, 62)",
       "border-top-width": "2",
       "border-left-width": "2"
       "border-right-width": "2"
       "border-bottom-width": "2"
	},
	"-div02": {
		 "isVisible": "true"
	}
}
```



__isVisible__

- Boolean [true/false]
- Default: true
- Determines whether the element will be rendered
- Can be used to turn _on_ and invisible element or hide elements that you don't want to render in Atlas

__position__

- (x, y, z)
- Default: (0,0,0)
<!-- should this be absolute position? -->
- Determines _offset_ from generic position
<!-- should the units be metres or pixels? -->
- Units:
- Can be Int / Float

__rotation__

- (pitch, yaw, roll)
- Default: (0,0,0)
<!-- should this be absolute position? -->
- Determines _offset_ from generic rotation
- Units: radians

__scale__

- (x, y, z)
- Default: (1.0,1.0,1.0)
- Determines object scale relative to default render
<!-- what are the units of scale -->
- Units: (Float)

__COLORS__

- (r, g, b, a)
- Default: (0, 0, 0, 1.0)
- the alpha channel is optional
- (124, 53, 46) and (0, 255, 0, 0.24) are both valid
- r, g, b is in the range [0-255]
- a is [0,1]

__background-color__<br>
__color__<br>
__border-top-color__<br>
__border-left-color__<br>
__border-right-color__<br>
__border-bottom-color__<br>

__BORDER-<>-WIDTH__

- _width_
- determines the _absolute_ width of the relevant border
- the inner edge of the border will remain in the same position relative to the other edges
- the outer edge will move to accommodate changes in size
<!-- what are the units? -->
- units:











<!--  -->
