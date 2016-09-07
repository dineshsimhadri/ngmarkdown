#ngMarkdown
> Fully-Configurable Markdown Service

##Overview
An [AngularJS](https://angularjs.org) module that integrates a full-blown, fully configurable markdown service
for your angularjs apps. Contains a simple directive and a service.

ngMarkdown isn't a WYSISYG editor. Its just a plain text markdown editor, with a few extra few features enabled.
Depends on [CodeMirror](https://codemirror.net)(customized, minimized & built into the project), [Marked](https://github.com/chjj/marked) & [AngularJS](https://angularjs.prg) projects.

Inspiration from [Lepture](https://github.com/lepture/editor) was the kickstart of the project.

**NOTE:** The module is still under its beta development. Please keep checking the master branch for changes.


## Quickstart
- Install ngMarkdown using bower

```bash
$ bower install ngMarkdown -save
```

- Include the required dependencies

```html
<script src="bower_components/angular/angular.js"></script>
<script src="bower_components/marked/lib/marked.js"></script>
```


- Include the required libraries in your applications index page

```html
<link rel="stylesheet" href="bower_components/angular-markdown/angular-markdown.css"/>
<script src="bower_components/angular-markdown/angular-markdown.js"></script>
```

- Inject the module into your angularjs application

```javascript
var app = angular.module('app', ['ngMarkdown']);
```

- To configure the editor on config phase, use the `$markdownProvider`

```javascript
app.config(function($markdownProvider){
  $markdownProvider.config({
    gfm: false,
    toolbar: false,
    statusbar: false,
    ...
  });
});
```

Options will be coming soon.

- Use the markdown directive where ever you want the editor to be placed

```html
<body ng-app="app">
  <markdown class="post"></markdown>
</body>
```


## Developers
Clone the repo using `git clone https://github.com/whoisandie/ngMarkdown.git`.
ngMarkdown builds are automated by `gulp` and tested by `karma`.

Run the below two commands to get started.

```bash
$ npm install
$ gulp
```

You can build the latest version of ngMarkdown using

```bash
$ gulp build
```

As mentioned earlied, all the module is tested by karma. Run the tests using

```bash
$ gulp test
```


##Contribution
Want to make a contribution ? Cool! Fork the repo, tweak, add your changes, submit a pull request :)
And yes contributions will be appreciated !