# Javascript Example

Using this magic code, we can make the button works! 🪄

```js
const buttonScrollTop = () => {
    const progressWrap = document.querySelector('.progress-wrap');
    const progressPath = progressWrap.querySelector('path');
    if(progressPath) {
        const docHeight = getDocumentHeight();
        const pathLength = progressPath.getTotalLength();
        progressPath.style.transition = progressPath.style.WebkitTransition = 'none';
        progressPath.style.strokeDasharray = pathLength + ' ' + pathLength;
        progressPath.style.strokeDashoffset = pathLength;
        progressPath.getBoundingClientRect();
        progressPath.style.transition = progressPath.style.WebkitTransition = 'stroke-dashoffset 10ms linear';
        
        updateProgress(docHeight, pathLength, progressPath);
        
        window.addEventListener('scroll', () => {
            updateProgress(docHeight, pathLength, progressPath)
        });
        
        const offset = 50;

        window.addEventListener('scroll', (e) => {
            if(window.scrollY > offset) {
                progressWrap.classList.add('active-progress');
            } else {
                progressWrap.classList.remove('active-progress')
            }
        });
    }
}

const updateProgress = (docHeight, pathLength, progressPath) => {
    let scroll = window.scrollY;
    let height = docHeight - window.innerHeight;
    let progress = pathLength - (scroll * pathLength / height);
    if(progress >= 0) {
        progressPath.style.strokeDashoffset = progress;
    }
}

const getDocumentHeight = () => {
    const body = document.body;
    const html = document.documentElement;
    return Math.max(body.scrollHeight, body.offsetHeight, html.clientHeight, html.scrollHeight, html.offsetHeight);
}

export { buttonScrollTop }
```

[Return to Scroll Top](scroll-top.md)