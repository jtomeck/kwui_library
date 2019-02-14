KW UI Design Library
==============

https://jtomeck.github.io/kwui_library

---

### Building & running locally

##### Using Vagrant

With [Vagrant](https://www.vagrantup.com/) and [Virtualbox](https://www.virtualbox.org/) installed, do:
```
vagrant up
```
Once that's done, which will take a while the first time through, do:
```
vagrant ssh
cd /vagrant
```

Now, skip ahead to [Running the documentation](#running-the-documentation).



##### Not using Vagrant
You will need to [install Jekyll](http://jekyllrb.com/docs/installation/). You will also need to [install Node.js](http://nodejs.org/download/). Node.js powers the front-end build and dependency management tools [Grunt](http://gruntjs.com/) and [Bower](http://bower.io/).

Once Jekyll and Node.js are installed, ensure you have Grunt and Bower installed globally with:
```
npm install grunt-cli -g
npm install bower -g
```

Then install the project's dependencies with:
```
npm install
bower install
```
---
#### Running the documentation
This project can be built with SASS(Beta) or LESS. The SASS assets are currently in beta and you may encounter minor correctable visual bugs.

To build the front-end assets (LESS/CSS/JS) with:
```
grunt build
```

(Beta) To build the front-end assets (SASS/CSS/JS) with:
```
grunt buildSass
```
 __Note:__ The SASS files require your project to install [Bootstrap Sass](https://github.com/twbs/bootstrap-sass) with NPM. The SASS files are looking for a 'node_modules' folder.

Run the project with Jekyll:
```
jekyll serve
```
This starts Jekyll, which compiles the markdown files into static html files, starts a server for you to view the documentation at, as well as watches for changes and recompiles.


##### Distribution Builds
After running `grunt build` and `jekyll build`, you will have a `_site` folder that contains the entire static site and resources.
