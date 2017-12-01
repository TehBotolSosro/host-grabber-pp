# Host Grabber ++
[![Build Status](https://travis-ci.org/rhadamanthe/host-grabber-pp.svg?branch=master)](https://travis-ci.org/rhadamanthe/host-grabber-pp)
[![License](https://img.shields.io/github/license/mashape/apistatus.svg)]()
&nbsp;
[![Firefox](docs/assets/images/firefox_x24.png)]()

A web extension that allows to find and download media files from web pages.  
It was originally designed for Mozilla Firefox but might be adapted to other web browsers.

It works like the former [Image Host Grabber](https://addons.mozilla.org/fr/firefox/addon/imagehost-grabber/)
extension, but unlike it, it is not restricted to downloading images.

> **This an alpha version**.

> Notice 1: user documentation will come soon.  
> Notice 2: the list of hosts has been seriously purged. Many hosts need to be readded.  
> Notice 3: links extraction is working quite correctly, but downloading is not yet
> perfect as Firefox API is very limited. I am thinking to relying on [Download Them All](https://www.downthemall.net/).


## Roadmap

* Add user documentation.
* Enhance the downloading part. Join the efforts with DTA is an option.
* Maybe adapt it for other web browsers.


## Development

Source code is available on Github.  
To test and debug it live, use...

CLI options:

```properties
# Install dependencies
npm install

# Execute tests
npm test

# Verifying linting
npm run lint

# Package the extension to submit it to addons.mozilla.org
npm run build
```

Testing in a separate browser:

* Make sure you have followed the previous instructions (CLI options).
* Then type in **npm run web-ext** in your terminal.
* A new instance of the browser will be launched.

Testing in your usual browser:

* Open **about:debugging** in Firefox.
* Click **Load Temporary Add-on** and select any file in the module's sources.


## Tesing the Documentation

```
cd docs/
docker run --rm --label=jekyll --volume=$(pwd):/srv/jekyll -it -p 4000:4000 jekyll/jekyll jekyll serve
```
