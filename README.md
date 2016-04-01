# npm-scripts

Collection of useful NPM scripts. 

---

## About

I ditched [Gulp](http://gulpjs.com/)/[Grunt](http://gruntjs.com/) a few years ago and never looked back. 

Why add another layer of complexity to your application if you can accomplish the same thing in a simpler fashion? These are based on some useful/simple scripts I use in most of my projects, if you want to easily try some of these out - take a look at  [g5-component.js](https://github.com/MajorLeagueBaseball/g5-component)

---

## Scripts

### Serve

| Command            | Dependency                                                | Description              |
|:-------------------|:-----------|:---------------------------------------------|:-------------------------|
| `serve`            | [http-server](https://www.npmjs.com/package/http-server)  | starts up server with cache disabled on localhost:9966 |

```json
"serve": "http-server -c-1 -p 9966"
```

### Lint

| Command            | Dependency                                         | Description              |
|:-------------------|:-----------|:--------------------------------------|:-------------------------|
| `lint`  | [jshint](https://www.npmjs.com/package/jshint) | detect errors and potential problems in JavaScript code |

```json
"lint": "jshint src/scripts/ || true"
```

### Compress Images

| Command            | Dependency                                         | Description              |
|:-------------------|:-----------|:--------------------------------------|:-------------------------|
| `compress-images`  | [imagemin](https://www.npmjs.com/package/imagemin) | minify images seamlessly |

```json
"compress-images": "imagemin --progressive src/images/* src/images/build"
```

### Minify CSS

| Command            | Dependency                                         | Description              |
|:-------------------|:-----------|:--------------------------------------|:-------------------------|
| `minify-css`  | [clean-css](https://www.npmjs.com/package/clean-css) | fast and efficient Node.js library for minifying CSS files |

```json
"minify-css": "cleancss --source-map -d -o src/static/g5-component-min.css src/static/g5-component.css"
```

### Prefix CSS

| Command            | Dependency                                         | Description              |
|:-------------------|:-----------|:--------------------------------------|:-------------------------|
| `prefix-css`  | [postcss](https://www.npmjs.com/package/postcss) + [autoprefixer](https://github.com/postcss/autoprefixer) | parse CSS and add vendor prefixes to rules by Can I Use |

```json
"prefix-css": "postcss -u autoprefixer -o src/static/g5-component.css src/static/g5-component.css"
```








---

## Defaults

* If there is a `server.js` file in the root of your package, then npm will default the `start` command to `node server.js`.
* If there is a `binding.gyp` file in the root of your package, npm will default the `install` command to compile using node-gyp.

## Best Practices

* TODO

## Reference

* [task automation with npm run](http://substack.net/task_automation_with_npm_run)

