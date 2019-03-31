# NodeJS
> - How does Browser Gets JS Files and who exavctly runs JS in Browser
> - What is JS Engine
> - What is the roles played by JS Engine and EventLoop in JS RunTime Environment
> - What is NodeJS


### How does Browser Gets JS Files and runs them ?
All the Browser have common mechanism for getting JS Files to them from the ***Hosted Server*** (HS). This mechanism starts by getting html file from HS which may or may not contain script tags to JS files, if they do have them Browser requests those files (Either CSS or JS files) to HS and gets them.

Based on the JS code triggering point, the *JS Engine* takes the JOB of running that JS.

### What is JS Engine ?
JS Engine is a *Computer Program* that can run JavaScript.  Each Browser uses one of the JS Engines to run JS.
| Browser| Engine |
| -|:-|
| Chrome|V8|
|Firefox|SpiderMonkey|
|Edge & IE|Chakra|
|Safari|Nitro|
|Opera|Futhark|
Above are some Browser specific JS Engines List.

***V8 Engine***
It is being used by Chrome. It is an Open Source Library written in C++. It can run standalone and can be embedded into any C++ application. It implemets [ECMAScript](https://en.wikipedia.org/wiki/ECMAScript) as specified in ECMA-262.

Here comes the Question for you !!!
> As it is Open Source Library, can we run Complete JS by providing C++ env to V8 ?

Most answers would reflect **YES** since it runs JS.
***But***
it can not run Complete JS.
