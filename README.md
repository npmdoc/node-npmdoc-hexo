# api documentation for  [hexo (v3.3.1)](https://hexo.io/)  [![npm package](https://img.shields.io/npm/v/npmdoc-hexo.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-hexo) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-hexo.svg)](https://travis-ci.org/npmdoc/node-npmdoc-hexo)
#### A fast, simple & powerful blog framework, powered by Node.js.

[![NPM](https://nodei.co/npm/hexo.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/hexo)

[![apidoc](https://npmdoc.github.io/node-npmdoc-hexo/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-hexo/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-hexo/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-hexo/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tommy Chen",
        "url": "http://zespia.tw"
    },
    "bin": {
        "hexo": "./bin/hexo"
    },
    "bugs": {
        "url": "https://github.com/hexojs/hexo/issues"
    },
    "dependencies": {
        "abbrev": "^1.0.7",
        "archy": "^1.0.0",
        "bluebird": "^3.4.0",
        "chalk": "^1.1.3",
        "cheerio": "^0.20.0",
        "deep-assign": "^2.0.0",
        "hexo-cli": "^1.0.2",
        "hexo-front-matter": "^0.2.2",
        "hexo-fs": "^0.1.5",
        "hexo-i18n": "^0.2.1",
        "hexo-log": "^0.1.2",
        "hexo-util": "^0.6.0",
        "js-yaml": "^3.6.1",
        "lodash": "^4.13.1",
        "minimatch": "^3.0.0",
        "moment": "~2.13.0",
        "moment-timezone": "^0.5.4",
        "nunjucks": "^2.4.2",
        "pretty-hrtime": "^1.0.2",
        "strip-indent": "^1.0.1",
        "swig": "1.4.2",
        "swig-extras": "0.0.1",
        "text-table": "^0.2.0",
        "tildify": "^1.2.0",
        "titlecase": "^1.1.2",
        "warehouse": "^2.2.0"
    },
    "description": "A fast, simple & powerful blog framework, powered by Node.js.",
    "devDependencies": {
        "chai": "^3.5.0",
        "chai-as-promised": "^5.3.0",
        "eslint": "^2.12.0",
        "eslint-config-hexo": "^1.0.3",
        "hexo-renderer-marked": "^0.2.10",
        "istanbul": "^0.4.3",
        "jscs": "^3.0.4",
        "jscs-preset-hexo": "^1.0.1",
        "mocha": "^2.5.3",
        "rewire": "^2.5.1",
        "sinon": "^1.17.4"
    },
    "directories": {
        "lib": "./lib",
        "bin": "./bin"
    },
    "dist": {
        "shasum": "6c38653b7239536a21036bfcf2e306cb24b98f63",
        "tarball": "https://registry.npmjs.org/hexo/-/hexo-3.3.1.tgz"
    },
    "gitHead": "d3054c6c143a97f4653bada24db31a34dbd20a23",
    "homepage": "https://hexo.io/",
    "keywords": [
        "website",
        "blog",
        "cms",
        "framework",
        "hexo"
    ],
    "license": "MIT",
    "main": "lib/hexo",
    "maintainers": [
        {
            "name": "abnerchou"
        },
        {
            "name": "tommy351"
        }
    ],
    "name": "hexo",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/hexojs/hexo.git"
    },
    "scripts": {
        "eslint": "eslint .",
        "jscs": "jscs .",
        "test": "mocha test/index.js",
        "test-cov": "istanbul cover --print both _mocha -- test/index.js"
    },
    "version": "3.3.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module hexo](#apidoc.module.hexo)
1.  [function <span class="apidocSignatureSpan"></span>hexo (base, args)](#apidoc.element.hexo.hexo)
1.  [function <span class="apidocSignatureSpan">hexo.</span>super_ ()](#apidoc.element.hexo.super_)
1.  [function <span class="apidocSignatureSpan">hexo.</span>toString ()](#apidoc.element.hexo.toString)
1.  string <span class="apidocSignatureSpan">hexo.</span>core_dir
1.  string <span class="apidocSignatureSpan">hexo.</span>lib_dir
1.  string <span class="apidocSignatureSpan">hexo.</span>version



# <a name="apidoc.module.hexo"></a>[module hexo](#apidoc.module.hexo)

#### <a name="apidoc.element.hexo.hexo"></a>[function <span class="apidocSignatureSpan"></span>hexo (base, args)](#apidoc.element.hexo.hexo)
- description and source-code
```javascript
function Hexo(base, args) {
  base = base || process.cwd();
  args = args || {};

  EventEmitter.call(this);

  this.base_dir = base + sep;
  this.public_dir = pathFn.join(base, 'public') + sep;
  this.source_dir = pathFn.join(base, 'source') + sep;
  this.plugin_dir = pathFn.join(base, 'node_modules') + sep;
  this.script_dir = pathFn.join(base, 'scripts') + sep;
  this.scaffold_dir = pathFn.join(base, 'scaffolds') + sep;
  this.theme_dir = pathFn.join(base, 'themes', defaultConfig.theme) + sep;
  this.theme_script_dir = pathFn.join(this.theme_dir, 'scripts') + sep;

  this.env = {
    args: args,
    debug: Boolean(args.debug),
    safe: Boolean(args.safe),
    silent: Boolean(args.silent),
    env: process.env.NODE_ENV || 'development',
    version: pkg.version,
    init: false
  };

  var multiConfigPath = require('./multi_config_path')(this);
  this.config_path = args.config ? multiConfigPath(base, args.config)
                                 : pathFn.join(base, '_config.yml');

  this.extend = {
    console: new extend.Console(),
    deployer: new extend.Deployer(),
    filter: new extend.Filter(),
    generator: new extend.Generator(),
    helper: new extend.Helper(),
    migrator: new extend.Migrator(),
    processor: new extend.Processor(),
    renderer: new extend.Renderer(),
    tag: new extend.Tag()
  };

  this.config = _.cloneDeep(defaultConfig);

  this.log = logger(this.env);

  this.render = new Render(this);

  this.route = new Router();

  this.post = new Post(this);

  this.scaffold = new Scaffold(this);

  this._dbLoaded = false;

  this._isGenerating = false;

  this.database = new Database({
    version: dbVersion,
    path: pathFn.join(base, 'db.json')
  });

  registerModels(this);

  this.source = new Source(this);
  this.theme = new Theme(this);
  this.locals = new Locals(this);
  this._bindLocals();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.hexo.super_"></a>[function <span class="apidocSignatureSpan">hexo.</span>super_ ()](#apidoc.element.hexo.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.hexo.toString"></a>[function <span class="apidocSignatureSpan">hexo.</span>toString ()](#apidoc.element.hexo.toString)
- description and source-code
```javascript
toString = function () {
    return toString;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
