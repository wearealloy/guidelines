
# Javascript Example

With the ```getDevice(``` function we can get the curren device type. 📱 💻 🖥 

```js
const getDevice = () => {
    const ua = navigator.userAgent;
    if (
        /(tablet|ipad|playbook|silk)|(android(?!.*mobi))/i.test(ua) ||
        (window.matchMedia('only screen and (min-width: 768px)').matches &&
            window.matchMedia('only screen and (max-width: 1279px)').matches)
    ) {
        return 'tablet';
    } else if (
        /Mobile|Android|iP(hone|od)|IEMobile|BlackBerry|Kindle|Silk-Accelerated|(hpw|web)OS|Opera M(obi|ini)/.test(
            ua,
        ) ||
        window.matchMedia('only screen and (max-width: 767px)').matches
    ) {
        return 'mobile';
    }
    return 'desktop';
};

```

Using this magic code, we can make the accessibility works! 🪄

```js
const menuNavigation = () => {
    const deviceType = getDevice();
    if (deviceType === 'desktop') {        
        const header = document.querySelector('header.header');
        const listItems = header.querySelectorAll('.menu-items-wrapper nav > ul > li');
        if(listItems.length > 0){
            const listButtons = header.querySelectorAll('.menu-items-wrapper nav > ul > li .cta-expandible button');
            const logo = header.querySelector('.logo-wrapper a');
    
            const searchButton = header.querySelector('.search-form button');
            searchButton.addEventListener('focusout',() => {
                listButtons.forEach((buttonItem) => {
                    buttonItem.classList.remove('is-visible');
                })
                listItems.forEach((list) => {
                    list.classList.remove('expanded');
                })
            })

            logo.addEventListener('focus',() => {
                listButtons.forEach((buttonItem) => {
                    buttonItem.classList.remove('is-visible');
                })
                listItems.forEach((list) => {
                    list.classList.remove('expanded');
                })
            })
            listItems.forEach((listItem, index) => {
                const anchor = listItem.querySelector('.cta-expandible a');
                const button = listItem.querySelector('.cta-expandible button');
                if(anchor && button){
                    anchor.addEventListener('focus', (e) => {
                        if(typeof anchor.dataset.focusVisibleAdded === 'string') {
                            listButtons.forEach((buttonItem) => {
                                buttonItem.classList.remove('is-visible');
                            })
                            button.classList.add('is-visible');    
                            listItems.forEach((list) => {
                                list.classList.remove('expanded');
                            })
                        }
                    })
                    button.addEventListener('focusout',() => {
                        button.classList.remove('is-visible');
                    })
                    button.addEventListener('keypress',(e) => {
                        if(e.key === 'Enter'){
                            if(listItem.classList.contains('expanded')){
                                listItem.classList.remove('expanded');
                            } else {
                                listItem.classList.add('expanded');
                            }
                        }
                    })
                }
            })
            document.addEventListener('keydown', function(event){
                if(event.key === "Escape"){
                    listItems.forEach((list) => {
                        list.classList.remove('expanded');
                    })
                }
            });
        } 
    }
}

```

[Return to Accessible Nav](accessible-nav.md)