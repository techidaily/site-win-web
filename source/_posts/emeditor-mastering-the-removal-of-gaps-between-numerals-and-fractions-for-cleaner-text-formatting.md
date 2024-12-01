---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2024-11-25T18:43:25.723Z
updated: 2024-11-30T17:25:08.964Z
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
<li><a href="https://digital-screen-recording.techidaily.com/updated-the-complete-breakdown-setting-up-game-capture-on-ps4-console-for-2024/"><u>[Updated] The Complete Breakdown Setting Up Game Capture on PS4 Console for 2024</u></a></li>
<li><a href="https://extra-approaches.techidaily.com/2024-approved-navigating-previewed-fb-activity-is-it-safe-or-not/"><u>2024 Approved Navigating Previewed FB Activity Is It Safe or Not?</u></a></li>
<li><a href="https://screen-activity-recording.techidaily.com/2024-approved-step-by-step-guide-exploring-every-nook-and-cranny-of-stardew-valley-particularly-ginger-island/"><u>2024 Approved Step-by-Step Guide Exploring Every Nook and Cranny of Stardew Valley, Particularly Ginger Island</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/delta-airlines-reveals-disturbing-confession-that-could-annoy-passengers-insights-from-zdnet/"><u>Delta Airlines Reveals Disturbing Confession That Could Annoy Passengers - Insights From ZDNet</u></a></li>
<li><a href="https://win-web.techidaily.com/how-to-transfer-your-entire-windows-system-to-an-external-hdd/"><u>How to Transfer Your Entire Windows System to an External HDD</u></a></li>
<li><a href="https://bypass-frp.techidaily.com/in-2024-addrom-bypass-an-android-tool-to-unlock-frp-lock-screen-for-your-tecno-phantom-v-flip-by-drfone-android/"><u>In 2024, AddROM Bypass An Android Tool to Unlock FRP Lock Screen For your Tecno Phantom V Flip</u></a></li>
<li><a href="https://android-pokemon-go.techidaily.com/in-2024-what-legendaries-are-in-pokemon-platinum-on-oppo-find-x6-pro-drfone-by-drfone-virtual-android/"><u>In 2024, What Legendaries Are In Pokemon Platinum On Oppo Find X6 Pro? | Dr.fone</u></a></li>
<li><a href="https://win-web.techidaily.com/les-options-superieures-a-wd-smartware-pour-les-systemes-dexploitation-windows-10-and-11-guide-comparatif/"><u>Les Options Supérieures À WD Smartware Pour Les Systèmes D'Exploitation Windows 10 & 11 : Guide Comparatif</u></a></li>
<li><a href="https://win-web.techidaily.com/professionelle-anweisungen-zur-sicherung-ihrer-yahoo-mail-mails-auf-lokale-festplatten-vier-effektive-strategien/"><u>Professionelle Anweisungen Zur Sicherung Ihrer Yahoo Mail-Mails Auf Lokale Festplatten – Vier Effektive Strategien</u></a></li>
<li><a href="https://win-web.techidaily.com/quick-guide-to-reviving-your-efi-partition-in-windows-11/"><u>Quick Guide to Reviving Your EFI Partition in Windows 11</u></a></li>
<li><a href="https://win-web.techidaily.com/reversing-an-accidentally-deleted-main-profile-solutions-for-windows-11-users/"><u>Reversing an Accidentally Deleted Main Profile: Solutions for Windows 11 Users</u></a></li>
<li><a href="https://win-web.techidaily.com/step-by-step-tutorial-for-shifting-video-content-onto-any-ipad-model-proairmini-from-computer/"><u>Step-by-Step Tutorial for Shifting Video Content Onto Any iPad Model (Pro/Air/Mini) From Computer</u></a></li>
<li><a href="https://extra-information.techidaily.com/unboxing-t5s-capability-as-a-sports-recorder/"><u>Unboxing T5's Capability as a Sports Recorder</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/YpnYKIrpgZQ?si=94zicAHp1CH-0oso" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

