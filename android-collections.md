# The Android Collections
A Collection of Android practices. This collection is meant to make it easier for me to keep the vast amounts information about the android eco system in check. There will be categories that will help to break up the search into smaller pieces.

### The Build
  * Bitrise a paid service that is well worth it.
  * configure your build properly [here](https://developer.android.com/studio/build/application-id)

### Best practices
  * [futurice](https://github.com/futurice/android-best-practices) has a good base collection started.
  * Build types
    * make build types and flavors easy to recognize with [easylauncher](https://github.com/akaita/easylauncher-gradle-plugin)
  * Build Flavors
    * [Build Variants](https://developer.android.com/studio/build/build-variants#sourceset-build)
    * [Manifest Merge](https://developer.android.com/studio/build/manifest-merge)
  * Fonts
    * [Google fonts](https://www.youtube.com/watch?reload=9&v=TfB-TsLFJdM)

  * API 28 Pie forces https: what is the best order of action for this?
    1. API split on the build ?
    2. Self signed Cert for the https ?


### Release Check List
  * Were there database changes? If so was the application updated with existing data in said database?
    - adb install -r <your.apk> will imitate this. But the best test is to use the Playstore beta channel.
  * [Standard checklist](https://developer.android.com/distribute/best-practices/launch/launch-checklist#checklist)

### Views

### Android Studio Environment
 * [Tips and Tricks](https://medium.com/@mmbialas/50-android-studio-tips-tricks-resources-you-should-be-familiar-with-as-an-android-developer-af86e7cf56d2)

### Design
  [Google Design Medium](https://medium.com/google-design)  
  [Motion](https://medium.com/google-design/motion-design-doesnt-have-to-be-hard-33089196e6c2)  
  [Typeography](https://medium.com/google-design/the-android-developers-guide-to-better-typography-97e11bb0e261)  

  * Android vs. iOS
    * [compare design](https://medium.com/@chunchuanlin/android-vs-ios-compare-20-ui-components-patterns-part-1-ad33c2418b45)
    * [the never ending lazy chevron debate](http://mobiledesignguy.com/2018/07/20/chevrons-android-google-material-uxdesign/)
 * Principles
    * [Design Principles](https://material.io/design/motion/understanding-motion.html#principles)

    * [Disney Design principles](https://en.wikipedia.org/wiki/12_basic_principles_of_animation)

    * [Ten rules of product design](https://uxdesign.cc/ten-rules-of-good-design-e3dcabc61bc)


#### Screen sizes
  * the explanation of the DIP dp/sp etc [here](https://developer.android.com/training/multiscreen/screendensities).
  * From a designers point of view [Prototypr](https://blog.prototypr.io/designing-for-multiple-screen-densities-on-android-5fba8afe7ead)
  * [dpi.lv](http://dpi.lv/#1920%C3%971080@5%E2%80%B3)
  * [fono](https://github.com/shakee93/fonoapi) - [fonoapi](https://fonoapi.freshpixl.com/)
    curl https://fonoapi.freshpixl.com/v1/getdevice -XPOST -H 'Accept: application/json' -d 'token=YOUR_TOKEN_HERE&limit=5&device=A8'
  * [ My notes on the DPI](density-independent-pixels.md)


### Gotchas
  * Do not put ViewPagers in a scrollview nested or other wise, the view pager collides with the scroll behavior and will not scroll fully in the window. The ViewPager will get to the top of the Coordinator view and stop.


### TODO Techs
  * Wire from Square [here](https://github.com/square/wire)
