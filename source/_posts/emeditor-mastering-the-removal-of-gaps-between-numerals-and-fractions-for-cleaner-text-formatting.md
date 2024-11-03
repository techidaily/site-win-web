---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2024-10-28T19:02:26.394Z
updated: 2024-11-03T21:16:30.208Z
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
<li><a href="https://some-techniques.techidaily.com/new-explore-new-horizons-in-video-editing-software/"><u>[New] Explore New Horizons in Video Editing Software</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/new-hidden-sound-scribes-unveiling-ios-and-android-stealth-recorders/"><u>[New] Hidden Sound Scribes Unveiling iOS & Android Stealth Recorders</u></a></li>
<li><a href="https://instagram-videos.techidaily.com/new-in-2024-accelerating-your-watch-experience-on-instagram-videos/"><u>[New] In 2024, Accelerating Your Watch Experience on Instagram Videos</u></a></li>
<li><a href="https://facebook-video-recording.techidaily.com/updated-2024-approved-the-complete-pathway-to-success-with-your-first-facebook-live/"><u>[Updated] 2024 Approved The Complete Pathway to Success with Your First Facebook Live</u></a></li>
<li><a href="https://win-web.techidaily.com/1-seamless-transfer-of-hidden-iphone-photos-to-pc-using-fonebackup/"><u>1. Seamless Transfer of Hidden iPhone Photos to PC Using FoneBackup</u></a></li>
<li><a href="https://win-web.techidaily.com/cddvd/"><u>映像轉移手段介紹：將CD/DVD的容量轉存至最新硬碟之上</u></a></li>
<li><a href="https://win-web.techidaily.com/error-almacenamiento-inadecuado-causando-falla-de-backup-en-windows-server/"><u>Error Almacenamiento Inadecuado Causando Falla De Backup en Windows Server</u></a></li>
<li><a href="https://win-web.techidaily.com/guia-eficiente-para-activar-la-sincronizacion-automatica-de-archivos-en-windows-8-7-y-11/"><u>Guía Eficiente Para Activar La Sincronización Automatica De Archivos en Windows 8, 7 Y 11</u></a></li>
<li><a href="https://common-error.techidaily.com/navigate-and-optimize-windows-11s-file-explorer-like-a-pro/"><u>Navigate and Optimize Windows 11'S File Explorer Like a Pro</u></a></li>
<li><a href="https://win-web.techidaily.com/step-by-step-guide-retrieving-accidentally-erased-data-from-your-sd-card/"><u>Step-by-Step Guide: Retrieving Accidentally Erased Data From Your SD Card</u></a></li>
<li><a href="https://games-able.techidaily.com/the-silent-switch-disable-controller-jolts/"><u>The Silent Switch: Disable Controller Jolts</u></a></li>
<li><a href="https://tech-recovery.techidaily.com/top-rated-magsafe-wallet-picks-comprehensive-reviews-by-tech-experts-zdnet/"><u>Top-Rated MagSafe Wallet Picks - Comprehensive Reviews by Tech Experts | ZDNet</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/unintentional-warp-wonders-and-cyber-salutes-insights-on-vr-encounters-a-dive-into-digital-handshakes-techwise/"><u>Unintentional Warp Wonders & Cyber Salutes: Insights on VR Encounters - A Dive Into Digital Handshakes | TechWise</u></a></li>
<li><a href="https://win-web.techidaily.com/wie-speichert-man-erfolgreich-ihr-itunes-backup-sicher/"><u>Wie Speichert Man Erfolgreich Ihr iTunes-Backup Sicher?</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1886048/19272" target="_top" id="1886048">
  <img src="//a.impactradius-go.com/display-ad/19272-1886048" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1886048/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

