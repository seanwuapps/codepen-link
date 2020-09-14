![Built With Stencil](https://img.shields.io/badge/-Built%20With%20Stencil-16161d.svg?logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz4KPCEtLSBHZW5lcmF0b3I6IEFkb2JlIElsbHVzdHJhdG9yIDE5LjIuMSwgU1ZHIEV4cG9ydCBQbHVnLUluIC4gU1ZHIFZlcnNpb246IDYuMDAgQnVpbGQgMCkgIC0tPgo8c3ZnIHZlcnNpb249IjEuMSIgaWQ9IkxheWVyXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4IgoJIHZpZXdCb3g9IjAgMCA1MTIgNTEyIiBzdHlsZT0iZW5hYmxlLWJhY2tncm91bmQ6bmV3IDAgMCA1MTIgNTEyOyIgeG1sOnNwYWNlPSJwcmVzZXJ2ZSI%2BCjxzdHlsZSB0eXBlPSJ0ZXh0L2NzcyI%2BCgkuc3Qwe2ZpbGw6I0ZGRkZGRjt9Cjwvc3R5bGU%2BCjxwYXRoIGNsYXNzPSJzdDAiIGQ9Ik00MjQuNywzNzMuOWMwLDM3LjYtNTUuMSw2OC42LTkyLjcsNjguNkgxODAuNGMtMzcuOSwwLTkyLjctMzAuNy05Mi43LTY4LjZ2LTMuNmgzMzYuOVYzNzMuOXoiLz4KPHBhdGggY2xhc3M9InN0MCIgZD0iTTQyNC43LDI5Mi4xSDE4MC40Yy0zNy42LDAtOTIuNy0zMS05Mi43LTY4LjZ2LTMuNkgzMzJjMzcuNiwwLDkyLjcsMzEsOTIuNyw2OC42VjI5Mi4xeiIvPgo8cGF0aCBjbGFzcz0ic3QwIiBkPSJNNDI0LjcsMTQxLjdIODcuN3YtMy42YzAtMzcuNiw1NC44LTY4LjYsOTIuNy02OC42SDMzMmMzNy45LDAsOTIuNywzMC43LDkyLjcsNjguNlYxNDEuN3oiLz4KPC9zdmc%2BCg%3D%3D&colorA=16161d&style=flat-square)

# `codepen-link`

[Codepen](https://codepen.io/) is an awesome tool to showcase a piece of front-end code. Did you know there is a way to dynamically create a pen with pre-filled code?

Codepen has an amazing API to allow developers do this, however the way to do it is via submitting a `form`. The `codepen-link` component simplifies this set up. 


## Usage

```html
<codepen-link
  html="<h1>Hello world</h1>"
  title="Open in CodePen"
  pen-title="New demo pen"
  editors="110"
  css-preprocessor="scss"
  css="body{ font-family: 'Open Sans', sans-serif; }"
  css-external="//fonts.googleapis.com/css?family=Open+Sans:300,400,600,700"
  js-external="https://cdn.jsdelivr.net/npm/codepen-link/dist/codepen-link/codepen-link.js"
>
  <button type="button">Click me view in Codepen</button>
</codepen-link>
```


## Installation

### CDN

```html
<script type="module" src="https://cdn.jsdelivr.net/npm/codepen-link/dist/codepen-link/codepen-link.esm.js"></script>
<script nomodule src="https://cdn.jsdelivr.net/npm/codepen-link/dist/codepen-link/codepen-link.js"></script>
```

add the script tags in your html and the component will get lazy loaded when it's used on the page.

### Framework integration
Please see [framework integration](https://stenciljs.com/docs/overview) in the Stencil documentation.

### Node Modules

- Run `npm install codepen-link --save`
- Put a script tag similar to this `<script src='node_modules/codepen-link/dist/codepen-link.js'></script>` in the head of your index.html
- Then you can use the element anywhere in your template, JSX, html etc

### In a stencil-starter app

- Run `npm install codepen-link --save`
- Add an import to the npm packages `import 'codepen-link';`
- Then you can use the element anywhere in your template, JSX, html etc


## Properties

| Property           | Attribute            | Description                                                                                                                                                       | Type                                                                  | Default                                      |
| ------------------ | -------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------- | -------------------------------------------- |
| `css`              | `css`                | CSS code                                                                                                                                                          | `string`                                                              | `''`                                         |
| `cssExternal`      | `css-external`       | semi-colon separate multiple files                                                                                                                                | `string`                                                              | `''`                                         |
| `cssPreProcessor`  | `css-pre-processor`  | CSS preprocessor                                                                                                                                                  | `"less" \| "none" \| "sass" \| "scss" \| "stylus"`                    | `'none'`                                     |
| `cssPrefix`        | `css-prefix`         | CSS prefix                                                                                                                                                        | `"autoprefixer" \| "neither" \| "prefixfree"`                         | `'neither'`                                  |
| `cssStarter`       | `css-starter`        | CSS reset or normalisation                                                                                                                                        | `"neither" \| "normalize" \| "reset"`                                 | `'neither'`                                  |
| `description`      | `description`        | Description of new pen                                                                                                                                            | `string`                                                              | `''`                                         |
| `editors`          | `editors`            | Set which editors are open. In this example HTML open, CSS closed, JS open                                                                                        | `string`                                                              | `'111'`                                      |
| `head`             | `head`               | Code that should go inside <head></head>                                                                                                                          | `string`                                                              | `''`                                         |
| `html`             | `html`               | HTML code                                                                                                                                                         | `string`                                                              | `'<p>Generated by &lt;codepen-link&gt;</p>'` |
| `htmlClasses`      | `html-classes`       | HTML classes                                                                                                                                                      | `string`                                                              | `''`                                         |
| `htmlPreProcessor` | `html-pre-processor` | HTML preprocessor                                                                                                                                                 | `"haml" \| "markdown" \| "none" \| "slim"`                            | `'none'`                                     |
| `isPrivate`        | `is-private`         | When the Pen is saved, it will save as Private if logged in user has that privledge, otherwise it will save as public                                             | `boolean`                                                             | `false`                                      |
| `js`               | `js`                 | JavaScript code                                                                                                                                                   | `string`                                                              | `''`                                         |
| `jsExternal`       | `js-external`        | semi-colon separate multiple files                                                                                                                                | `string`                                                              | `''`                                         |
| `jsPreProcessor`   | `js-pre-processor`   | JavaScript preprocessor                                                                                                                                           | `"babel" \| "coffeescript" \| "livescript" \| "none" \| "typescript"` | `'none'`                                     |
| `layout`           | `layout`             | Layout of the new pen                                                                                                                                             | `"left" \| "right" \| "top"`                                          | `'top'`                                      |
| `parent`           | `parent`             | If supplied, the Pen will save as a fork of this id. Note it's not the slug, but ID. You can find the ID of a Pen with `window.CP.pen.id` in the browser console. | `string`                                                              | `''`                                         |
| `penTitle`         | `pen-title`          | Title of new pen                                                                                                                                                  | `string`                                                              | `'New Pen'`                                  |
| `tags`             | --                   | an array of strings                                                                                                                                               | `string[]`                                                            | `[]`                                         |


----------------------------------------------