---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2024-10-08T17:07:38.517Z
updated: 2024-10-10T18:20:21.676Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/845fcd5e3eadfdeed515b58ea51b6008ffc3adda0043bb6ffedd07e36277b4e8.jpg
---

## EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting

Viewing 4 posts - 1 through 4 (of 4 total)

* Author  
Posts
* November 7, 2009 at 4:18 pm [#7797](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/6bcb99132a36c4c1b97328e2a7058784?s=80&d=identicon&r=g)WmMitchell](https://www.emeditor.com/forums/users/wmmitchell/ "View WmMitchell's profile")  
Participant  
I’m trying EmEditor out. Jury is still out on whether or not this one is a keeper. If I can just figure out how to get the S&R functions down, that will determine on whether or not this is the app to keep.  
 The trouble is that I’m dealing with trying to figure out the regexp to use with EmEditor (which I’m woefully inexperienced in to begin with) and trying to figure out the EmEditor macro language at the same time! Not easy .  
 I need to know how to remove the space between a number-space-fraction text string. If I have something like  
 2 ½  
 I need to change that to  
 2½  
 I’ve tried this type of thing:  
 document.selection.Replace(“\[0-9\]+ ¼”,”\[0-9\]+¼”,eeFindNext | eeReplaceAll | eeFindReplaceRegExp);  
 The above seems great to \_find\_ the items but used to try to find entries such as this:  
 2½  
 I get this as a result:  
 \[0-9\]+½  
 How can we fix this from the macro:  
 document.selection.Replace(“\[0-9\]+ ¼”,”\[0-9\]+¼”,eeFindNext | eeReplaceAll | eeFindReplaceRegExp);  
 so that we get the desired result, pls?  
 From there, I’m sure that will help me learn how to work with the other parts of the script that deal with the same type of thing.  
 Thanks. :)  
