In Black Magic we do animations from another planet, we work with [Gsap](https://github.com/greensock/GSAP), [LottieFiles](https://lottiefiles.com/), [Three.js](https://threejs.org/), [After Effects](https://www.adobe.com/mx/products/aftereffects.html), with these visual effects animations we make the web pages more dynamic and not only that we try that despite the animations the web page has a fast performance.

- [Good Practices Making Animations.](#good-practices-making-animations)
- [Bonus Tips.](#bonus-tips)
- [Useful Links.](#useful-links)

## Good Practices Making Animations.
In many occasions that we work with animations there are things that we are discovering along the way, or there are ways to implement them that in the documentation little is talked about because it is taken for granted that the developers know it and as progammers sometimes we do not know about it, It is known that animations can alter the accessibility or performance of the website, to avoid this we leave here some good practices that can be very useful when you start creating animations on your website:

- How to create [high-performance CSS animations.](https://web.dev/animations-guide/#layout)

- Examples of [high-performance CSS animations.](https://web.dev/animations-examples/)

- Animating the height of an html element is not a good idea because you put the browser to recalculate the viewport and if you are doing a lot of animation based on height or width you will have performance problems.

- If you need to hide elements, you usually use the opacity and visibility properties instead of using the display property (since it's a non-animatable property: [Properties that can be animated](https://developer.mozilla.org/es/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions#propiedades_que_pueden_ser_animadas)).

- Avoid animating many properties at the same time.

## Bonus Tips.
Respecting user preferences is key for modern websites, there are users who prefer a site with animations and on the other hand there are users who prefer to remove them as it can be a bit annoying for them. For these cases we have `prefers-reduced-motion` which allows you to design a variant of your site with reduced motion for users who have opted for this preference.


 - [Detailed explanation of the use of prefers-reduced-motion.](https://web.dev/prefers-reduced-motion/)

## Useful Links.

 - Gsap Animation Showcase. Link 👉🏻 [Here](https://greensock.com/showcase/).
 - Animations and performance. Link 👉🏻 [Here](https://web.dev/animations-and-performance/).
 - Why are some animations slow? Link 👉🏻 [Here](https://web.dev/animations-overview/).
 - Inspect and modify animations with the Chrome DevTools Animation Inspector. Link 👉🏻 [Here](https://developer.chrome.com/docs/devtools/css/animations/).
 - Web Animations API. Link 👉🏻 [Here](https://developer.mozilla.org/en-US/docs/Web/API/Web_Animations_API/Using_the_Web_Animations_API#meet_the_web_animations_api).


[Return](../README.md)
