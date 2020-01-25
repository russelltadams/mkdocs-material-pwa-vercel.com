## Mkdocs Material PWA

Welcome to Mkdocs Material PWA  

This is an example of how a PWA based on Mkdocs and Material theme deployed to [Zeit.co](https://zeit.co) can be done. I'll do my best to give you all the hints you need to get this off the ground yourself.  Further custimizations specific to your needs will need to be explored on your own, but this will be a pretty good base to start from.  

## Documentation Sources

You should be familiar with the following documentation sources, or get ready to!    
[- Mkdocs.org](https://mkdocs.org)  
[- Material for Mkdocs](https://squidfunk.github.io/mkdocs-material/)  
[- Zeit.co](https://zeit.co/docs)  

## Possible Use Cases

### Highlevel reasons to do this    

* Serverless setup  
* Git based content revisioning
* Markdown content source stays portable to many other frameworks
* Material design, nothing to do but add content  
* PWA example built-in, installable, with offline caching
* Deploy to Zeit.co for so much profit
* Deploy to Github pages easy like Sunday morning
* Local development server with one command
* No database  
 
### More Reasons

Mkdocs makes a great choice for turning markdown formated source files into a very nice, well orginized, easy to use statically generated HTML website. This is fun as it is well adapted to `serverless` setups if that is your thing. If that's not your thing, you could still take the rendered HTML and host it like a gray beard with Apache on your home built UNIX serveri at the local colo.
 
Mkdocs is also a cool choice for open-courseware or, in other words, writing neat and tidy little eBooks, or How-to webistes, that others can easily read and walk through a in orginized structured way. The poor-man's online classroom?  

Nothing to take care of except your content and perhaps occasionally updating/upgrading the Mkdocs bits if you want. Upgrading is as easy as doing a `pip install -r requirements.txt`. You'll only need to touch one other file, besides your content, for making customization if they are needed, which is `mkdocs.yml`.

The Material theme for Mkdocs is the bees knees. Its really quite remarkable how well it `just works`. It look wonderful on 23 inch flat screen displays and some how without any fuss shrinks itself to look fantastic on a mobile phone screen. 

Oh, did I mention the Progressive Web App? Yea, its pretty cool. Material theme already looks good in a mobile browser, but adding PWA capabilities is fun and can turn a good web-app-site into an installable app very easily.  If you are not convinced, at least consider the ability for your audiance to install the app to their phones for ease of access, and to get an offline experience, being able to access the content even if the internet/mobile network is not available. 

## Ok, Where Are The Real Docs?

Further documentation can be found in the repo [README.md](https://github.com/russelltadams/mkdocs-material-pwa-zeit.co)

## Credits

Some credit must go to [stavfx](https://github.com/stavfx) for encouraging me to check out PWA as possible solution for my idea, and for taking the time to listen to it.  
Some inspiration was derived [](https://github.com/Snickdx/pwadocs/) which didn't quite work for me but gave me a few hints on my way.  

