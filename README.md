# docdash-hia

Because of the need to cooperate with [jsdoc-plugin-hia](https://github.com/mandolin/jsdoc-plugin-hia) code preview function that will be implemented later, some specific styles are needed, and there may be more customization requirements in the future, so I forked docdash.It is more convenient by this way.

Because only a few style adjustments have been made for the time being, only the project itself is at present. If the expansion is more in the later stage, then I maybe consider whether to build the corresponding project official website.

因为需要配合 [jsdoc-plugin-hia](https://github.com/mandolin/jsdoc-plugin-hia) 后期将会实现的代码预览功能，因而需要一些针对性的样式，加上以后可能会有更多的自定义需求，因此fork出docdash的衍生项目，这样更方便些。

因为暂时只做了一些样式调整，因此目前只有项目本身，后期如果扩展的更多，则再考虑是否搭建相应的项目官网。

### npm install:

```bash
	npm i docdash-hia -D
````

## The following is the original docdash content.以下为原docdash内容。

----

# Docdash
[![Build Status](https://api.travis-ci.org/clenemt/docdash.png?branch=master)](https://travis-ci.org/clenemt/docdash) [![npm version](https://badge.fury.io/js/docdash.svg)](https://badge.fury.io/js/docdash) [![license](https://img.shields.io/npm/l/docdash.svg)](LICENSE.md)

A clean, responsive documentation template theme for JSDoc 3.

![docdash-screenshot](https://cloud.githubusercontent.com/assets/447956/13398144/4dde7f36-defd-11e5-8909-1a9013302cb9.png)

![docdash-screenshot-2](https://cloud.githubusercontent.com/assets/447956/13401057/e30effd8-df0a-11e5-9f51-66257ac38e94.jpg)

## Example
See http://clenemt.github.io/docdash/ for a sample demo. :rocket:

## Install

```bash
$ npm install docdash
```

## Usage
Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/docdash
```

## Usage (npm)
In your projects `package.json` file add a new script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc -c jsdoc.json"
}
```

In your `jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/docdash"
}
```

## Sample `jsdoc.json`
See the config file for the [fixtures](fixtures/fixtures.conf.json) or the sample below.

```json
{
    "tags": {
        "allowUnknownTags": false
    },
    "source": {
        "include": "../js",
        "includePattern": ".js$",
        "excludePattern": "(node_modules/|docs)"
    },
    "plugins": [
        "plugins/markdown"
    ],
    "opts": {
        "template": "assets/template/docdash/",
        "encoding": "utf8",
        "destination": "docs/",
        "recurse": true,
        "verbose": true
    },
    "templates": {
        "cleverLinks": false,
        "monospaceLinks": false
    }
}
```

## Options
Docdash supports the following options:

```
{
    "docdash": {
        "static": [false|true],         // Display the static members inside the navbar
        "sort": [false|true],           // Sort the methods in the navbar
        "sectionOrder": [        // Order the main section in the navbar (default order shown here)
             "Classes",
             "Modules",
             "Externals",
             "Events",
             "Namespaces",
             "Mixins",
             "Tutorials",
             "Interfaces"
        ]
        "disqus": "",                   // Shortname for your disqus (subdomain during site creation)
		"openGraph": {                  // Open Graph options (mostly for Facebook and other sites to easily extract meta information)
			"title": "",                // Title of the website
			"type": "website",          // Type of the website
			"image": "",                // Main image/logo
			"site_name": "",            // Site name
			"url": ""                   // Main canonical URL for the main page of the site
		},
		"meta": {                       // Meta information options (mostly for search engines that have not indexed your site yet)
			"title": "",                // Also will be used as postfix to actualy page title, prefixed with object/document name
			"description": "",          // Description of overal contents of your website
			"keyword": ""               // Keywords for search engines
		},
        "search": [false|true],         // Display seach box above navigation which allows to search/filter navigation items
        "collapse": [false|true],       // Collapse navigation by default except current object's navigation of the current page
        "typedefs": [false|true],       // Include typedefs in menu
        "navLevel": [integer],          // depth level to show in navbar, starting at 0 (false or -1 to disable)
        "private": [false|true],        // set to false to not show @private in navbar
        "removeQuotes": [none|all|trim],// Remove single and double quotes, trim removes only surrounding ones
        "scripts": []                   // Array of external (or relative local copied using templates.default.staticFiles.include) scripts to inject into HTML,
        "menu":{                        // Adding additional menu items after Home
            "Project Website":{         // Menu item name
                "href":"https://myproject.com", //the rest of HTML properties to add to manu item
                "target":"_blank",
                "class":"menu-item",
                "id":"website_link"
            },
            "Forum":{
                "href":"https://myproject.com.forum",
                "target":"_blank",
                "class":"menu-item",
                "id":"forum_link"
            }
        }
    }
}
```

Place them anywhere inside your `jsdoc.json` file.

## Contributors

[![0](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/0)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/0)
[![1](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/1)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/1)
[![2](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/2)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/2)
[![3](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/3)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/3)
[![4](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/4)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/4)
[![5](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/5)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/5)
[![6](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/6)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/6)
[![7](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/images/7)](https://sourcerer.io/fame/ar2rsawseen/clenemt/docdash/links/7)

## Thanks
Thanks to [lodash](https://lodash.com) and [minami](https://github.com/nijikokun/minami).

## License
Licensed under the Apache License, version 2.0. (see [Apache-2.0](LICENSE.md)).
