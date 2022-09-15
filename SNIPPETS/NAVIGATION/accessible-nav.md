# Accessible Nav

Accesible Navigation Structure Example, we can see the parent menu items in the menubar represent a section of a web site and open a submenu containing menu items that link to pages within that section.

> Keyboard navigation should follow this pattern, as they are good
> practices when integrating an accessible menu and it is a great approach.

For situations where the main menu item needs to perform a function, such as linking to a web page, a separate button can be added to the main item to open and close the submenu. This button can also act as a visual indicator of the presence of a submenu. (*This would be the ideal way to do it*).

In the following code we add a button "*The Arrow*" to each top-level menu item with a submenu. When the button is activated with the **keyboard navigation**, it shows or hides the submenu. The button's invisible label is set to "show submenu" or "hide submenu", which reflects the state of the submenu so we can navigate the submenu accessible by keyboard

### Usage:

The HTML structure is composed by these main elements:

 1. `<header>`  is the main navigation content.
 2. `main-header-inner` contains the last `container`,  inside this last container we have two principal `<div>`: 
	 -  **1.** `logo-wrapper` there will be the logo resource.
	 -  **2.** `menu-items-wrapper` this is the `nav` container, which holds a unordered list with list items. Inside each `<li>` we found a list with two principal `<div>`:
		 -  the first is `cta-expandible` there we gotta our top level menu items with the main actionable anchor followed by an accessible button that will appear when the header is navigated using the keyboard.
		 - the second `<div>` is `list-sub-items` in this container we have the internal sub items which will be visible when hovered or when the accessible button in `cta-expandible`.
	-  **3.** The `<li>` structure is repeated according to the number of items in the header.

#### Javascript

Import function:

js/components/sidenav.js

```js
import { menuNavigation  } from  "menu-navigation";
```	

 The following code sample may help you as a guide how you could make your JS code accessible:
 1. [JavaScript Example](./accessible-nav-js.md)


#### Get Styles ```/main.scss```:

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
    <header>
        <div>
            <div class="main-header-inner">
                <div class="container">
                    <div class="logo-wrapper">Logo content Here</div>
                    <div class="menu-items-wrapper">
                        <nav>
                            <ul>
                                <li>
                                    <div class="cta-expandible">
                                        <a href="#">Top Level Menu Item</a>
                                        <button>
                                            <span class="sr-only">Click to open dropdown and see the links inside it.</span>
                                        </button>
                                    </div>
                                    <div class="list-sub-items">
                                        <div class="container">
                                            <ul>
                                                <li>
                                                    <a href="#">
                                                        <span>Sub Item Here</span>
                                                        <span class="arrow"></span>
                                                    </a>
                                                </li>
                                            </ul>
                                        </div>
                                    </div>
                                </li>
                                <li>
                                    <!-- Continues the same structure of the previous LI -->
                                    <div></div>
                                    <div></div>
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </div>
        </div>
    </header>
```

**Example:**

<table>
  <tr>
    <th align="center">📱 This is the Result on Mobile</th>
	<th align="center">🖥  This is the Result of the development</th>
	<th align="center">🖥 This is Result on Desktop with keyboard navigation</th>
  </tr>
  <tr>
    <td align="center"><img src="https://imgur.com/uO799of.jpg" height="250" alt="Accessible Nav Mobile"></td>
	<td align="center"><img src="https://imgur.com/RYmb28s.jpg" height="250" alt="Development Accessible Nav Desktop"></td>
	<td align="center"><img src="https://imgur.com/OQJ8LdO.jpg" height="250" alt="Desktop With Keyboard Navigation"></td>
  </tr>
</table>


[Return to Black Magic Development Guidelines](../../README.md)