## Webpaige Foundation [![Build Status](https://travis-ci.org/askcs/webpaige-foundation.png?branch=master)](https://travis-ci.org/askcs/webpaige-foundation)

---

### Foundation framework of WebPaige projects

A **compilation boilerplate** based AngularJS, Generator-Angular for Yeoman, Angular-Seed, RequireJS, Jade, SASS, Twitter Bootstrap, HTML5 Boilerplate and many handy Grunt plugins for making development processes streamlined.


### Installation
Please complete the steps to setup project on your local development environment. This is a one time setup process.

1. Please make sure that **Node** is installed, otherwise please use this link to [download and install](http://nodejs.org/).

2. You will be needing **Ruby** for compiling SASS'ed style documents to distribution folders. 

	Ruby is already installed on most **Mac and Linux platforms**. 
	
	**Windows users** please use [this link to download and install](http://rubyinstaller.org/) Ruby on your Windows machine.

	Test if Ruby is installed on your command line with;
		
		ruby -version
		
3. **Compass and SASS** gem for Ruby is needed to run SASS compilers on Ruby. Please install them through your command line.
	
	On **Windows**;
	
		gem install compass
		
	On **OSX / Linux** (You may need to authorize the installation);
	
		sudo gem install compass
		
4. After above stated steps are completed, which means that your development environment is ready to setup the project. 

	Please install **Grunt** and **Bower** for managing your watchers, compilers, test frameworks and runners, servers and dependency management.

		npm install -g grunt-cli bower
	
5. We will be fetching **node dependencies** and Grunt plugins with;

		npm install
		
6. Please install **third-libraries** with **Bower** as well;

		bower install 
		
7. At this stage project should have been installed and ready to be run. Please run your web server with (on `http://localhost:9000/`);

		grunt server



### Development workflow

* Please **start your webserver** with;

		grunt server

* **Build a distribution package **with;

		grunt build
		
* To **start webserver from distribuition folder**, please use;

		grunt server:dist
		
* To **initialise unit tests** please use;

		grunt karma:unit
		
	Default test runner for unit tests is **PhantomJS**. Please refer to section about PhantomJs for installation instructions below. Please change **karma.conf.js** file under the root directory. You can change browsers variable to use your preferable browser(s). 
	
	Available browsers are `Chrome`, `ChromeCanary`, `Firefox`, `PhantomJS` (headless browser) and `Internet Explorer`. (For using internet explorer you will be needing to install ie launcher. Please use; **npm install karma-ie-launcher** and and add **karma-ie-launcher** in the plugins variable of the config file.)	
	
		
* For initialising end-to-end tests please use;

		grunt karma:end

* For **automated releases** please use;

		grunt patch
		
		grunt minor
		
		grunt major


### PhantomJS
In order for the unit task to work properly, [PhantomJS](http://www.phantomjs.org/) should be installed (unless an another browser selected) and in the system PATH (if you can run "phantomjs" at the command line, this task should work).

Unfortunately, PhantomJS cannot be installed automatically via npm or grunt, so you need to install it yourself. There are a number of ways to install PhantomJS.

* [PhantomJS and Mac OS X](http://ariya.ofilabs.com/2012/02/phantomjs-and-mac-os-x.html)
* [PhantomJS Installation](http://code.google.com/p/phantomjs/wiki/Installation) (PhantomJS wiki)

Note that the `phantomjs` executable needs to be in the system `PATH` for grunt to see it.

* [How to set the path and environment variables in Windows](http://www.computerhope.com/issues/ch000549.htm)
* [Where does $PATH get set in OS X 10.6 Snow Leopard?](http://superuser.com/questions/69130/where-does-path-get-set-in-os-x-10-6-snow-leopard)
* [How do I change the PATH variable in Linux](https://www.google.com/search?q=How+do+I+change+the+PATH+variable+in+Linux)


### Git Commit Message Conventions
There is a special `Grunt` plugin is installed and running for generating `CHANGELOG.md` logs by script. 

Which allows allow ignoring commits by git bisect (not important commits like formatting) and provide better information when browsing the history.

These three sections in changelog: new features, bug fixes, breaking changes.

This list could be generated by script when doing a release. Along with links to related commits.

**Format of the commit message**

	**-type-**(**-scope-**): **-subject-**

Allowed **-type-**

	- feat (feature)
	- fix (bug fix)
	- docs (documentation)
	- style (formatting, missing semi colons, …)
	- refactor
	- test (when adding missing tests)
	- chore (maintain)
	
Allowed **-scope-**

	Scope is optional and could be anything specifying place 	of the commit 	change. For example function or class 	names or file names etc...

**-subject-** text	

	Subject line should contain succinct description of the 	change.
	
	Try to use imperative, present tense: “change” not 	“changed” nor “changes” and don't capitalize first letter 	or no dot (.) at the end. 
	
	Just as in <subject> use imperative, present tense: 	“change” not “changed” nor “changes”

	includes motivation for the change and contrasts with 	previous behavior

Please [refer to this documentation](https://docs.google.com/a/ask-cs.com/document/d/1QrDFcIiPjSLDn3EL15IJygNPiHORgU1_OOAqWjiDU5Y/edit#heading=h.em2hiij8p46d) for more information on these conventions. 


### Credits
Projects and frameworks has been used for making this;

* AngularJS
* Generator-Angular for Yeoman
* Angular-Seed
* RequireJS
* Jade
* Bootstrap-SASS
* Twitter Bootstrap 3
* HTML5 Boilerplate
* Many other Grunt plugins.