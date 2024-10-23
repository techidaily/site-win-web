---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2024-10-21T00:35:15.696Z
updated: 2024-10-23T05:43:08.881Z
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
<li><a href="https://fox-blue.techidaily.com/updated-2024-approved-step-by-step-on-building-perfect-srt-files/"><u>[Updated] 2024 Approved Step-by-Step on Building Perfect SRT Files</u></a></li>
<li><a href="https://youtube-web.techidaily.com/ed-giggles-galore-7-entertaining-video-sets-for-chuckleheads-for-2024/"><u>[Updated] Giggles Galore 7 Entertaining Video Sets for Chuckleheads for 2024</u></a></li>
<li><a href="https://on-screen-recording.techidaily.com/updated-in-2024-perfect-your-xbox-footage-4-recording-strategies-revealed/"><u>[Updated] In 2024, Perfect Your Xbox Footage 4 Recording Strategies Revealed</u></a></li>
<li><a href="https://tiktok-video-recordings.techidaily.com/updated-unlock-your-music-best-free-on-web-tiktok-to-mp3-convertors-for-2024/"><u>[Updated] Unlock Your Music Best Free, On-Web TikTok to MP3 Convertors for 2024</u></a></li>
<li><a href="https://extra-information.techidaily.com/2024-approved-a-guide-to-pinpointing-a-list-video-creators/"><u>2024 Approved A Guide to Pinpointing A-List Video Creators</u></a></li>
<li><a href="https://win-web.techidaily.com/effortless-iphone-data-removal-tool-complete-icloud-cleanup-at-no-cost/"><u>Effortless iPhone Data Removal Tool - Complete iCloud Cleanup at No Cost</u></a></li>
<li><a href="https://win-web.techidaily.com/festplatten-datenrettung-erfolgreich-durchfuhren-entdecken-sie-drei-effektive-strategien/"><u>Festplatten-Datenrettung Erfolgreich Durchführen: Entdecken Sie Drei Effektive Strategien</u></a></li>
<li><a href="https://win-web.techidaily.com/guide-complet-comment-retrouver-les-emails-dans-une-boite-aux-lettres-videe-efficacement/"><u>Guide Complet : Comment Retrouver Les Emails Dans Une Boîte Aux Lettres Vidée Efficacement ?</u></a></li>
<li><a href="https://video-capture.techidaily.com/in-2024-economical-pc-streaming-with-simple-obs-configurations/"><u>In 2024, Economical PC Streaming with Simple OBS Configurations</u></a></li>
<li><a href="https://ios-unlock.techidaily.com/in-2024-forgot-locked-apple-iphone-12-password-learn-the-best-methods-to-unlock-by-drfone-ios/"><u>In 2024, Forgot Locked Apple iPhone 12 Password? Learn the Best Methods To Unlock</u></a></li>
<li><a href="https://win-web.techidaily.com/resolving-system-writer-missing-from-backup-issue-3-effective-solutions/"><u>Resolving 'System Writer Missing From Backup' Issue: 3 Effective Solutions</u></a></li>
<li><a href="https://win-web.techidaily.com/schutz-ihrer-anwendungen-auf-ios-geraten-mit-icloud-sichern-tipps-und-tricks-fur-iphone-ipad-ipod-and-mac/"><u>Schutz Ihrer Anwendungen Auf iOS-Geräten Mit iCloud Sichern - Tipps Und Tricks Für iPhone, iPad, iPod & Mac</u></a></li>
<li><a href="https://activate-lock.techidaily.com/ultimate-guide-from-apple-iphone-8-icloud-activation-lock-bypass-by-drfone-ios/"><u>Ultimate Guide from Apple iPhone 8 iCloud Activation Lock Bypass</u></a></li>
<li><a href="https://win-web.techidaily.com/windows-7-4/"><u>Windows 7 起動修復に失敗する場合の解決手段 - 4 つの方法</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2123727/7443" target="_top" id="2123727">
  <img src="//a.impactradius-go.com/display-ad/7443-2123727" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2123727/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

