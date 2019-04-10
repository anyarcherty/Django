JS 

1. keypress vs keyup

    `keypress events` are fired `before` the `new character` is added to the value of the element (so the first keypress event is fired before the first character is added, while the value is still empty). 
    
    `keyup events` are fired after the character has been added.

2. numeric variable

    Char code :

    `48-57` equal to 0, 1, 2, 3, 4, 5, 6, 7, 8, 9

    `0` is Backspace(otherwise need refresh page on Firefox)

    `46` is dot
  
    && is AND , || is OR operator.

3. url herf
    
    ```
    var url = document.createElement('a');
    url.href = 'https://developer.mozilla.org/en-US/search?q=URL#search-results-close-container';
    console.log(url.href); // https://developer.mozilla.org/en-US/search?q=URL#search-results-close-container
    console.log(url.protocol); // https:
    console.log(url.host); // developer.mozilla.org
    console.log(url.hostname); // developer.mozilla.org
    console.log(url.port); // (blank - https assumes port 443)
    console.log(url.pathname); // /en-US/search
    console.log(url.search); // ?q=URL
    console.log(url.hash); // #search-results-close-container
    console.log(url.origin); // https://developer.mozilla.org
    ```
    
4. update url link without pageloading
    
    
    `window.history.pushState("", "", window.location.pathname)`
