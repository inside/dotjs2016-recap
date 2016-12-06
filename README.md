# DotJS 2016

First Round
===========

1. **Nolan Lawson** (IE team) talked about how browsers evolved and explained
   how service workers are implemented in Microsoft Edge. Service workers are
   useful for developing PWA and their top features are:
    * Offline support
    * Push notifications
    * Background synchronization

    http://egde.ms is a place where you can download Virtual Machine with
    different versions of IE.


2. **Ada Rose Edwards** talked about VR on the web. It could be used for real
   estate classified ads.


3. **Christophe Porteneuve** talked about Babel and what's the current support
   of browsers for es2015:
   https://tdd.github.io/dotjs2016-babel-tuning/#/native-support

   His slides are available here: https://tdd.github.io/dotjs2016-babel-tuning/

   Babels configuration in either done in the .babelrc file or directly in the
   package.json under the babel key.

   Important things to remember:

   * A babel plugin is a piece of code that transpiles a new langage construct
   to an older langage construct.
   For example, this plugin compiles ES2015 arrow functions to ES5:
   https://babeljs.io/docs/plugins/transform-es2015-arrow-functions/

   * A preset is a group of plugins. Babel provides different presets so you
   don't have to assemble your own set of plugins.
   The es2015 preset includes all transformation plugins for es2015, while the
   es2016 preset only contains the diff from es2015 to es2016. Meaning, if you
   want to code in es2016, you'll have to install both presets.

   * The react preset is needed to code in react.

   * The latest preset is recommended, it includes all finished proposals of
   es2015, es2016 and es2017.

   * The env preset lets babel choose which plugin is needed for the specific
   environment.

4. Guy Bedford talks about SystemJS. It's an universal dynamic module loader.
   His work is essentially towards module loading optimization like tree shaking.
   It can load web assembly files.

   It's not a tool we are interested in since we opted for webpack.

Lightning talks
===============

1. **Overview of React Redux RxJS**. RxJS brings cancellation (the ajax abort
   method).

2. **npm i -g lint-filter**
   From npmjs.com:
   "Only show style errors of things that have changed since master. This
   support tools that support exporting output in checkstyle format. This can
   be useful if you want to convert a project gradually towards a new config,
   (e.g. adding a new rule from the latest release of your linter). Another
   case were this is beneficial is were you do not want to break a build when
   updating the linter."

3. **NoSQL injection in mongodb**
   There's a NoSQL injection vuln in mongodb (can't remember what version). The
   solution for avoiding this type of vuln is to validate data. You're a cool
   kid if you're using the Hapi node server, because data validation is
   included. If you're using express, you can use joi + celebrate for data
   validation.

4. **Moox talks about phenomic**, a Modern static* website generator based on
   the React and Webpack ecosystem.

Second Round
============

1. **@zeke** talks about the npm ecosystem. Here are a list of tools for making our
   developers lives easier:

   * http://ghub.io/ Redirect to a npm package's GitHub page, if available.
   * http://ghub.io/npmrc Switch between different .npmrc files with ease and
     grace.
   * https://github.com/zeke/npm-hub A browser extension for exploring npm
     dependencies on GitHub repos http://npmhub.org
   * http://octolinker.github.io/ Links together, what belongs together.
   * https://github.com/VictorBjelkholm/trymodule Puts you in a REPL to easily
     try the module you want to test
   * https://www.npmjs.com/package/ghwd Open the GitHub URL that matches your
     shell's current branch and working directory. Works for BitBucket and
     GitLab too.
   * https://www.npmjs.com/package/ntl Npm Task List: Interactive cli menu to
     list/run npm tasks
   * https://www.npmjs.com/package/dependent-packages Offline collection of the
     dependents and devDependents of every package in the npm registry.
   * http://electron.atom.io/userland/

2. **Evan You** talks about vue.js. Its render optimisation is done by push instead
   of pull used by React (one must implement shouldComponentUpdate). He's also
   using Patreon as funding system.

Lightning talks
===============

1. **Webvim**, a vim distribution for web development.
   http://webvim.org/

2. **Bit operators explained**

3. **[Nuxt.js](https://github.com/nuxt/nuxt.js)** It can do dynamic routing
   based on the filesystem as an api.
   * /pages/home.js => /home
   * /pages/about.js => /about
   etc...

   Backendless hosting: nuxt generates html files and when the data changes it
   calls AWS lambda which regenerates the pages.

Third Round
===========

1. NodeJS Core contributor **Fedor Indutny** talks about memory layout.

2. LiveJS, Tim and Sam demonstrate how to create music using the gameboy
   advanced, node, the browser, LEDs and the fog machine. They use:
   * ModV
   * Nerd disco
   * The midi web api and the novation launch control

3. **Guillermo Rauch** talks about universal js. He uses now.sh for deployment
   and talks about the next.js framework.
   * [Next.js](https://github.com/zeit/next.js) uses the file system as an api
   for the routing. Dynamic routing is not supported yet.
   * It uses isomorphic-fetch.
   * Can do prefetching with the Link component: &lt;Link&gt;&lt;a href="..."&gt;foo&lt;/a&gt;&lt;/Link&gt;
   * Code splitting is out of the box.
   * The &lt;Head&gt; component can update elements in the &lt;head&gt; (much like Helmet?).
   * The 'next/css' module does css in js.

4. Igor Minar, angular lead, talks about being open minded in the open source
world.
