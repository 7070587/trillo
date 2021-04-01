$ sass <input.scss> [output.css]
# sass compile

## One-to-One Mode
```bash
sass <input.scss> [output.css]
```

```bash
sass scss/main.scss:css/style.css
sass scss/main.scss:css/style.css --style=compressed
```

## Many-to-many Mode
```bash
sass [<input.css>:<output.css>] [<input/>:<output/>]...
```

## Watch Mode
```bash
 sass --watch scss/main.scss:css/style.css
```

## package.json script
auto open live server and compile scss --> css
```bash
"start": "live-server && sass --watch scss/main.scss:css/style.css",
```
auto open live server
```bash
  "live": "live-server", 
```
compile scss --> css
```bash
    "watch": "sass --watch scss/main.scss:css/style.css",
```

compile scss --> css
```bash
    "compile": "sass scss/main.scss:css/style.css",
    "compile": "sass scss/main.scss:css/style.css --style=compressed",
```

concat multiple css files to one css file
```bash
   "concat": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css"
```
autoprefixer css 
```bash
    "prefix": " postcss css/style.css --replace --use autoprefixer"
```
compress css lines
```bash
    "compress": "sass scss/main.scss:css/style.css --style=compressed"
```

conbime concat && autoprefixer && compress
```bash
    "build": "sass scss/main.scss:css/style.css --style=compressed && concat -o css/style.css css/icon-font.css css/style.css && postcss css/style.css --replace --use autoprefixer"
```

