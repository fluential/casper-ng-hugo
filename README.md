# Victor Hugo CMS Template NG
## Casper CMS NG - Hugo version of Casper theme for Ghost

This is continuation of the work from https://github.com/bdougie/casper-cms-template
Provides cleaned up version supporting latest version of Hugo in native way.

## New Features:
* Mermaid graphs (see diagrams page for example)

Casper is a single-column theme for [Hugo](http://gohugo.io/).
Ported from [Casper theme for Ghost ](https://github.com/TryGhost/Casper)

Demo: https://casper-cms-ng.netlify.app/

Original author:
blog demo : http://vjeantet.fr
blog source : https://github.com/vjeantet/vjeantet.fr

![Hugo Casper Theme screenshot](https://raw.githubusercontent.com/vjeantet/hugo-theme-casper/master/images/screen.png)

## Features

* Mermaid graphs (see diagrams page for example)
* Google Analytics (optional)
* Disqus ( can disable comments by content)
* Share buttons on Facebook, Twitter, Google (can disable share by content)
* Big cover image (optional)
* Custom cover by content (optional)
* Tagging
* Pagination
* Menu

# Theme usage and asumptions
* All blog posts are in the ```post``` folder (```content/post```)
* The homepage displays a paginated list of contents from the post Section (other contents may be added to main menu, see bellow)

# Installation

A working, clean version of the original template that works under most recent version of Hugo. Removed bloat and simplified.

<!-- Markdown snippet -->
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/fluential/casper-cms-template-ng)

![casper theme image](https://s3-us-west-1.amazonaws.com/publis-brian-images/casper.jpg)

**A [Hugo](http://gohugo.io/) boilerplate for creating truly epic websites**

## Usage
Make sure that you have the latest [Hugo](https://gohugo.io/overview/installing/) installed.

Clone this repository and run:

```bash
hugo server --buildDrafts --debug
```

Then visit http://localhost:1313/

To build your static output to the `public` folder, use:

```bash
hugo --gc
```

## Structure

```
|--site                // Everything in here will be built with hugo
|  |--content          // Pages and collections - ask if you need extra pages
|  |--data             // YAML data files with any data for use in examples
|  |--layouts          // This is where all templates go
|  |  |--partials      // This is where includes live
|  |  |--index.html    // The index page
|  |--static           // Files in here ends up in the public folder
|--src                 // Files that will pass through the asset pipeline
|  |--css              // CSS files in the root of this folder will end up in /css/...
|  |--js               // app.js will be compiled to /js/app.js with babel
```
## CMS

### How it works

Netlify CMS is a single-page app that you pull into the `/admin` part of your site.

It presents a clean UI for editing content stored in a Git repository.

You setup a YAML config to describe the content model of your site, and typically
tweak the main layout of the CMS a bit to fit your own site.

### Setup GitHub as a Backend

In the `config.yml` file [change the GitHub owner and repo](https://github.com/bdougie/strata-cms-template/blob/master/site/static/admin/config.yml#L3) to reflect your repo:

```yaml
backend:
  name: github
  repo: owner/repo # Path to your Github repository
  branch: master # Branch to update (master by default)
  
  ...
```
When a user navigates to `/admin` she'll be prompted to login, and once authenticated
she'll be able to create new content or edit existing content.
The default Github-based authenticator integrates with Netlify's [Authentication Provider feature](https://www.netlify.com/docs/authentication-providers) and the repository
backend integrates directly with Github's API.

To get everything hooked up, setup continuous deployment from Github to Netlify
and then follow [the documentation](https://www.netlify.com/docs/authentication-providers)
to setup Github as an authentication provider.

That's it, now you should be able to go to the `/admin` section of your site and
log in.

### Find out more and contribute

Visit the [Netlify CMS](https://github.com/netlify/netlify-cms/) to find out more and contribute. 

## Basic Concepts

You can read more about Hugo's template language in their documentation here:

https://gohugo.io/templates/overview/

The most useful page there is the one about the available functions:

https://gohugo.io/templates/functions/

For assets that are completely static and don't need to go through the asset pipeline,
use the `site/static` folder. Images, font-files, etc, all go there.

Files in the static folder ends up in the web root. So a file called `site/static/favicon.ico`
will end up being available as `/favicon.ico` and so on...

The `src/js/app.js` file is the entrypoint for webpack and will be built to `/dist/app.js`.

You can use ES6 and use both relative imports or import libraries from npm.

Any CSS file directly under the `src/css/` folder will get compiled with [PostCSS Next](http://cssnext.io/)
to `/dist/css/{filename}.css`. Import statements will be resolved as part of the build

## Deploying to netlify

- Push your clone to your own GitHub repository.
- [Create a new site on Netlify](https://app.netlify.com/start) and link the repository.

Now netlify will build and deploy your site whenever you push to git.

##  Enjoy!!

#### License

[MIT](LICENSE)
