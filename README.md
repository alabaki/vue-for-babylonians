<p align="center"><a href="https://vuejs.org" target="_blank" rel="noopener noreferrer"><img width="100" src="https://vuejs.org/images/logo.png" alt="Vue logo"></a></p>


<h2 align="center">Vue.js for Babylonians</h2>

Vue.js is an MIT-licensed open source project with its ongoing development made possible entirely by the support of these awesome [backers](https://github.com/vuejs/vue/blob/dev/BACKERS.md).

#### What's the difference between this library and VueJs?

Forked from Vue branch of v2.6.11. Library is originally intended for BabylonJs projects but can be applied for any project where reactivity is desired to be optional. Vue automatically injects reactive getters and setters for all Vue variables. Injecting reactive getters and setters on large and fluid objects, e.g. Babylon objects, create significant bloat and causes performance hit on FPS. This library enables developers to prevent reactivity on objects and even specify the object properties that are intended to be reactive.

#### How to install?

Given the dependencies on the Vue runtime from the ecosystem of tools like vue-cli and the Vue compiler, the recommended approach is to npm install into your project with the same package alias with Vue. Please note this library currently only works for Vue v2.6.11.

```
npm i vue@npm:vue-for-babylonians@2.6.11
```

#### How to use?

If you have an object that you do not want Vue to automatically register as reactive and inject reactive getters/setters, then attach a property called '_permittedReactivity'.

 '_permittedReactivity' should hold a list of object property keys that you want to be reactive. All other object property keys will not be reactive. 
 
 ```
let example = {
    foo: 'FOO',
    bar: 'BAR',
    _permittedReactivity: ['foo']   //foo will be reactive. bar will not.
}
```

If your intention is to omit the entire object from becoming reactive, simply attach '_permittedReactivity' to the object as an empty list.

```
let example = {
    foo: 'FOO',
    bar: 'BAR',
    _permittedReactivity: []   //foo and bar will not be reactive.
}
```

If you do not attach '_permittedReactivity' to the object, then Vue will automatically register the entire object and its properties as reactive (just as Vue normally does). 

Please note Vue inject reactive getters/setters the first time it is set as a Vue variable. So you must set the _permittedReactivity property before setting it in Vue for it to take effect. Setting _permittedReactivity after the object is already made into a Vue variable will be ignored.


## License

[MIT](http://opensource.org/licenses/MIT)
