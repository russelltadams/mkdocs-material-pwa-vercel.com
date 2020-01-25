# mkdocs-material-pwa-zeit.co
An MkDocs-Material project with a PWA, ready for deployment with ZEIT Now  

## Build Status

[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co.svg?branch=master)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co) - Master branch  
[![Build Status](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co.svg?branch=develop)](https://travis-ci.org/russelltadams/mkdocs-material-pwa-zeit.co) - Develop branch  

## What's the point?

Read [here](https://github.com/russelltadams/mkdocs-material-pwa-zeit.co/blob/master/docs/index.md) for some background what this is and why you might want to do it if you are not already familiar with the parts of this little stack.

### Demo?

[https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/](https://mkdocs-material-pwa-zeitco.russelltadams.now.sh/)  

## Setup

Fork this repo, or in some other manner copy the contents into a repo of your own. I like to use virtualenv (virtual python environments) on my laptop, I recommended it. If you have a system with the virtualenv tools setup on your system simply follow the commands. If not improvise or use some other form of development environment separation to keep your python environment sane.

```
  mkvirtualenv mkdocs
  workon mkdocs
  pip install -r requirements.txt
  mkdocs serve
```

If you can get through the above, solving any complaints you run into, you should end up with a development server that is built into mkdocs running. This is super cool as you can not make changes to you mkdocs setup (mkdocs.yml) or your content (the markdown docs in /docs) and the "web server" will load the changes live when you save the file. Open your browser to `http://127.0.0.1:8000/`  

Now while the server is running, and you have the home page open in the browser, make changes to and save `/docs/index.md`. The server should automatically reload and show your changes. Cool! Your local dev flow is setup!

## Zeit.co serverless hosting and Github integration

Get an account on Zeit.co.  It's free, they currently do not ask for any CC information to get signed up, and the free account allows plenty of room for developing multiple apps, and even running them in production at small scales. You wont need to pay them a dime unitl your site goes viral or you get "slash-dotted", here is the break down of free stuff:

### Zeit Free Stuff

* Free SSL via Let's Encrypt  
* Custom domains  
* Push to deploy, Github, Gitlab, and Bitbucket  
* Unlimited deployments  
* 23 world wide CDN locations (Cloud Flare!)   

### Zeit Free Account Restrictions  

* 100 deployments per day  
* Deployment history limited to 10 per project  
* 20 GB transfer a month  
* 100MB log storage  

Not bad.

### Github Integration

Signup, then connect your Zeit account to your Github account following the instructions. Create a new project in Zeit pointing it at your copy of this repo in your Github account. Now, by default your `master` branch in Github will be considered production, but commits to other branches like `develop` will be pulled and built. Zeit will provide a nice <mythings>.sh.co url to see the output of your deployment build. There is also a very handy `build` and `runtime` logs available to look for errors is the build. There is also a `source` and `output` view which is super awesome for understanding what the actual output was if the build succeeds but the "app" or "site" that was built shows you something unexpected.

### Next steps for Zeit fanciness

Setup a custom domain(s) attached to the desired branch(es). You will need to point your domain registrar towards Zeit DNS servers. Zeit will give you a list of DNS servers after you submit your domain in the project. 

## Test the PWA

coming soon. 

## To-Do

* Explain the PWA bits (manifest, service worker, and supporting bits)
* Add some `Hipster Ipsum` to the demo content to show off the power of the material theme, or make the pages long enough that the TOC comes into play  
* Add some kind of notification or link to let the user know you can install the PWA. Chrome has a notification if you notice it, but I am not sure how other browser handle this if at all  
* Play witht the `now` stuff that Zeit provides  
* Change theme colors perhaps so they aren't the Material default  

 
