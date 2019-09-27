Androidx Auto Scroll ViewPager
==============================
* ViewPager which can auto scrolling, cycling, decelerating.  
* ViewPager which can be slided normal in parent ViewPager.
* ViewPager which is compatible with AndroidX library.

# Thanks
Many thanks to [Trinea](https://github.com/Trinea) because this library is the newest, kotlin version of his [library](https://github.com/Trinea/android-auto-scroll-view-pager). We support AndroidX library, so if you have problem when migrating to AndroidX, this version should work like a charm. 

## Usage
- include this library
- use below code

``` xml
<pl.pzienowicz.AutoScrollViewPager
	android:id="@+id/view_pager"
	android:layout_width="match_parent"
	android:layout_height="wrap_content" />
```
instead of
``` xml
<android.support.v4.view.ViewPager
	android:id="@+id/view_pager"
	android:layout_width="match_parent"
	android:layout_height="wrap_content" />
```

## Functions
- `startAutoScroll()` start auto scroll, delay time is `getInterval()`.
- `startAutoScroll(int)` start auto scroll delayed.
- `stopAutoScroll()` stop auto scroll.

## Setting
- `setInterval(long)` set auto scroll time in milliseconds, default is `DEFAULT_INTERVAL`.  
- `setDirection(int)` set auto scroll direction, default is `RIGHT`.  
- `setCycle(boolean)` set whether automatic cycle when auto scroll reaching the last or first item, default is true. 
- `setScrollDurationFactor(double)` set the factor by which the duration of sliding animation will change.  
- `setSlideBorderMode(int)` set how to process when sliding at the last or first item, default is `SLIDE_BORDER_MODE_NONE`.
- `setStopScrollWhenTouch(boolean)` set whether stop auto scroll when touching, default is true.  
- `setBorderAnimation(boolean)` set whether animating when auto scroll at the last or first item, default is true.  
- You cannot combine with [ViewPagerIndicator](https://github.com/JakeWharton/Android-ViewPagerIndicator) if `setCycle(true)`. 