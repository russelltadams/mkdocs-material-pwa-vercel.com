# mkdocs-material-pwa-vercel.com
An MkDocs-Material project with a PWA, ready for deployment to Vercel  

## Build Status

[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com.svg?branch=master)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com ) ![.github/workflows/link-checker.yml](https://github.com/russelltadams/mkdocs-material-pwa-vercel.com/workflows/.github/workflows/link-checker.yml/badge.svg) - Master branch  
[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com.svg?branch=develop)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-vercel.com ) ![.github/workflows/link-checker.yml](https://github.com/russelltadams/mkdocs-material-pwa-vercel.com/workflows/.github/workflows/link-checker.yml/badge.svg?branch=develop) - Develop branch  



## What's the point?

Read [here](https://github.com/russelltadams/mkdocs-material-pwa-vercel.com/blob/master/docs/index.md) for some background what this is and why you might want to do it if you are not already familiar with the parts of this little stack.

* Mkdocs - Markdown to static html [http://mkdocs.org](http://mkdocs.org)
* Material theme for MkDocs - [https://squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/)
* PWA builder for helpful PWA bits - [https://www.pwabuilder.com/](https://www.pwabuilder.com/)  
* Vercel serverless hosting - [https://vercel.com ](https://vercel.com )  

### Demo Sites

[https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/](https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/) - master  
[https://mkdocs-material-pwa-zeitco-git-develop.russelltadams.now.sh/](https://mkdocs-material-pwa-zeitco-git-develop.russelltadams.now.sh/) - develop

## Setup

This assumes you have forked, or copied `mkdocs-material-pwa-vercel.com ` to your own Github repo.   

### Local Development

The recent latest versions of Mkdocs have moved beyond python 2.x, and now require Python 3.5 and beyond. Python 3.8.x works fine.  

```shell
  mkvirtualenv --python=`which python3` mkdocs
  mkvirtualenv mkdocs
  workon mkdocs
  pip install -r requirements.txt
  mkdocs serve
```
The use of python virtual environment is optional but highly recommended.

If you can get through the above, solving any complaints you run into, you should end up with the local development server running. This is super cool as you can now make changes to you mkdocs setup (mkdocs.yml) or your content (the markdown docs in /docs) and the "web server" will load the changes live when you save the file. Open your browser to `http://127.0.0.1:8000/`.

Now while the server is running, and you have the home page open in the browser, make changes to and save `/docs/index.md`. The server should automatically reload and show your changes.

## vercel.com  serverless hosting and Github integration

Get an account on [vercel.com ](https://vercel.com ).  It's free, they currently do not ask for any CC information to get signed up, and the free account allows plenty of room for developing multiple apps, and even running them in production at small scales.

### Vercel Github Integration

Connect your Vercel account to your Github account following the instructions after logging into Vercel. Create a new project in Vercel pointing it at your copy of this repo in your Github account. By default your `master` branch in Github will be considered the production release, but commits to other branches like `develop` will be pulled and built to preview. You can of course change these setting if you desire.

### Next steps for Vercel fanciness

Setup a custom domain(s) attached to the desired branch(es). You will need to point your domain registrar towards Vercel DNS servers. Vercel will give you a list of DNS servers after you submit your domain in the project.

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

## Contribute?

Yes please. If you see an error, or something that could be better, or have an idea to enhance the concept here, feel free to fork, branch and PR, or raise an issue. Thanks!
