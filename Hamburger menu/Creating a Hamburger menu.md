Hamburger menus are used to toggle the mobile menu of the website

- We'll need to create a few files; index.html, styles.css, & app.js.
- Add the boiler plate and create the nav menu

### The HTML
```html
<nav>
        <div class="nav-menu">
            <a href="">
               <ul>
                    <li>Home</li>
                    <li>About</li>
                    <li>Service</li>
                   <li>Contact</li>
                </ul>
            </a>
        </div>
        <div class="hamburger-menu">
            <div class="ham-bar bar-top"></div>

            <div class="ham-bar bar-mid"></div>

            <div class="ham-bar bar-bot"></div>
       </div>
    </nav>
```

### CSS
Link the CSS
but first the CSS resets

```css
/* CSS RESET */

*,
*::before,
*::after {

  box-sizing: border-box;
}

body,h1,h2,h3,h4,p,figure,blockquote,dl,dd {
  margin: 0;
}

ul[role='list'],
ol[role='list'] {
  list-style: none;
}

html:focus-within {
    scroll-behavior: smooth;
  }  
body {
    min-height: 100vh;
    text-rendering: optimizeSpeed;
   line-height: 1.5;
}

a:not([class]) {
    text-decoration-skip-ink: auto;
 }

  input,  button, textarea, select {
    font: inherit;
 }
  
 @media (prefers-reduced-motion: reduce) {
  html:focus-within {
   scroll-behavior: auto;
  }

 *,
 *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  } 
ul {
    padding: 0;
    margin: 0;
}  
li {
    list-style: none;
}  
a {
    text-decoration: none;
}
```

Main Css

```css
body {
    font-family: monospace;
    font-size: 1.5rem;
}
  
nav {
    padding: 1rem;
    height: 3rem;
    background-color: #f1f1f1;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: flex-end;
}
  
.nav-menu {
   position: absolute;
   right: 1rem;
   top:3rem;
   background-color: #f1f1f1;
   padding: 1rem;
   text-align: left;
   transform: translateY(-100%) ;
   z-index: -1;	 
   transition: all 300ms ease-in-out;
}

.nav-menu.active{
    display: block;
    transform: translateY(0%);
}
```

### Hamburger styling

```css
.hamburger-menu {
    height: 50px;
    width: 50px;
    position: relative;
    cursor: pointer;
    padding: 1rem;
   }
  
.ham-bar {
    width: 70%;
    height: 4px;
    background-color: black;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
   transition: transform .3s, opacity .5s, top .3s;
}
  
.bar-top {
    top: 25%;
    transform: translate(-50%, -50%);
   }  
.bar-bot {
    top: 75%;
   }
```

When the hamburger menu has a class of `active`, we'll want to style the `<div class="ham-bar"></div>` appropriately. Lets do that now.

For `bar-top` we want to center it and rotate it:

### JavaScript
The JavaScript is very simple, we'll just want to add an event listener on <div class="hamburger-menu"></div>. We can create a variable for this as well:

All we want to do when this event is triggered, is toggle a class of active to <div class="hamburger-menu"></div>

```js
const hamMenu = document.querySelector('.hamburger-menu'); hamMenu.addEventListener('click', () => { 
	hamMenu.classList.toggle('active');
});
```

![Not Activated](https://github.com/Shubham-yelekar/What-I-ve-Learned/blob/master/Hamburger%20menu/assets/Not%20Activated.png)


## Activated

![Activatedd List](https://github.com/Shubham-yelekar/What-I-ve-Learned/blob/master/Hamburger%20menu/assets/Activated.png)

