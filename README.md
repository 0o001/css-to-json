# css-to-json
Convert a CSS file JSON or whatever you want

```css
:root {
    --title:My HTML Title;
    --html: {
        <title>var(--title)</title>
    };
    
    --my-json-title:"My JSON Title";
    --my-json: {
        "message": "hello",
        "title": var(--my-json-title),
        "items": [
            1,
            2,
            true
        ]
    };
}
```

```js
let root = document.querySelector(':root');

let html = getComputedStyle(root).getPropertyValue('--html');
let json = getComputedStyle(root).getPropertyValue('--my-json');
        
console.log(html);
console.log(JSON.parse(json));
```
