(For a complete list of all animated properties)[https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animated_properties]

# CSS Transitions

CSS transitions allow us to control the timing of visual state changes. We can control the following four aspects of an element’s transition:

* Which CSS properties transition
* How long a transition lasts
* How much time there is before a transition begins
* How a transition accelerates

Different properties transition in different ways, for example:

* Color values, like color and background-color, will blend to a new color.
* Length values like font-size, width, and height will grow or shrink.

```
a {
  transition-property: background-color;
  transition-duration: 2s;
}
```
```
a {
  display: block;
  width: 300px;
  padding: 31px 5px;
  border-radius: 5px;
  margin: 20% auto;
  background-color: orange;
  text-align: center;
  font-family: Helvetica;
  font-size: 32px;
  color: MintCream;
  transition-property: background-color;
  transition-duration:2s;
}

a:hover {
  background-color: LimeGreen;
}
```
# Duration

To create a simple transition in CSS, we must specify two of the four aspects:

* The property that we want to transition.
* The duration of the transition.

```
a {
  transition-property: color;
  transition-duration: 1s;
}
```

# Delay 
Delay specifies the time to wait before starting the transition. As with the duration property, the default value for transition-delay is 0s, which means no delay.
 
```
transition-property: width;
transition-duration: 750ms;
transition-delay: 250ms;
```

# Timing Function
The timing function describes the pace of the transition.
The default value is ease, which starts the transition slowly, speeds up in the middle, and slows down again at the end.

* Other valid values include:

  * ease-in — starts slow, accelerates quickly, stops abruptly
  * ease-out — begins abruptly, slows down, and ends slowly
  * ease-in-out — starts slow, gets fast in the middle, and ends slowly
  * linear — constant speed throughout
```
transition-property: color;
transition-duration: 1s;
transition-timing-function: ease-out;
```

# Shorthand 

```
transition-property: color;
transition-duration: 1.5s;
transition-timing-function: linear;
transition-delay: 0.5s;

to 

transition: color 1.5s linear 0.5s;


```
 one advantage over the set of separate transition-<property> rules: you can describe unique transitions for multiple properties, and combine them. To combine transitions, add a comma (,) before the semicolon (;) in your rule. After the comma, use the same shorthand syntax
```
#  transitions two properties at once
  
transition: color 1s linear,
font-size 750ms ease-in 100ms;
```


---
It is common to use the same duration, timing function, and delay for multiple properties. When this is the case you can set the transition-property value to all. This will apply the same values to all properties. To effect this, you can use all as a value for transition-property.
```
transition: all 1.5s linear 0.5s;
```

