# npm-scripts

Collection of useful NPM scripts.

---

## About

I ditched [Gulp](http://gulpjs.com/)/[Grunt](http://gruntjs.com/) a few years ago and never looked back. 

Why add another layer of complexity to your application if you can accomplish the same thing in a simpler fashion? These are based on some useful/simple scripts I use in most of my projects, if you want to easily try some of these out - take a look at  [g5-component.js](https://github.com/MajorLeagueBaseball/g5-component)

---

## Scripts

### Compress Images

| Command            | Dependency                                         | Description              |
|:-------------------|:-----------|:--------------------------------------|:-------------------------|
| `compress-images`  | [imagemin](https://www.npmjs.com/package/imagemin) | Minify images seamlessly |

```json
"compress-images": "imagemin --progressive src/images/* src/images/build"
```

---

## Defaults

* TODO

## Best Practices

* TODO

## Reference

* [task automation with npm run](http://substack.net/task_automation_with_npm_run)

