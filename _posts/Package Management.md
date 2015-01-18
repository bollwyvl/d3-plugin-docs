# Primary Distribution: npm
While many options exist for the distribution of javascript, [npm](https://npmjs.org) has the lowest barrier to entry. What it lacks in focus on front-end assets, like `bower`, it makes up for with access to tooling for tests.

## `package.json`
Where possible, the plugin's `package.json` should be the single source of truth for all metadata. Most JS-specific tools can use it as their configuration store. Here are some guidelines that will help.

### [`name`](https://docs.npmjs.com/files/package.json#name)
It has to be unique. It could have d3 in the name. Maybe keep it lowercase. Otherwise have fun.

> Example: `"name": "d3-layout-orbital"`

### [`peerDepenencies`](https://docs.npmjs.com/files/package.json#license)
Unlike its siblings, the more popular `dependencies`, and the nerdier `devDependencies`, this key exists exactly for the purpose of documenting that one package is a [plugin of another package](http://blog.nodejs.org/2013/02/07/peer-dependencies/). This is critical so you don't end up with _n_ versions of d3 running around if you install 10 plugins.

> Example: `"peerDepenencies": {"d3": "3.x"}`


### [`keywords`](https://docs.npmjs.com/files/package.json#keywords)
Because

### [`version`](https://docs.npmjs.com/files/package.json#version)
This is the thing you have to maintain when you do your releases. You can help your users by following [semantic versioning](http://semver.org).

### [`license`](https://docs.npmjs.com/files/package.json#license)
Let's not have the lawyer talk right now. Once you create some software, you own it, and for other people to use it with confidence, you have to make sure that is clear how they can use it.

d3 is licensed under the [BSD license](https://spdx.org/licenses/BSD-3-Clause). Read up: it's pretty good.
