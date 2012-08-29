[Bootstrap for KISS Web Design](https://github.com/KISS-Web-Design/bootstrap)
=============================
  
This project is based on, and incorporates all code/markup from twiter/bootstrap 2.1.0
  
How this differs from Twitter Bootstrap  
=======================================  
  
This file
---------  
The readme.MD file you are reading is different from the original projects readme.md, as it contains a summary of the changes made to the project that differentiate it from the orginal.  

Uses rem units as well as px
----------------------------
LESS Changes to output font-size, line-height and height in rem as well as px (px is only used if the browser does not support rem units)  

References regarding the use and understanding of rem units.  
W3C, Understanding WCAG 2.0, Resize Text states "Ensuring that text containers resize when the text resizes AND using measurements that are relative to other measurements in the content..."  
Detailed explanation: [http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-scale.html](http://www.w3.org/TR/UNDERSTANDING-WCAG20/visual-audio-contrast-scale.html)  
W3C quick overview: [http://www.w3.org/WAI/WCAG20/quickref/Overview.php#visual-audio-contrast](http://www.w3.org/WAI/WCAG20/quickref/Overview.php#visual-audio-contrast)    
Using rem units: [http://snook.ca/archives/html_and_css/font-size-with-rem](http://snook.ca/archives/html_and_css/font-size-with-rem)    
Web Accessibility for Designers infographic: [http://webaim.org/resources/designers/](http://webaim.org/resources/designers/)  
  
Alternative useage for tooltips  
-------------------------------  
Added js tooltip function so a tooltip can be called without using rel="tooltip"  
Update tooltip explanation/useage html to reflect and explain the new function  
Using rel="tooltip" causes a W3C validation error because "tooltip" is not a valid attibute.  
It generates the following failure: "Error: Bad value tooltip for attribute rel on element a: Keyword tooltip is not registered."

References for HTML links and valid rel attributes/keywords.
Valid HTML4 keywords from W3C: [http://www.w3.org/TR/html4/types.html#h-6.12](http://www.w3.org/TR/html4/types.html#h-6.12)  
HTML4 link structure from W3C: [http://www.w3.org/TR/html4/struct/links.html](http://www.w3.org/TR/html4/struct/links.html)  
Valid HTML5 keywords from W3C (Editors draft): [http://dev.w3.org/html5/spec/single-page.html#linkTypes](http://dev.w3.org/html5/spec/single-page.html#linkTypes)  
HTML5 ink structure from W3C (Editors draft): [http://dev.w3.org/html5/spec/single-page.html#the-link-element](http://dev.w3.org/html5/spec/single-page.html#the-link-element)  
Valid HTML5 keywords from WhatWG live document: [http://www.whatwg.org/specs/web-apps/current-work/multipage/links.html#linkTypes](http://www.whatwg.org/specs/web-apps/current-work/multipage/links.html#linkTypes)  
HTML5 link structure from WhatWG live document: [http://www.whatwg.org/specs/web-apps/current-work/multipage/links.html#links](http://www.whatwg.org/specs/web-apps/current-work/multipage/links.html#links)  

Items removed  
-------------  
 - All build files
   + /docs/build (folder)
   + /docs/template (folder)
   + /Makefile (file)
   + /package.json (file)
 - /img (folder)
 - /js (folder)
 - /docs/assets/bootstrap.zip (file)
  
All other contents in the /docs folder have been retained, only the changes listed above have been made.
All the LESS files have been retained, only the changes listed above have been made. The LESS files can be re-used on any project that wants to use those changes.

Items added  
-----------  
 - /docs/bootstrap.zip (file): contains all the files needed to run bootstrap on a webserver.
  
  
Live website  
------------  
Live example at [http://twitterbootstrap.stempsite.co.uk/](http://twitterbootstrap.stempsite.co.uk/)  
  
  
[Forked from Twitter Bootstrap](http://twitter.github.com/bootstrap)  
=============================  
  
Bootstrap is a sleek, intuitive, and powerful front-end framework for faster and easier web development, created and maintained by [Mark Otto](http://twitter.com/mdo) and [Jacob Thornton](http://twitter.com/fat) at Twitter.  
  
To get started, checkout http://getbootstrap.com!  
  
  
  
Quick start  
-----------  
  
Clone the repo, `git clone git://github.com/twitter/bootstrap.git`, or [download the latest release](https://github.com/twitter/bootstrap/zipball/master).  
  
  
  
Versioning  
----------  
  
For transparency and insight into our release cycle, and for striving to maintain backward compatibility, Bootstrap will be maintained under the Semantic Versioning guidelines as much as possible.  
  
Releases will be numbered with the following format:  
  
`<major>.<minor>.<patch>`  
  
And constructed with the following guidelines:  
  
* Breaking backward compatibility bumps the major (and resets the minor and patch)  
* New additions without breaking backward compatibility bumps the minor (and resets the patch)  
* Bug fixes and misc changes bumps the patch  
  
For more information on SemVer, please visit http://semver.org/.  
  
  
  
Bug tracker  
-----------  
  
Have a bug? Please create an issue here on GitHub that conforms with [necolas's guidelines](https://github.com/necolas/issue-guidelines).  
  
https://github.com/twitter/bootstrap/issues  
  
  
  
Twitter account  
---------------  
  
Keep up to date on announcements and more by following Bootstrap on Twitter, [@TwBootstrap](http://twitter.com/TwBootstrap).  
  
  
  
Blog  
----  
  
Read more detailed announcements, discussions, and more on [The Official Twitter Bootstrap Blog](http://blog.getbootstrap.com).  
  
  
  
Mailing list  
------------  
  
Have a question? Ask on our mailing list!  
  
twitter-bootstrap@googlegroups.com  
  
http://groups.google.com/group/twitter-bootstrap  
  
  
  
IRC  
---  
  
Server: irc.freenode.net  
  
Channel: ##twitter-bootstrap (the double ## is not a typo)  
  
  
  
Developers  
----------  
  
We have included a makefile with convenience methods for working with the Bootstrap library.  
  
+ **dependencies**  
Our makefile depends on you having recess, connect, uglify.js, and jshint installed. To install, just run the following command in npm:  
  
```  
$ npm install recess connect uglify-js jshint -g  
```  
  
+ **build** - `make`  
Runs the recess compiler to rebuild the `/less` files and compiles the docs pages. Requires recess and uglify-js. <a href="http://twitter.github.com/bootstrap/less.html#compiling">Read more in our docs &raquo;</a>  
  
+ **test** - `make test`  
Runs jshint and qunit tests headlessly in [phatomjs] (http://code.google.com/p/phantomjs/) (used for ci). Depends on having phantomjs installed.  
  
+ **watch** - `make watch`  
This is a convenience method for watching just Less files and automatically building them whenever you save. Requires the Watchr gem.  
  
  
  
Contributing  
------------  
  
Please submit all pull requests against *-wip branches. If your unit test contains javascript patches or features, you must include relevant unit tests. Thanks!  
  
  
  
Authors  
-------  
  
**Mark Otto**  
  
+ http://twitter.com/mdo  
+ http://github.com/markdotto  
  
**Jacob Thornton**  
  
+ http://twitter.com/fat  
+ http://github.com/fat  
  
  
  
Copyright and license  
---------------------  
  
Copyright 2012 Twitter, Inc.  
  
Licensed under the Apache License, Version 2.0 (the "License");  
you may not use this work except in compliance with the License.  
You may obtain a copy of the License in the LICENSE file, or at:  
  
   http://www.apache.org/licenses/LICENSE-2.0  
  
Unless required by applicable law or agreed to in writing, software  
distributed under the License is distributed on an "AS IS" BASIS,  
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.  
See the License for the specific language governing permissions and  
limitations under the License.