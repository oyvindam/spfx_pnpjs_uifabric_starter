## spfx-pnpjs-uifabric-starter

Starter for spfx-webpart using react:

- **office-ui-fabric-react** (LTS-version)

- **@pnp** (latest)

- **tslint-react**

- **luxon** (date-handling)

- **polyfills (core-js + @pnp/polyfill-ie11)**
  ! Take care here: there seems to be conflicts between these. Loading core-js has led to infinite loops and errors in IE.
  Best approach so far has been to load polyfills from core-js as needed.

````javascript
  import '@pnp/polyfill-ie11';
  import 'core-js/modules/es6.array.find.js';
  import 'core-js/modules/es6.array.find-index.js';
  import 'core-js/modules/es6.number.is-nan.js';```

---

### Building the code

```bash
git clone the repo
npm i
npm i -g gulp
gulp
````

This package produces the following:

- lib/\* - intermediate-stage commonjs build artifacts
- dist/\* - the bundled script, along with other resources
- deploy/\* - all resources which should be uploaded to a CDN.

### Build options

gulp clean - TODO
gulp test - TODO
gulp serve - TODO
gulp bundle - TODO
gulp package-solution - TODO
