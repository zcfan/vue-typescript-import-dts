# NOTICE
This is the esModule version of [locoslab/vue-typescript-import-dts](https://github.com/locoslab/vue-typescript-import-dts)

I meet some trouble to serve two modules definition with same name in one module, so if you know what's I am talking about... Send a PR to the original repo please.

Use this if you set the `esModule` option of vue-loader to `true`, or else check the link above.

## Usage

1. Install: `npm install zcfan/vue-typescript-import-dts --save-dev`

2. Either include it in the `types` field of your `tsconfig.json`

```javascript
{
    "compilerOptions": {
        "types": ["vue-typescript-import-dts"],
...
```

or explicitly in a TypeScript source file

```typescript
/// <reference path="PATH/TO/node_modules/vue-typescript-import-dts/index.d.ts"/>
```

Then, it is possible to `import` a `*.vue` file

```js
import Child from './child.vue'
```

Note: TypeScript will not type check, parse, or even verify the existence of the `.vue` file: this project only instructs the TypeScript compiler to assume the import of 'something' that ends with `.vue` succeeds and is a `Vue.ComponentOptions<Vue>` object.

## Shameless Plug
If you are using TypeScript 2.0 together with Vue.js 2.0, you might also be interested in
* [vue-typescript-component](https://github.com/locoslab/vue-typescript-component) to use TypeScript classes as Vue.js components
* [vue-typescript-jest](https://github.com/locoslab/vue-typescript-jest) to test Vue.js components and TypeScript sources using Jest
* [vue-jest-utils](https://github.com/locoslab/vue-jest-utils) to simplify snapshot testing of Vue.js components using Jest and html2jade
* [vue-typescript-component-example](https://github.com/locoslab/vue-typescript-component-example) as an example for this package and the projects above that shows a TypeScript/Tsify/Vue.js/Vueify/Pug setup supporting Hot Module Replacement and unit/snapshot testing with Jest


## License
[MIT](http://opensource.org/licenses/MIT)
