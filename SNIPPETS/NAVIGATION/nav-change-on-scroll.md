# Nav Change On Scroll

Accesible Navigation Structure Example, we can see the parent menu items in the menubar represent a section of a web site and open a submenu containing menu items that link to pages within that section.

> Keyboard navigation should follow this pattern, as they are good
> practices when integrating an accessible menu and it is a great approach.

For situations where the main menu item needs to perform a function, such as linking to a web page, a separate button can be added to the main item to open and close the submenu. This button can also act as a visual indicator of the presence of a submenu. (*This would be the ideal way to do it*).

In the following code we add a button "*The Arrow*" to each top-level menu item with a submenu. When the button is activated with the **keyboard navigation**, it shows or hides the submenu. The button's invisible label is set to "show submenu" or "hide submenu", which reflects the state of the submenu so we can navigate the submenu accessible by keyboard

### Usage:

Import function:

js/components/sidenav.js

```js
import { menuNavigation  } from  "menu-navigation";
```	

 The following code sample may help you as a guide how you could make your JS code accessible:
 1. [Example JavaScript](./nav-change-on-scroll-js.md)

#### HTML Structure

```html
    <header>
        <div>
            <div class="main-header-inner">
                <div class="container">
                    <div class="logo-wrapper">Logo content Here</div>
                    <div class="menu-items-wrapper" id="js-menu">
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

