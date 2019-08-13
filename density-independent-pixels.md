# Density Independent Pixels

[*reference*](https://www.youtube.com/watch?v=zhszwkcay2A)

Devices have different pixel densities measured in dots-per-inch (dpi). _How many dots will fit in an inch._

| Logical densities | Name | Scale |
| --- | :---: | ---: |
| 160 | mdpi | 1X  (baseline) |
| 240 | dhpi | 1.5x |
| 320 | xhdpi | 2x |
| 480 | xxhdpi | 3x |
| 640 | xxxhdpi | 4x |

Density-independent pixels (dp or dip)  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; are virtual pixel units or logical pixel densities, **equivalent to one physical pixel on a 160 dpi (mdpi) screen** and scaled proportionally on higher or  lower density screens.

**1 dpi** on an on a **mdpi** screen will be **1 pixel**.   
**1 dpi** on on and **xhdpi** screen will be **4 pixels**, *two down and two across*.

The human finger tip is approximately 50 dp. In most UX specs the **minimum touch target that you should provide is 48x48 dp**.

Formulas to calculate densities :
###### mdpi
1 px  / 1 dp = 160 dpi / 160 dpi  

###### hdpi
1.5 px / 1 dp = 240 dpi / 160 dpi

###### xhdpi
2 px / 1 dp = 320 dpi / 160 dpi

###### xxmdpi
3 px / 1 dp = 480 dpi / 160 dpi

_So, the Nexus 7 has a screen that is 1920x1200 px and it is an xhdpi. This means ..._  
1920x1200 px on hdpi = 1280x800 dpi  
1920x1200 px on xhdpi = 960x600 dpi  
1920x1200 px on xxhdpi = 640x400 dpi  
1920x120 px on xxxhdpi = 480x300 dpi  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[Nice tools](http://angrytools.com/android/pixelcalc/)

Provide graphic assets for each density to avoid auto scaling. If an asset does not reach the density cut off limit such as 320 for xhdpi the next lower asset will be used. This can cause unintended visual affects. Images will not take up as much real estate on the screen that is displayed. This could in turn cause other elements to shift accordingly to their relation to said asset.

  * Design and spec layouts in **dp** units
  * Provide graphic assets for each density to avoid auto scaling.

  If you want an asset to be 32px on a mdpi screen. You will need to generate a matching asset that is 96px for a xxhdpi screen to have them the same size on the different screens.  


### Vector graphics
[Google talks](https://www.youtube.com/watch?v=Ls3KzLRmrXg)
