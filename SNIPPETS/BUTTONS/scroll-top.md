# Scroll Top

Button used to go up to the top of the page, once you have scrolled down at a certain point it will appear, the code is made accessible.

### Usage:

he HTML structure is composed by these main elements:

 1. `.button-scroll` Button Container.
 2. `<a href="#main-header">` the tag `<header>` used for navigation, a `.main-header` class will be added to it, unless you already have a class assigned the href will be redirected there.
 3. `sr-only`Used for accessibility.
 4. `<svg>` In case the design contains an arrow.

#### Javascript

Import function:
```import { buttonScrollTop } from './modules/button-scroll';```

  

The following code sample may help you as a guide how you could make your JS code:

1. [JavaScript Example](scroll-top-js.md)

  
#### Get Styles ```/main.scss;```

  

`sr-only` CSS class, Visually hidden but screen readers can get into it.
```css
.sr-only {
	position: absolute;
	left: -10000px;
	top: auto;
	width: 1px;
	height: 1px;
	overflow: hidden;
}
```

  

#### HTML Structure
```html
<div  class="button-scroll">
	<a  href="#main-header">
		<span  class="sr-only">Jump to top of page</span>
		<svg aria-hidden="true"
			focusable="false"
			class="progress-circle svg-content"
			width="100%"
			height="100%"
			viewBox="-1 -1 102 102">
			<path  d="M50,1 a49,49 0 0,1 0,98 a49,49 0 0,1 0,-98"/>
		</svg>
	</a>
</div>
```


**Example:**

<table>
  <tr>
    <th align="center">📱 This is the Result on Mobile</th>
	<th align="center">🖥  This is the Result on Desktop</th>
  </tr>
  <tr>
    <td align="center"><img src="https://imgur.com/hGJAhim.jpg" height="250" alt="Accessible Nav Mobile"></td>
	<td align="center"><img src="https://imgur.com/I3B8rE6.jpg" height="250" alt="Development Accessible Nav Desktop"></td>
  </tr>
</table>

  
 
[Return to Black Magic Development Guidelines](../../README.md)