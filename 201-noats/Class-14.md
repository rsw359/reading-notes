# CSS Transformations and Animations

## Transform

- There are 2 settings for the transform property in Css, 2d and 3d, each with their own properties and values
- The syntax is not complicated: sample taken from <https://learn.shayhowe.com/advanced-html-css/css-transforms/>

  ```div {
  -webkit-transform: scale(1.5);
     -moz-transform: scale(1.5);
       -o-transform: scale(1.5);
          transform: scale(1.5);

}```

- Browser support may be sketchy, so vendor prefixes are used, with the unprefixed value capable of overwriting the others
- Two dimensional transforms work on x,y axis, while three dimensional transforms add the additional -z- axis
- 2D rotate property  accepts values of 0 to 360, employing positive numbers for clockwise rotation and negative values for counter-clockwise
- 2d scale property allows for the appearance of size to modified, with a default value of 1. Values below one appear smaller and values above one appear larger
- Additional properties include:
  - Skew
  - Translate
  - Transform-Origin
  - Perspective
  - Perspective Depth
  - Perspective Origin

## Transitions and Animations

There are four  properties related to transition

- Transition-property - specifies which properties will be altered by transitional properties (not all properties can be transitioned)
- Transition-duration - timing values for the duration of the transition
- Transition-timing-function - transition speed
- Transition-delay - sets a delay for transitions to occur

## Animations

Animations allow for more control than transitions

- To set multiple points of transition, the @keyframes property is used
- Animation duration, timing, and delay can all be set using specific properties
- Animation styling and direction can also be customized

### Other Stuff

- A few cool transitions to use to spice up the UI:
  - .fade
  - .color:hover
  - .grow:hover
  - .shrink:hover
  - .rotate:hover
  - .circle:hover (change border-radius)
