# Content

* [Overview](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues#overview)
* [Symptoms](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues#symptoms)
* [Diagnosis](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues#diagnosis) 
    * [Site speed problems](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues#site-speed-problems)
    * Page-specific problems
    * Database problems

## Overview

If your web application slows down or stuck, it's need to find the causes of this strange behavior. There are following main causes of the slowness of the web page:  
* is being caused by a problem on the machine level of your server:
    * Huge CPU load
    * Huge Memory load
    * Huge  value of Input/Output Operations on Hard Disk
* is being caused by a problem on the network level of your server:
    * Large files
    * Elements included from other servers
    * Plugins
* is being caused by a problem on the software level of your server:
    * not optimized code of the application
    * frequent "hard" requests to database
    * not use cache methods and services

And there are several methods to find the cause for it and most of them you can without any restrictions and with minimal knowledge about them, because every method has very detailed and full description and man pages.

## Symptoms

* Web page loads slowly.
* Elements of the page don't load.
* The page seems to "hang" before loading a certain element, and then loads quickly.

## Diagnosis

### Site speed problems

***

1. You need to know which application you are testing: [local or remote](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#remote-or-local-application). From this depends which method you will use for investigation: [a couple of them](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#local-tools) can be used in both cases, [others](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#remote-tools) - only for remote applications. Anyway, testing and analyzing speed of the your web application will help to find firsts signs of the problems in it.