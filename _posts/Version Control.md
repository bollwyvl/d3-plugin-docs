# A notional plugin repo structure
A plugin should be stored in a VCS repository. We'll assume [git](http://git-scm.org) on [github](http://github.com), though if you are using something else that is compatible with `npm`, it should be very similar.

At any given time, the `master` branch should contain:
```
├─ d3.plugin-name.js
├─ README.md
├─ package.json
├─ .travis.yml
├─ .gitignore
├─ examples/
|  ├─ index.html
|  └─ something/
|     └─ index.html
└─
```

## Github-specific: `gh-pages`
The plugin should have a page hosted where a developer can go open up a console and do some live coding with a some running instances of the plugin. Maintaining a `gh-pages` branch is the easiest way to have an easily-linkable, live page, without relying on third-parties.
