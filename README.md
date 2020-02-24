# mkdocs-material-pwa-zeit.co
An MkDocs-Material project with a PWA, ready for deployment with ZEIT Now  

## Build Status

[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co.svg?branch=master)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co) ![.github/workflows/link-checker.yml](https://github.com/russelltadams/mkdocs-material-pwa-zeit.co/workflows/.github/workflows/link-checker.yml/badge.svg) - Master branch  
[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co.svg?branch=develop)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co) ![.github/workflows/link-checker.yml](https://github.com/russelltadams/mkdocs-material-pwa-zeit.co/workflows/.github/workflows/link-checker.yml/badge.svg?branch=develop) - Develop branch  



## What's the point?

Read [here](https://github.com/russelltadams/mkdocs-material-pwa-zeit.co/blob/master/docs/index.md) for some background what this is and why you might want to do it if you are not already familiar with the parts of this little stack.

* Mkdocs - Markdown to static html [http://mkdocs.org](http://mkdocs.org)
* Material theme for MkDocs - [https://squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/)
* PWA builder for helpful PWA bits - [https://www.pwabuilder.com/](https://www.pwabuilder.com/)  
* Zeit serverless hosting - [https://zeit.co](https://zeit.co)  

### Demo Sites

[https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/](https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/) - master  
[https://mkdocs-material-pwa-zeitco-git-develop.russelltadams.now.sh/](https://mkdocs-material-pwa-zeitco-git-develop.russelltadams.now.sh/) - develop

## Setup

This assumes you have forked, or copied `mkdocs-material-pwa-zeit.co` to your own Github repo.   

### Local Development

```shell
  mkvirtualenv mkdocs
  workon mkdocs
  pip install -r requirements.txt
  mkdocs serve
```
The use of python virtual environment is optional but highly recommended.

If you can get through the above, solving any complaints you run into, you should end up with the local development server running. This is super cool as you can now make changes to you mkdocs setup (mkdocs.yml) or your content (the markdown docs in /docs) and the "web server" will load the changes live when you save the file. Open your browser to `http://127.0.0.1:8000/`.

Now while the server is running, and you have the home page open in the browser, make changes to and save `/docs/index.md`. The server should automatically reload and show your changes.

## Zeit.co serverless hosting and Github integration

Get an account on [Zeit.co](https://zeit.co).  It's free, they currently do not ask for any CC information to get signed up, and the free account allows plenty of room for developing multiple apps, and even running them in production at small scales.

### Zeit Github Integration

Connect your Zeit account to your Github account following the instructions after logging into Zeit. Create a new project in Zeit pointing it at your copy of this repo in your Github account. By default your `master` branch in Github will be considered the production release, but commits to other branches like `develop` will be pulled and built to preview. You can of course change these setting if you desire.

### Next steps for Zeit fanciness

Setup a custom domain(s) attached to the desired branch(es). You will need to point your domain registrar towards Zeit DNS servers. Zeit will give you a list of DNS servers after you submit your domain in the project.

## Test the PWA

Easy way to test the PWA bits is to use Google Chrome Developer tools built into Chrome.

1. In Google Chrome, go to the URL you want to audit. You can audit any URL on the web.
1. Open Chrome DevTools.
1. Click the Audits tab.
1. Make sure PWA is selected, run the Audits  

That will give the basic validation. DevTools can show you much more if you dig around.   

## To-Do

* Explain the PWA bits (manifest, service worker, and supporting bits)
* Add some `Hipster Ipsum` to the demo content to show off the power of the material theme, or make the pages long enough that the TOC comes into play  
* Add some kind of notification or link to let the user know you can install the PWA. Chrome has a notification if you notice it, but I am not sure how other browser handle this if at all  
* Play with the `now` stuff that Zeit provides  
* Change theme colors perhaps so they aren't the Material default

## Contribute?

Yes please. If you see an error, or something that could be better, or have an idea to enhance the concept here, feel free to fork, branch and PR, or raise an issue. Thanks!
