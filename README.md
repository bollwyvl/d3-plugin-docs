# So you want to write a plugin for d3...
> A while ago, you discovered [d3.js](http://d3js.org), a Javascript library for building data-driven documents for the web. You've learned to create [bl.ocks](http://bl.ocks.org) for your works in progress with [gist](http://gist.github.com), and have gone from learning a few things from [Stack Overflow](http://stackoverflow.com/questions/tagged/d3.js) and the [mailing list](https://groups.google.com/forum/#!topic/d3-js) to teaching others. You've copy-and-pasted the same bar chart a couple times now, and have decided, if only for your own sanity, that you want to make it publicly available. But where?

While there exists a [d3-plugins](http://github.com/d3/d3-plugins) repository, it has several shortcomings:

- it puts all of the effort on the maintainers of a single repository to curate the repositories, which doesn't scale
- if it did scale, and had thousands of plugins, it would probably no longer be useful or manageable
- it has no metadata, documentation or examples embedded with the code
- it is not distributable via any of the package managers, e.g. bower, npm, etc.
- it is not maintained on a true CDN
  - > NOTE: while `d3-plugins` is reachable from rawgit by way of github, even the [production](https://rawgit.com/faq#diff-between-rawgit-and-cdn) URL scheme lacks many of the features of traditional CDNs

Based on [this conversation](https://groups.google.com/forum/#!topic/d3-js/VaRDXom79Uc) between some developers of d3 plugins, a need was identified for a resource where a developer can:
- find d3 plugins (not frameworks built on top of d3) for use
  - off a CDN, in live coding, i.e. codepen, tributary
  - in a package manager for app development
- learn how to build d3 plugins
  - that follow best practices
  - don't require lots of meta-work/chores i.e. publishing, etc.

The rest of this document is the beginning of that documentation. It will likely become multiple documents. It should also guide and explain the creation of additional resources, including:

- a d3-specific plugin discovery page, backed by an existing package manager
- a [Yeoman](http://yeoman.io) generator
