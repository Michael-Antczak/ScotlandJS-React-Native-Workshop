# Chapter 1 - Introduction

1. What is React & React Native?

    > **[React Native](https://facebook.github.io/react-native/)** is a framework that allows you to build **native** mobile apps using **JavaScript**.  
      
      ------
    
    > **React Native** is not about avoiding any native development, it’s more about boosting productivity and sharing business logic and practices among very different platforms. [[1]](https://github.com/Michael-Antczak/ScotlandJS-React-Native-Workshop/blob/master/chapters/1-Introduction.md#resources) . 
      

2. Why need for React Native?

    - Learn Once, Write Anywhere - reuse ideas and skills across platforms
    - make mobile dev experience as quick as that of a web developer
    - maintain one codebase instead of two
    - cost of hiring a native developer
    - increase the pool of mobile developers
    
3. Who's using React Native?

   You can check [Showcase](https://facebook.github.io/react-native/showcase.html) page and [React Native Apps](https://github.com/ReactNativeNews/React-Native-Apps) GitHub pages.  

4. Some misconceptions about React Native

    > Is it for everybody and every case? 
    
    NO.

    Read about the Airbnb experience with React Native [[2]](https://github.com/Michael-Antczak/ScotlandJS-React-Native-Workshop/blob/master/chapters/1-Introduction.md#resources) and the reasons they are moving away. 
    
    **tl;dr**  
    #### Some of the things that worked for Airbnb:
    - Cross-platform
        > Most features that used React Native were able to achieve 95–100% shared code and 0.2% of files were platform-specific (*.android.js/*.ios.js).
        
    - Iteration speed
        > While developing in React Native, we were able to reliably use hot reloading to test our changes on Android and iOS in just a second or two. (...) At best, native compilation times are 15 seconds but can be as high as 20 minutes for full builds.
        
    - Performance
        > One of the largest concerns around React Native was its performance. However, in practice, this was rarely a problem. Most of our React Native screens feel as fluid as our native ones. Performance is often thought of in a single dimension. We frequently saw mobile engineers look at JS and think “slower than Java”. However, moving business logic and layout off of the main thread actually improves render performance in many cases.
    
    - Animations
        > Thanks to the [React Native Animated](https://facebook.github.io/react-native/docs/animated.html) library, we were able to achieve jank-free animations and even interaction-driven animations such as scrolling parallax.
        
    #### Some of the things that didn't worked for Airbnb:
    
    - Performance
        > However, the initialization and first-render time (outlined below) made React Native perform poorly for launch screens, deeplinks, and increased the TTI time while navigating between screens.
     
     - Immaturity
        > React Native is less mature than Android or iOS. It is newer, highly ambitious, and moving extremely quickly.
        
     - JavaScriptCore inconsistencies
        > ... it is executed on a [JavaScriptCore environment](https://facebook.github.io/react-native/docs/javascript-environment.html). The following are consequences we encountered as a result: 
        > - iOS ships with its own JavaScriptCore out of the box. This meant that iOS was mostly consistent and not problematic for us.
        > - Android doesn’t ship its own JavaScriptCore so React Native bundles its own. However, the one you get by default is ancient. As a result, we had to go out of our way to bundle a newer one.
        > - While debugging, React Native attaches to a Chrome Developer Tools instance. This is great because it is a powerful debugger. However, once the debugger is attached, all JavaScript runs within Chrome’s V8 engine. This is fine 99.9% of the time.
      
      - Initialization Time
        > Before React Native can render for the first time, you must initialize its runtime. Unfortunately, this takes several seconds for an app of our size, even on a high-end device. This made using React Native for launch screens nearly impossible.
    
    Also, have a look at the follow up by Charlie Cheever from Expo team [[3]](https://github.com/Michael-Antczak/ScotlandJS-React-Native-Workshop/blob/master/chapters/1-Introduction.md#resources).

    > Does it mean I don't need to know Java/Kotlin/Objective-C/Swift etc? 
    
    YES and NO.

5. What is Expo? 

    > **[Expo](https://expo.io/)** is a free and open source toolchain built around React Native to help you build native iOS and Android projects using JavaScript and React.


6. Where to seek help

    - [React Native docs](https://facebook.github.io/react-native/docs/getting-started.html)
    - [Expo docs](https://docs.expo.io/versions/latest/)
    - [Expo feature request on Canny](https://expo.canny.io/)

### Resources
1. [Thoughts about React Native after a few months working with it.](https://blog.usejournal.com/thoughts-about-react-native-after-a-few-months-working-with-it-4b3e255c3120)
2. [React Native at Airbnb.](https://medium.com/airbnb-engineering/react-native-at-airbnb-f95aa460be1c)
3. [Should we use React Native?](https://blog.expo.io/should-we-use-react-native-1465d8b607ac)