November 7, 2009 at 8:39 pm [#7798](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/7df0e2050847a9b05989f897cae9bf03?s=80&d=identicon&r=g)MariaK](https://www.emeditor.com/forums/users/MariaK/ "View MariaK's profile")  
Participant  
You can use a group and a back reference.  
 Find:  
(\[0-9\]+) ½  
 Replace with:  
1½  
 Extended version:  
 Find:  
(\[0-9\]+) (\[¼,½,¾\])  
 Replace with:  
12  
November 8, 2009 at 2:48 pm [#7800](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/6bcb99132a36c4c1b97328e2a7058784?s=80&d=identicon&r=g)WmMitchell](https://www.emeditor.com/forums/users/wmmitchell/ "View WmMitchell's profile")  
Participant  
> Extended version:  
>  
> Find:  
> (\[0-9\]+) (\[¼,½,¾\])  
> Replace with:  
> 12  
That is amazing! I really thought that was going to work. It’s very confusing to be dealing with a whole bunch of software applications, but I seem to remember using something similar a long time ago in Word and it works in Word. But, unfortunately, it didn’t work here.  
 I really liked the extended version since it would take care of all number-fraction combinations, but the 1 and 2 didn’t work as expected in EmEditor.  
 When I ran the macro, which looks like this:  
 document.selection.Replace(“(\[0-9\]+) (\[¼,½,¾\])”,”12″,eeFindNext | eeReplaceAll | eeFindReplaceRegExp); /\* Remove space between number & fraction.\*/  
 I get those funny little boxes come up in the editor:  
 \[\] \[\]  
 rather than, say, 1½.  
 We’re close (“we”??!! I mean, obviously, you), but this isn’t quite right. Can you suggest how to fix? The 1 and 2 should put the number and fraction back that was there before, instead it’s replacing it with little boxes. (?)  
 Thanks.  
November 9, 2009 at 12:20 pm [#7808](https://tools.techidaily.com/emeditor/products/)  
[![](https://secure.gravatar.com/avatar/7df0e2050847a9b05989f897cae9bf03?s=80&d=identicon&r=g)MariaK](https://www.emeditor.com/forums/users/MariaK/ "View MariaK's profile")  
Participant  
It’s very simple; within a macro you must mask the backslash ”” with a prefix backslash ””. Here’s an example:  
document.selection.Replace(“(\[0-9\]+) (\[¼,½,¾\])”,”12″,eeFindNext | eeReplaceAll | eeFindReplaceRegExp);
* Author  
Posts

Viewing 4 posts - 1 through 4 (of 4 total)

* You must be logged in to reply to this topic.

<ins class="adsbygoogle"
     style="display:block"
     data-ad-format="autorelaxed"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="1223367746"></ins>

<ins class="adsbygoogle"
     style="display:block"
     data-ad-client="ca-pub-7571918770474297"
     data-ad-slot="8358498916"
     data-ad-format="auto"
     data-full-width-responsive="true"></ins>

<span class="atpl-alsoreadstyle">Also read:</span>
<div><ul>
<li><a href="https://facebook-video-content.techidaily.com/new-2024-approved-thriving-financially-with-successful-facebook-video-advertising-tactics/"><u>[New] 2024 Approved Thriving Financially with Successful Facebook Video Advertising Tactics</u></a></li>
<li><a href="https://extra-skills.techidaily.com/new-step-by-step-journey-mastering-the-art-of-gs-with-kinemaster/"><u>[New] Step-by-Step Journey Mastering the Art of GS with KineMaster</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/1-movavi-video-suite-purchase-guide-secure-discounted-deals-for-safe-downloads/"><u>1. Movavi Video Suite Purchase Guide - Secure Discounted Deals for Safe Downloads</u></a></li>
<li><a href="https://win-web.techidaily.com/2022s-top-seating-innovation-an-exclusive-review-of-andaseat-kaiser-3-on-zdnet/"><u>2022'S Top Seating Innovation: An Exclusive Review of AndaSeat Kaiser 3 on ZDNET</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/2024-approved-capture-the-season-wardrobe-top-5-winter-yt-scenes/"><u>2024 Approved Capture the Season' Wardrobe Top 5 Winter YT Scenes</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/agrarian-adventures-unplugged-stardews-kin-titles/"><u>Agrarian Adventures Unplugged Stardew's Kin Titles</u></a></li>
<li><a href="https://common-error.techidaily.com/guide-restoring-displayed-wi-fi-settings-on-windows-11/"><u>Guide: Restoring Displayed Wi-Fi Settings on Windows 11</u></a></li>
<li><a href="https://android-location-track.techidaily.com/how-to-track-a-lost-xiaomi-13t-for-free-drfone-by-drfone-virtual-android/"><u>How to Track a Lost Xiaomi 13T for Free? | Dr.fone</u></a></li>
<li><a href="https://some-approaches.techidaily.com/1726027235003-mp4windows-10/"><u>MP4ファイルを簡単に切り取るWindows 10のガイドブック</u></a></li>
<li><a href="https://win-web.techidaily.com/singapore-adopts-microsoft-copilot-next-gen-tech-in-legal-services-zdnet-insights/"><u>Singapore Adopts Microsoft Copilot: Next-Gen Tech in Legal Services | ZDNet Insights</u></a></li>
<li><a href="https://win-web.techidaily.com/steven-ballmer-previously-at-the-helm-of-microsoft-discusses-his-courageous-traits-or-lack-thereof-the-verge/"><u>Steven Ballmer, Previously at the Helm of Microsoft, Discusses His Courageous Traits or Lack Thereof | The Verge</u></a></li>
<li><a href="https://win-web.techidaily.com/tech-review-how-microsofts-new-lineup-of-easy-to-repair-laptops-outshines-rivals-leaving-apple-to-catch-up-zdnet/"><u>Tech Review: How Microsoft's New Lineup of Easy-to-Repair Laptops Outshines Rivals, Leaving Apple to Catch Up | ZDNET</u></a></li>
<li><a href="https://win-web.techidaily.com/transform-your-macbook-into-a-touchscreen-masterpiece-with-this-compact-portable-display-discover-more-on-zdnet/"><u>Transform Your MacBook Into a Touchscreen Masterpiece with This Compact Portable Display - Discover More on ZDNet!</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://unicoeye.pxf.io/c/5597632/2134492/18498" target="_top" id="2134492">
  <img src="//a.impactradius-go.com/display-ad/18498-2134492" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://unicoeye.pxf.io/i/5597632/2134492/18498" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

