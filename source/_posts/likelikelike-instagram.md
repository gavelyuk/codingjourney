---
title: likelikelike-instagram
date: 2018-07-31 13:14:06
tags:
---
My thousand Instagram subscribers. Here I would like to share my story about how I got  1000 subscribers. So let's start hacking Instagram.
<!-- more --> <!-- more -->
So as a developer I'm install on my **Firefox** and onlyone extension called: **grease Monkey**. Idea was do automatic following and likes all of the content of my followers. This is little bit mmmm... a irresponsible  because huge amount of people have just crazy content so if you likes in automatic mode you can miss pretty damn good people or like some people and content what you will never like. And after reading this post I will just remind you when you use any scripts you can be banned and nobody will help you also your account can be steeled.
So basically you need dedicated computer,  probably your old notebook with installed  **Firefox + grease monkey extension four Firefox**. Basically you need just copy paste or download the script, but I would like you learn and not blind copy paste, I would like to teach you the basic principles all the web.
So any element on your page have a classes for style (CSS) and IDs for a JavaScript so basically if you know any language related to Web you can do it.
Lets start writing simulator of yourself. More or less we will have a small bot/script  what likes user posts.
So Instagram loading your browser with feed oWe need to find with JavaScript grey hearts they have CSS classes `"glyphsSpriteHeart__outline__24__grey_9"` so we took all elements and put in array after these we take first element of the array as you remember it will be element number zero and simulating event with click. For this we use document `create event` and after this we need `event` and `dispatch` it, later increase our counter and scroll manually page and do this again and again.
Instagram have limitation on speed how you clicking and quantity of click (likes).  so you're not allowed  click faster then 3 milliseconds and you do not allowed to do more than 1600 likes at least I've got problems then do around this number.
Likes with speed of 3 milliseconds it will actually looks like somebody attack the server and of course when you do more than thousand likes in one hour it will looks very suspicious. So basically if you have limits on the cache you can do this trick to improve your Instagram stats. Second very important thing is following for other users.
The script will work in same way you just need to choose **"follow button"** and do same checks do not click when you're already following that user.
Basically if you will work hard you can get **around 300 new subscribers per day** and this will be from the total value of your users 20% of all you following.
In other words if you will be follow 5000 person 1000 person for sure will be subscribe  to your channel, Of course from these thousand persons will be around 300 persons what have their own business and they do most likely the same what you doing. Natural subscribers it's more good thing but you will gain them very very slow. You can choose some predefined path take music, almost nude girls, memes, but in this case you will lose your personality and for some people you personal style and work very important. People would like to see your face and know this person stay behind this advertisement and this person don't scare to show his face and the name because he or she do not trick people, they would like to know about this person really like to do proper job. I would like to thanks  to all my subscribers and hopefully you will read this text and  and it will be improve your situation on Instagram platform and/or understanding how the web works.
Please bookmark my blog page, here will be more interesting content, you will able to learn more about marketing, development, and other interesting stuff. Code of simple script as always in the end.

you can  donate with your CPU power and mine for me some Monero coins, by the way, you can register on the site and go to the Brotherhood of Eden, download the web app and install on your website,  you can change credentials and use this handy beautiful cross platform, well tested donation button.

See you soon,   best regards.

```JavaScript
// ==UserScript==
// @name     Likelikelike
// @version  1
// @grant    none
// ==/UserScript==
var likes = 0;
var scrooltobottom = 200;
window.addEventListener('DOMContentLoaded', function() {
  console.log('window - DOMContentLoaded - bubble'); // 3rd
function simulateCliks(el, evntType){
  if (el.fireEvent) {
    el.fireEvent('on' + evntType);
  } else {
    var evObj = document.createEvent('Events');
    evObj.initEvent(evntType, true, false);
    el.dispatchEvent(evObj);
  }
  likes++;
}
//  <span class="glyphsSpriteHeart__filled__24__red_5 Szr5J">Unlike</span>
//  <span class="glyphsSpriteHeart__outline__24__grey_9 Szr5J">Like</span>
var greyHearts = [];   //	Array of unliked things
var likeButton = [];   //	Array of buttons
var scrooltobottom =0;
var fixedScrool = 600; //	scrool for 600 px
var timerInt = 6000; //	6 sec
  setInterval(function(){
    greyHearts = document.getElementsByClassName("glyphsSpriteHeart__outline__24__grey_9");
    simulateCliks(greyHearts[0].parentElement, 'click', likes);
    window.scrollTo(0,scrooltobottom);
    scrooltobottom=scrooltobottom+fixedScrool;
    console.log(likes+"-- likes for this session");
  }, timerInt);
});
```
