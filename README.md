# Explaining

## DEV
Run `npm run dev -- -o` causes a 500 error in the browser and invoke the unability to provide the view (nothing more):

```shell
500

location is not defined

at new me (./node_modules/@epicgames-ps/lib-pixelstreamingfrontend-ue5.2/dist/lib-pixelstreamingfrontend.js:1:19505)
at Proxy.created (./app.js:12:9)
at callWithErrorHandling (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:156:32)
at callWithAsyncErrorHandling (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:164:17)
at callHook (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:3501:3)
at applyOptions (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:3419:5)
at finishComponentSetup (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:7295:5)
at handleSetupResult (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:7247:3)
at setupStatefulComponent (./node_modules/@vue/runtime-core/dist/runtime-core.cjs.js:7216:7)
```

## BUILD
Run `npm run build && npm run preview` causes a 500 error in the browser (with no explanation) whereas in preview console, there's a hint on what is going on:

```js
[nuxt] [request error] [unhandled] [500] Named export 'Config' not found. The requested module '@epicgames-ps/lib-pixelstreamingfrontend-ue5.2' is a CommonJS module, which may not support all module.exports as named exports.
CommonJS modules can always be imported via the default export, for example using:

import pkg from '@epicgames-ps/lib-pixelstreamingfrontend-ue5.2';
const { PixelStreaming, Config } = pkg;

  at ModuleJob._instantiate (node:internal/modules/esm/module_job:123:21)
  at async ModuleJob.run (node:internal/modules/esm/module_job:189:5)
[nuxt] [request error] [unhandled] [500] Named export 'Config' not found. The requested module '@epicgames-ps/lib-pixelstreamingfrontend-ue5.2' is a CommonJS module, which may not support all module.exports as named exports.
CommonJS modules can always be imported via the default export, for example using:

import pkg from '@epicgames-ps/lib-pixelstreamingfrontend-ue5.2';
const { PixelStreaming, Config } = pkg;

  at ModuleJob._instantiate (node:internal/modules/esm/module_job:123:21)
  at async ModuleJob.run (node:internal/modules/esm/module_job:189:5)
```
