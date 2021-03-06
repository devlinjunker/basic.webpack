**NOTE: Any manual changes to Github Wiki will be overwritten by push (PR merged) to `master` branch**

These files should updated whenever we merge to master, and be in sync between:
 - The README files in the repo,
 - The [Github Wiki](https://github.com/devlinjunker/template.webpack.fend/wiki), and
 - The [generated doc site](https://devlinjunker.github.io/template.webpack.fend/manual/index.html) served
    when running the server and on github pages

This project uses a Github Action to accomplish this. The action is executed on merge to the `master` branch
and defined inside of the `./.github/workflows/` directory([github](https://github.com/devlinjunker/template.webpack.fend/tree/master/.github/workflows))
(along with all other github actions) that creates a commit to update the docs directory on github and then
calls a script in the `scripts/actions` directory([github](https://github.com/devlinjunker/template.webpack.fend/tree/master/scripts/actions)).

The script retrieves the following markdown files (defined in `./.esdoc.json`) and copies them to a temporary
directory, then uses the [wiki-page-creator-action](https://github.com/marketplace/actions/wiki-page-creator-action)
to update the Github wiki.

### Table of Contents

- [Setup](manual/README.setup.html) - dependencies and how to install and start development (eventually production?)
- [Entry](manual/README.entry.html) - How Javascript Bundles are defined and files that can be included
- [HTML](manual/README.html.html) - How HTML files are created and the processes we use to ensure quality
- [CSS](manual/README.css.html) - CSS Normalization, Processing and Frameworks
- [Images](manual/README.img.html) - Including images and SVG icons from free library
- [Helpers](manual/README.helpers.html) - Javascript Helper Classes and Code that is used in the project
- [Static HTML Components](manual/README.static.html) - HTML Components that are generated during the build process
- [Dynamic HTML Components](manual/README.components.html) - HTML/JS Components that are created with Handlebars dynamically during runtimes
- [Github Actions](manual/README.scripts.html) - Notes about Actions run on to ensure quality
- [Testing](manual/README.test.html) - How testing is configured and how to run tests
- [Custom Webpack Loaders](manual/README.loaders.html) - Explaining how we configure webpack loaders to generate the application



.
