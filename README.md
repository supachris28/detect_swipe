jquery.detectSwipe
==================

Gives easy access to left/right/up/down swipe events for iOS and other touch devices.  Also includes swipe from edge functionality.

Based on Andreas Waltl's [jQuery TouchWipe](http://www.netcu.de/jquery-touchwipe-iphone-ipad-library).

How to use
----------

    $(".selector").on('swipeleft',  function(){ /*...*/ })
                  .on('swiperight', function(){ /*...*/ })
                  .on('swipeup',    function(){ /*...*/ })
                  .on('swipedown',  function(){ /*...*/ });

Edge swipes:

    $(".selector").on('swipefromleft',   function(){ /*...*/ })
                  .on('swipefromright',  function(){ /*...*/ })
                  .on('swipefrombottom', function(){ /*...*/ })
                  .on('swipefromtop',    function(){ /*...*/ });

This won't have any effect on non-touch devices. You can rely on:

    $.detectSwipe.enabled // true on touch devices, false otherwise

Global setting:

    $.detectSwipe.threshold // The number of pixels your finger must move to trigger a swipe event.  Defaults is 20.
    $.detectSwipe.preventDefault // Should touchmove events be prevented?  Defaults to true.
    $.detectSwipe.edgethreshold // The number of pixels at the edges the the start of the swipe that should be interpreted as an "edge" swipe.  Defaults to 15% of the page width on load.
