# NodeJS
> - How does Browser Gets JS Files and who exavctly runs JS in Browser
> - What is JS Engine
> - What are the roles played by JS Engine and EventLoop in JS RunTime Environment
> - What is NodeJS


### How does Browser Gets JS Files and runs them ?
***
All the Browser have common mechanism for getting JS Files to them from the ***Hosted Server*** (HS). This mechanism starts by getting html file from HS which may or may not contain script tags to JS files, if they do have them Browser requests those files (Either CSS or JS files) to HS and gets them. 

Based on the JS code triggering point, the *JS Engine* takes the JOB of running that JS.

### What is JS Engine ?
***
JS Engine is a *Computer Program* that can run JavaScript.  Each Browser uses one of the JS Engines to run JS. 
| Browser| Engine |
| -|:-|
| Chrome|V8|
|Firefox|SpiderMonkey|
|Edge & IE|Chakra|
|Safari|Nitro|
|Opera|Futhark|
Above are some Browser specific JS Engines List.
These are responsible in ***Memory Allocation and Execution*** your JS code.

***V8 Engine***
It is being used by Chrome. It is an Open Source Library written in C++. It can run standalone and can be embedded into any C++ application. It implemets [ECMAScript](https://en.wikipedia.org/wiki/ECMAScript) as specified in ECMA-262.
 
Here comes the Question for you !!!
> As it is Open Source Library, can we run Complete JS by providing C++ env to V8 ?

Most answers would reflect **YES** since it runs JS. 
***But***
it can not run Complete JS. Since, Observing the code base of V8, no clues related to vital terms of modern JS run time like handling HTTP Requests, EventLoop, DOM events, Timers etc.. get detected. So there is something beyond V8 which deal above things.

### What are the roles played by JS Engine and EventLoop in JS RunTime Environment ?
***
***JS Runtime ENV***
This env plays bright role in making JS App efficient. This contains Four Major Parts to get into:
![JS RunTime Env](https://s3.amazonaws.com/media-p.slid.es/uploads/1011920/images/5841485/JS_Runtime.png)

1. JS Engine
	This doesn't require any introduction since this got injected into your brain just above our current section.
2. EventLoop
3. WebAPIs
4. Callback Queue
