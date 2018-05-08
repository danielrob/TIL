## 8th
##### You muppet... eslint no-use-before-define 
Can be quite easily set to `["error", { "functions": true, "classes": true }]`, so it's absolutely fine for a const to be declared below a function that is consumed in that function... how had I ruled that out? 

##### Stop using google, use npm directly
It's surprising how I'd assumed searching google would get me the npm results I wanted. Nope. Use npm more. 

##### Text inputs are harder than they look in react...
Especially if you want to change a value in the onChange. React then thows an `¯\_(ツ)_/¯` about where to put the cursor cause it's like "you changed it (wo)man". I couldn't actually figure this out and threw a sadface... I'd always get cursor jumping on the old `element.setSelectionRange(pos, pos)` with react with a 32ms render. I'll have to read libraries like `react-input-enhancements` more closely or just create custom text masks from `text-mask` but that's a heavy solution. 

## 3rd

###### `Object.defineProperty`
Is like a single property proxy, allowing you to intercept a property get _with context_. That last part helped me out of a [pickle](https://stackoverflow.com/questions/50150554/add-function-to-constructor-prototype-with-method-with-access-to-this-from-const/50151472#50151472). 

###### `choose your drag and drop`
Litmus test: do you want a drag preview? If you just want to move something, this is probably better: 
```
element.addEventListener('mousedown', mouseDownHandler)

mouseDownHandler = () => {
 document.addEventListener('mouseover', mouseOverHandler)
 document.addEventListener('mouseup', mouseUpHandler)
}

mouseUpHandler = () => {
 document.removeEventListener('mouseover', mouseOverHandler)
 document.removeEventListener('mouseup', mouseUpHandler)
}

mouseOverHandler = ({ clientX, clientY }) => {
   console.log(`mouse position: (${clientX}, ${clientY})`)
}
```
Also: [clientX & clientY & drag events in Firefox not gonna happen](https://twitter.com/dan_abramov/status/529048892189724673)

###### bits and bobs
- `String.repeat(n)` is handy and `'\u00A0'` is a space  
- You can steal text from a page by selecting all of it copying the highlight and deselecting. `user-select` property. Draggable elements have it as `none` by default. 
-  [wow, a css painting recreation](http://diana-adrianne.com/purecss-francine/)

###### a good icon lib: [ionicons](http://ionicons.com/)

## May

### 23rd

###### wtf... js proxies... 
They allow you intercept object.key accesses and perform actions! [ES2015 Proxies](https://developers.google.com/web/updates/2016/02/es2015-proxies)

### 22nd

###### today I created: 
[styled-as-components](https://www.npmjs.com/package/styled-as-components) I had to remind myself of a bit of prototype / inheritance features of javascript which in this case was useful to avoid loops inside a factory function. 

Thanks to [this medium](https://medium.com/@BrodaNoel/how-to-create-a-react-component-and-publish-it-in-npm-668ad7d363ce) for how to publish. 

### 21st 

###### devtools has a colorpicker 
[(tweet)](https://twitter.com/danztweet/status/987602024597409797)

###### the lodash of styled-components
[polished](https://polished.js.org/)

###### React components: 
- [a set of color picker components](https://github.com/casesandberg/react-color/)
- [gmail style popover](https://github.com/sasha240100/react-rectangle-popup-menu)

###### `fetch` accepts `FormData` objects as the body... very nice, even though `FormData` objects are non iterable and somewhat awful in that regard :D. 
https://medium.com/@everdimension/how-to-handle-forms-with-just-react-ac066c48bd4f

###### TIR:
- https://medium.com/@albinotonnina/magic-hat-technique-408a3fa590bb  
- https://medium.com/ux-in-motion/creating-usability-with-motion-the-ux-in-motion-manifesto-a87a4584ddc
- https://hackernoon.com/making-of-a-component-library-for-react-e6421ea4e6c7
- https://medium.freecodecamp.org/every-developer-should-have-a-blog-heres-why-and-how-to-stick-with-it-5fd55a247fbf


## April

# 2018
