# Content

* [Overview](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#overview)
* [Remote or Local application?](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#remote-or-local-application)
* [Tools for Diagnostic](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#tools-for-diagnostic)
    * [Remote Tools](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#remote-tools)
        * [Ping and Traceroute](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#ping-and-traceroute)
        * [DNS Health](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#dns-health)
        * [Google PageSpeed Insights](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#google-pagespeed-insights)
        * [WebPage Performance Test](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#webpage-performance-test)
        * [Pingdom Website Speed Test](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#pingdom-website-speed-test)
    * [Local Tools](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#local-tools)
        * [Firefox with Firebug and YSlow Add-ons](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#firefox-with-firebug-and-yslow-add-ons)
        * [Google Chrome with Developer Tools and PageSpeed Insights extension](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#google-chrome-with-developer-tools-and-pagespeed-insights-extension)

## Overview

There are a lot of causes for web page is slowing down and a lot of tools, which can help to find the most  long time loadable elements of your site and it's bottlenecks. But if your web application slows down, the first step which needs to execute: to check which version of application [remote or local](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#remote-or-local-application), are you using? 

## Remote or Local application?

From the network type of application will depend and method of it's testing and analyzing. There are specific tools for [REMOTE](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#remote-tools) (begging from simple [Ping and Traceroute](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#ping-and-traceroute), [DNS health checkers](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#dns-health) and ending specific software, which testing live your site: [Google PageSpeed Insights](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#google-pagespeed-insights), [WebPage Performance Test](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#webpage-performance-test), [Pingdom Website Speed Test](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#pingdom-website-speed-test) ) and [LOCAL](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#local-tools)  (which are based on the features of the browser and their extensions, like [Firebug and YSlow](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#firefox-with-firebug-and-yslow-add-ons) or [Google Chrome Developer Tools and PageSpeed Insights](https://github.com/clevertech/wiki/wiki/Mitigating-with-performance-issues:-Debugging-Site-Speed-Checklist#google-chrome-with-developer-tools-and-pagespeed-insights-extension) ) connection to web application.

## Tools for Diagnostic

### Remote Tools:

***

More of those tools make possibility to test your remote application with a lot of tests for speed and present analysis of those tests with recommendation for optimization.
Let's meet with Diagnostics Tools for Remote Application:

#### Ping and Traceroute

***

The most simple and first self-testing utilities, can help us to understand if our application is available. Can execute it from our local system with simple commands:  
`ping ip/hostname`  
`tracert ip/hostname` for Windows  
`traceroute ip/hostname` for Linux/MacOS X  
 also I can recommend to use for Linux/MacOS X [My TraceRoute utility](http://www.bitwizard.nl/mtr/) and for Windows [WinMTR](http://winmtr.net/)
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/mtr_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/mtr_clevertech.png)

Of course there are and online utility with more features, like make a ping [from 50 worldwide locations](http://cloudmonitor.ca.com/en/ping.php), [multiply worldwide locations](http://www.super-ping.com/) and useful [http://www.pingtest.net/](http://www.pingtest.net/)

#### DNS Health

***

Domain Name System Health is playing one of important roles too. You can use tools from your system like `nslookup` and `dig` or online tools: [check DNS working from worldwide locations](https://www.whatsmydns.net/) 
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/whatsmydns_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/whatsmydns_clevertech.png)

and [check current issues with DNS zone](http://www.dnsstuff.com/)
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/dns_stuff_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/dns_stuff_clevertech.png)

#### Google PageSpeed Insights

***


If you want to test your remote web application with outsider tools, firstly we can recommend to use specific tool from [Google PageSpeed Insights](http://developers.google.com/speed/pagespeed/insights/). This tool performs a several tests for Speed and User Experience for Mobile and Desktop version of the site.
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/pagespeed_insights_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/pagespeed_insights_clevertech.png)

#### WebPage Performance Test

***


For more advanced statistics and tests you can use [WebPage Performance Test](http://www.webpagetest.org/) which give possibility to test your remote app from a lot of locations and for different browsers environment. Also it give possibility to perform test of your remote app on [Mobile Device powered by Akamai](http://www.webpagetest.org/mobile) 
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/web_page_test_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/web_page_test_clevertech.png)

#### Pingdom Website Speed Test

***

And one more tools for test your remote app is [Pingdom Website Speed Test](http://tools.pingdom.com/fpt/), which make possibility to test speed of every component of the site and presents full analysis about this.
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/pingdom_website_test_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/pingdom_website_test_clevertech.png)

### Local Tools:

***

More of those tools make possibility to test your local application with using capabilities of your browser or IDE. Let's meet with Diagnostics Tools for Local Application:

#### Firefox with Firebug and YSlow Add-ons

***

If you are using Firefox Browser the best tool for check site speed is [Firebug](http://getfirebug.com/), which make possibility to check your local and remote website components speed.
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/firebug_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/firebug_clevertech.png)

But using an add-on [YSlow](https://addons.mozilla.org/en-US/firefox/addon/yslow/) can show and analysis for speed of the components of the website.
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/yslow_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/yslow_clevertech.png)

Also I want to pay attention that YSlow can be use and [for Google Chrome Browser too](https://chrome.google.com/webstore/detail/yslow/ninejjcohidippngpapiilnmkgllmakh)

#### Google Chrome with Developer Tools and PageSpeed Insights extension

***

If you are using Google Chrome Browser the best tool for check site speed it is native feature of the browser, as [Chrome Developer Tools](https://developers.google.com/chrome-developer-tools/)
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/google_developer_tools_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/google_developer_tools_clevertech.png)

And of course this Tools can be supplemented by extension also from Google, which is can analyze website speed and was previously mentioned like [PageSpeed Insights](https://chrome.google.com/webstore/detail/pagespeed-insights-by-goo/gplegfbjlmmehdoakndmohflojccocli)
![https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/pagespeed_clevertech.png](https://s3.amazonaws.com/clevertech-files/images_for_wiki/mitigating_with_performance_issues/pagespeed_clevertech.png)
