# npm-scripts

Collection of NPM scripts, based on some useful and simple scripts I use in most of my projects.

If you want to easily try some of these out - take a look at [g5-component.js](https://github.com/MajorLeagueBaseball/g5-component)

---

## Scripts

### Serve

Dependency                                                  | Description              |
|:-----------|:---------------------------------------------|:-------------------------|
| [http-server](https://www.npmjs.com/package/http-server) | starts up server with cache disabled `-c-1` on `-p` localhost:9966 |

```json
"serve": "http-server -c-1 -p 9966"
```

### Lint

| Dependency                                         | Description              |
|:-----------|:--------------------------------------|:-------------------------|
| [jshint](https://www.npmjs.com/package/jshint) | detect errors and potential problems in JavaScript code |

```json
"prelint": "echo 'Checking code via JSHint...'"
```

```json
"lint": "jshint src/scripts/ || true"
```

### Test

Dependency                                                  | Description              |
|:-----------|:---------------------------------------------|:-------------------------|
| [babel-tape-runner](https://www.npmjs.com/package/babel-tape-runner) | [Babel](https://babeljs.io/) + [Tape](https://github.com/substack/tape) for running your ES Next tests |

```json
"test": "babel-tape-runner test/*.js | tap-spec"
```

### Compress Images

| Dependency                                         | Description              |
|:-----------|:--------------------------------------|:-------------------------|
| [imagemin](https://www.npmjs.com/package/imagemin) | minify images seamlessly |

```json
"compress-images": "imagemin --progressive src/images/* src/images/build"
```

### Build LESS

| Dependency                                         | Description              |
|:-----------|:--------------------------------------|:-------------------------|
| [less](https://www.npmjs.com/package/less) | Compile LESS to CSS |

```json
"build-less": "lessc src/styles/component.less > src/static/g5-component.css"
```

### Minify CSS

| Dependency                                         | Description              |
|:-----------|:--------------------------------------|:-------------------------|
| [clean-css](https://www.npmjs.com/package/clean-css) | fast and efficient Node.js library for minifying CSS files |

```json
"minify-css": "cleancss --source-map -d -o src/static/g5-component-min.css src/static/g5-component.css"
```

### GZip CSS

| Dependency                                         | Description              |
|:-----------|:--------------------------------------|:-------------------------|
|  | Gzip via the built in compress tool in Linux/Unix based OS |

```json
"gzip-css": "gzip -c -f -9 src/static/g5-component-min.css > src/static/g5-component-min.css.gz"
```

### Prefix CSS

| Dependency                                         | Description              |
|:-----------|:--------------------------------------|:-------------------------|
| [postcss](https://www.npmjs.com/package/postcss) + [autoprefixer](https://github.com/postcss/autoprefixer) | parse CSS and add vendor prefixes to rules by [Can I Use](http://caniuse.com/) |

```json
"prefix-css": "postcss -u autoprefixer -o src/static/g5-component.css src/static/g5-component.css"
```

---

## Notes

* Install packages as `devDependencies` _(i.e._ `npm i --save-dev jshint`_)_ or globally _(i.e._ `npm i -g jshint` _)_
* Pre and post commands with matching names will be run for those as well _(i.e._ `prelint`, `postlint`_)_

## Defaults

* If there is a `server.js` file in the root of your package, then npm will default the `start` command to `node server.js`.
* If there is a `binding.gyp` file in the root of your package, npm will default the `install` command to compile using node-gyp.

## Further Reading

* [npm scripts docs](https://docs.npmjs.com/misc/scripts)
* [task automation with npm run](http://substack.net/task_automation_with_npm_run)
* [why npm scripts](https://css-tricks.com/why-npm-scripts/)
* [how to use npm as a build tool](http://blog.keithcirkel.co.uk/how-to-use-npm-as-a-build-tool/)
* [command-line utilities with Node.js](http://cruft.io/posts/node-command-line-utilities/)
* [mimicking npm scripts in node js](https://www.nczonline.net/blog/2016/03/mimicking-npm-script-in-node-js/)
