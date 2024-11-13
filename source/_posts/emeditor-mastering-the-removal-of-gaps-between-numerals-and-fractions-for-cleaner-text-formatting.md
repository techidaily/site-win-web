---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2024-11-05T18:00:25.010Z
updated: 2024-11-12T23:20:09.219Z
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
<li><a href="https://visual-screen-recording.techidaily.com/new-lol-gaming-on-air-top-3-recording-methods/"><u>[New] LOL Gaming On Air Top 3 Recording Methods</u></a></li>
<li><a href="https://some-approaches.techidaily.com/2024-approved-the-illustrator-way-adding-realistic-blur-to-your-pics/"><u>2024 Approved The Illustrator Way Adding Realistic Blur to Your Pics</u></a></li>
<li><a href="https://blog-min.techidaily.com/5-easy-ways-to-copy-contacts-from-vivo-s17-pro-to-iphone-14-and-15-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>5 Easy Ways to Copy Contacts from Vivo S17 Pro to iPhone 14 and 15 | Dr.fone</u></a></li>
<li><a href="https://fox-links.techidaily.com/a-deep-dive-into-top-10-streaming-platforms-compared/"><u>A Deep Dive Into Top 10 Streaming Platforms Compared</u></a></li>
<li><a href="https://win-web.techidaily.com/abrufen-ihrer-letzten-gespeicherten-dateien-mit-myrecover-schnelle-losung-finden/"><u>Abrufen Ihrer Letzten Gespeicherten Dateien Mit MyRecover - Schnelle Lösung Finden!</u></a></li>
<li><a href="https://win-web.techidaily.com/exploring-the-essential-capabilities-of-aomei-backupper-software/"><u>Exploring the Essential Capabilities of AOMEI Backupper Software</u></a></li>
<li><a href="https://win-web.techidaily.com/five-effective-methods-to-retrieve-deleted-documents-post-windows-11-upgrade/"><u>Five Effective Methods to Retrieve Deleted Documents Post-Windows 11 Upgrade</u></a></li>
<li><a href="https://win-web.techidaily.com/five-effective-solutions-for-fixing-windows-11-startup-problems/"><u>Five Effective Solutions for Fixing Windows 11 Startup Problems</u></a></li>
<li><a href="https://ios-unlock.techidaily.com/how-to-bypass-the-required-apple-store-verification-for-iphone-12-pro-by-drfone-ios/"><u>How To Bypass the Required Apple Store Verification For iPhone 12 Pro</u></a></li>
<li><a href="https://win-web.techidaily.com/how-to-fully-recover-data-after-formatting-your-wd-my-book/"><u>How To Fully Recover Data After Formatting Your WD My Book</u></a></li>
<li><a href="https://screen-video-capture.techidaily.com/in-2024-essential-steps-for-recording-on-facebook-live/"><u>In 2024, Essential Steps for Recording on Facebook Live</u></a></li>
<li><a href="https://apple-account.techidaily.com/in-2024-protecting-your-privacy-how-to-remove-apple-id-from-iphone-11-pro-max-by-drfone-ios/"><u>In 2024, Protecting Your Privacy How To Remove Apple ID From iPhone 11 Pro Max</u></a></li>
<li><a href="https://win-web.techidaily.com/restaurer-les-videos-mp4-perdues-sur-votre-carte-sd/"><u>Restaurer Les Vidéos MP4 Perdues Sur Votre Carte SD</u></a></li>
<li><a href="https://win-web.techidaily.com/sauvegarde-de-windows-server-2er3-facons-methodes-efficaces-et-conseils-dexperts/"><u>Sauvegarde De Windows Server 2Er3 Façons : Méthodes Efficaces Et Conseils D'experts</u></a></li>
<li><a href="https://technical-tips.techidaily.com/windows-11-microsoft-abandons-support-for-android-applications/"><u>Windows 11: Microsoft Abandons Support for Android Applications</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/1868575/19272" target="_top" id="1868575">
  <img src="//a.impactradius-go.com/display-ad/19272-1868575" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/1868575/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

