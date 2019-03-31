# Performance Aspects!
> - Verify performance aspects of Node React Application
> - Audit the application performance using chrome Audit Mechanism
> - Reason for less performance
> - Ways to increase performance


All we applications are serving most things and are been maintaining to do lot more, but only common Problem comes there is **Performance** !.

### Why does it Matters ?
Performance is about retaining ***Users***
Performance is about improving ***Conversions***
Performance is about the ***User experience***
Performance is about ***People***

Detailed description relies in [Web Fundamentals](https://developers.google.com/web/fundamentals/performance/why-performance-matters/).

## Verify performance aspects of Node React Application
Verified AUTO project using Google Speed Insights which showed
- Stats of performance
- Reasons for less performance
- Improvements to be taken etc.

Following can Provide the detailed aspects of Auto
https://developers.google.com/speed/pagespeed/insights/?url=https%3A%2F%2Fwww.auto.com%2Fcars-for-sale%2Fless-than-10000-dollars&tab=desktop

## Audit the application performance using chrome Audit Mechanism
In Chrome Dev Tools,
> Move to Audits tab powered by Google Light House
>  Select Run Audits for selected URL to be verified

Following the above steps will give us LightHouse Report which is being used by many **webpages** for Performance aspects and are Integrated to their applications and generate regular reports to audit Performance.

This provides you similar stats to [GooglePageInsights](https://developers.google.com/speed/pagespeed/insights/).

Using Command Palette ( Ctrl + Shift + P ) in  Chrome Dev Tools, commands to show Performance, Coverage, Audits etc.. are allowed.
 For Detailed description visit [LightHouse](https://developers.google.com/web/tools/lighthouse/).

## Reasons for less performance
On Auditing both Insights and LightHouse for AUTO
Major reasons from them are,
- Larger image sizes impacting
- Unused Large js files (Code Splitting)
- Images Lazy loading
- Tree Shaking

***Code Splitting***
  It is most compelling feature that allows us to split our code into variable bundles which can then be loaded on demand or in parallel.
   It can be used to achieve smaller bundles and control resource load prioritization which, if used correctly can have a major impact on load time.

***Tree Shaking***
Tree Shaking is the term used in JS context for dead-code elimination.This plays major role in reducing bundle sizes which there by improve Performance.

Webpack enables this in Production Mode.

## Ways to increase performance
Code Coverage showed us unused code in js files which can be removed or major modules like Moment.js can go with other modules like date-fns (which is of 6 times lesser to Moment in bundle size)
- Image sizes are to be reduced
- Formatting images to webp helps
- Code Splitting helps to reduce js file sizes
- Tree Shaking also helps to reduce js file
