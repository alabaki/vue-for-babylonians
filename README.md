<p align="center"><a href="https://vuejs.org" target="_blank" rel="noopener noreferrer"><img width="100" src="https://vuejs.org/images/logo.png" alt="Vue logo"></a></p>


<h2 align="center">Vue.js for Babylonians</h2>

Vue.js is an MIT-licensed open source project with its ongoing development made possible entirely by the support of these awesome [backers](https://github.com/vuejs/vue/blob/dev/BACKERS.md).

#### What's the difference between this library and VueJs?

Forked from Vue branch of v2.6.11. Library is configured for BabylonJs projects. The current implementation of Vue automatically injects reactive getters and setters for all Vue variables. Injecting reactive getters and setters on Babylon objects create significant bloat and causes performance hit on FPS. This library prevents all Babylon objects from being set with reactive setters/getters.

#### How to use?

Given the dependencies on the Vue runtime from the ecosystem of tools like vue-cli and the Vue compiler, the recommended approach is to npm install into your project with the same package alias with Vue. 

'''
npm i vue@npm:vue-for-babylonians@2.6.1-1.0
'''

## License

[MIT](http://opensource.org/licenses/MIT)
