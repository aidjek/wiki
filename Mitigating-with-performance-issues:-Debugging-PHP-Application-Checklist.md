# Content

* [Overview](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#overview)
* [Get Application Settings](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#get-application-settings)
    * [PHP Settings Information](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#php-settings-information)
    * [APC PHP Status](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#apc-php-status)
    * [Memcached PHP Status](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#memcached-php-status)
* [Benchmark Your Application](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#benchmark-your-application)
    * [Siege Benchmark](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#siege-benchmark)
    * [Apache Bench](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#apache-bench)
* [Enable Debug on Server or Client side?](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#enable-debug-on-server-or-client-side)
* [Tools for Diagnostic](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#tools-for-diagnostic)
    * [Server Side Tools](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#server-side-tools)
        * [XDebug](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug)
            * [XDebug and Integrated development environments (IDE) ](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-integrated-development-environments-ide)
                * [XDebug and Eclipse](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-eclipse)
                * [XDebug and PHPStorm](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-phpstorm)
                * [XDebug and NetBeans](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-netbeans)
                * [XDebug and Zend Studio](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-zend-studio)
            * [XDebug and Webgrind](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-webgrind)
            * [XDebug and KCachegrind](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-kcachegrind)
        * [XHProf and XHGui](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xhprof-and-xhgui)
    * [Client Side Tools](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#client-side-tools)
        * [Firefox with Firebug and FirePHP Add-ons](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#firefox-with-firebug-and-firephp-add-ons)
        * [Google Chrome with Developer Tools and PHP Console extension](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#google-chrome-with-developer-tools-and-php-console-extension)

## Overview

To identify which elements are slowing down your web page, you should use some additional diagnostic methods or tools to benchmarking or to break down your page load into individual items. Web pages, which are using PHP code can contain some of complex elements which increase the overall load time of the web page and this not depends from how powerful is host, where this PHP application works.
Before debugging of PHP application we need to get some information about PHP settings, may be load several benchmarks and decide, as for and Debugging Site Speed Checklist, on which side - [SERVER](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#server-side-tools) (which has [XDebug tool](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug) with implementation it [for different cases](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xdebug-and-integrated-development-environments-ide) and [XProf with XHGui](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#xhprof-and-xhgui) ) or [CLIENT](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#client-side-tools) (which are based on the features of the browser and their extensions, like [Firebug and FirePHP](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#firefox-with-firebug-and-firephp-add-ons) or [Google Chrome Developer Tools and PHP Console](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-PHP-Application-Checklist#google-chrome-with-developer-tools-and-php-console-extension) ) will use  methods and tools for debugging.

## Get Application Settings

### PHP Settings Information

***

**[phpinfo](http://www.inmotionhosting.com/support/website/php/create-phpinfo-page-to-see-php-settings)**

### APC PHP Status

***

**[apc status](http://alvinalexander.com/php/how-display-apc-cache-information-installation-test)**
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/apc_status.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/apc_status.png)

### Memcached PHP Status

***

**[memcached status](http://livebookmark.net/journal/2008/05/21/memcachephp-stats-like-apcphp/)**
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/memcache_status.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/memcache_status.png)

## Benchmark Your Application

### Siege Benchmark

***

to benchmark your application one of the best tools is **[Siege](http://www.joedog.org/siege-readme/)** 

### Apache Bench

***

and **[Apache Bench](http://httpd.apache.org/docs/2.2/programs/ab.html)**

## Enable Debug on Server or Client side?

## Tools for Diagnostic

### Server Side Tools

***

On the server side to debug PHP application we can use following useful tools, like:

#### XDebug
another of the powerful debug utility is **[Xdebug](http://www.xdebug.org/docs/)**

##### XDebug and Integrated development environments (IDE)
###### XDebug and Eclipse

***

which can be use with any IDE like **[Eclipse](http://techmania.wordpress.com/2008/07/02/debugging-php-in-eclipse-using-xdebug/)**

###### XDebug and PHPStorm

***

 **[PHPStorm](https://www.jetbrains.com/phpstorm/webhelp/configuring-xdebug.html)**

###### XDebug and NetBeans

***

 **[NetBeans](http://wiki.netbeans.org/HowToConfigureXDebug)**

###### XDebug and Zend Studio
 **[Zend Studio](http://vitalflux.com/configure-xdebug-debugger-for-zend-studio/)**

##### XDebug and Webgrind

***

to inspect the result of Xdebug you can use **[Webgrind](https://github.com/jokkedk/webgrind)**
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/webgrind.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/webgrind.png)

##### XDebug and KCachegrind

***

Xdebug generates cachegrind-compatible files which can also be used to create easy-to-understand graphs using **[KCachegrind](http://kcachegrind.sourceforge.net/html/Home.html)**.
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/kcachegrind.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/kcachegrind.png)

#### XHProf and XHGui

***

Xdebug is a very good tool to check where your bottlenecks are in development, but for production you can try to use **[XHProf](http://pecl.php.net/package/xhprof)** with **[XHGui](https://github.com/perftools/xhgui)**
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/xhgui.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/xhgui.png)

### Client Side Tools

***

On the client side to debug PHP application we can use following useful tools, like:  

#### Firefox with Firebug and FirePHP Add-ons

***

 **[Firebug](http://getfirebug.com/whatisfirebug)** and **[FirePHP](http://www.firephp.org/)** applications

#### Google Chrome with Developer Tools and PHP Console extension

***

**[Google Chrome Developer Tools](https://developers.google.com/chrome-developer-tools/)** and **[PHP Console](https://chrome.google.com/webstore/detail/php-console/nfhmhhlpfleoednkpnnnkolmclajemef)**