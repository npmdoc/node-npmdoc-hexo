# api documentation for  [hexo (v3.2.2)](https://hexo.io/)  [![npm package](https://img.shields.io/npm/v/npmdoc-hexo.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-hexo) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-hexo.svg)](https://travis-ci.org/npmdoc/node-npmdoc-hexo)
#### A fast, simple & powerful blog framework, powered by Node.js.

[![NPM](https://nodei.co/npm/hexo.png?downloads=true)](https://www.npmjs.com/package/hexo)

[![apidoc](https://npmdoc.github.io/node-npmdoc-hexo/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-hexo_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-hexo/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-hexo/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-hexo/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tommy Chen",
        "email": "tommy351@gmail.com",
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
        "shasum": "9b8e7022aec95e02021cec140afd7888d4ceb931",
        "tarball": "https://registry.npmjs.org/hexo/-/hexo-3.2.2.tgz"
    },
    "gitHead": "792bbb4ed70625d76be0920edb700faf05848108",
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
            "name": "tommy351",
            "email": "tommy351@gmail.com"
        }
    ],
    "name": "hexo",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
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
    "version": "3.2.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module hexo](#apidoc.module.hexo)
1.  [function <span class="apidocSignatureSpan">hexo.</span>super_ ()](#apidoc.element.hexo.super_)
1.  string <span class="apidocSignatureSpan">hexo.</span>core_dir
1.  string <span class="apidocSignatureSpan">hexo.</span>lib_dir
1.  string <span class="apidocSignatureSpan">hexo.</span>version



# <a name="apidoc.module.hexo"></a>[module hexo](#apidoc.module.hexo)

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



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
