---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2025-03-03T17:42:01.201Z
updated: 2025-03-07T16:16:18.009Z
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
<li><a href="https://facebook-clips.techidaily.com/new-in-2024-fix-facebook-videos-not-playing-on-androidiphonechrome/"><u>[New] In 2024, Fix Facebook Videos Not Playing on Android/iPhone/Chrome</u></a></li>
<li><a href="https://video-capture.techidaily.com/new-in-2024-ultimate-selection-of-ps1-games-now-on-your-computer/"><u>[New] In 2024, Ultimate Selection of PS1 Games, Now on Your Computer</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/updated-leading-edge-in-photo-editing-top-6-signature-removers-unveiled/"><u>[Updated] Leading Edge in Photo Editing Top 6 Signature Removers Unveiled</u></a></li>
<li><a href="https://win-web.techidaily.com/curating-a-successful-cryptocurrency-portfolio-with-expert-advice-from-yl-software/"><u>Curating a Successful Cryptocurrency Portfolio with Expert Advice From YL Software</u></a></li>
<li><a href="https://win-web.techidaily.com/effective-strategies-to-mitigate-risks-of-static-electricity-insights-from-yl-computing-and-software-solutions/"><u>Effective Strategies to Mitigate Risks of Static Electricity: Insights From YL Computing & Software Solutions</u></a></li>
<li><a href="https://win-web.techidaily.com/exploring-the-origins-the-dawn-of-chinas-unification-a-historical-insight-by-yl-computing-and-yl-software/"><u>Exploring the Origins: The Dawn of China's Unification - A Historical Insight by YL Computing & YL Software</u></a></li>
<li><a href="https://win-web.techidaily.com/fast-track-to-reverting-control-panel-configurations-tips-by-yl-software-experts/"><u>Fast Track to Reverting Control Panel Configurations: Tips by YL Software Experts</u></a></li>
<li><a href="https://win-web.techidaily.com/how-to-fix-non-responsive-device-components-with-tips-from-yl-software-experts/"><u>How to Fix Non-Responsive Device Components with Tips From YL Software Experts</u></a></li>
<li><a href="https://techidaily.com/how-to-transfer-whatsapp-from-apple-iphone-14-plus-to-other-iphone-11-devices-drfone-by-drfone-transfer-whatsapp-from-ios-transfer-whatsapp-from-ios/"><u>How To Transfer WhatsApp From Apple iPhone 14 Plus to other iPhone 11 devices? | Dr.fone</u></a></li>
<li><a href="https://review-topics.techidaily.com/how-to-unlock-poco-f5-pro-5g-without-password-by-drfone-android-unlock-android-unlock/"><u>How to Unlock Poco F5 Pro 5G Without Password?</u></a></li>
<li><a href="https://sim-unlock.techidaily.com/in-2024-the-best-android-unlock-software-for-sony-xperia-5-v-device-top-5-picks-to-remove-android-locks-by-drfone-android/"><u>In 2024, The Best Android Unlock Software For Sony Xperia 5 V Device Top 5 Picks to Remove Android Locks</u></a></li>
<li><a href="https://win-web.techidaily.com/potsdam-agreement/"><u>Potsdam Agreement</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/streamlined-approach-to-add-linktree-in-tiktok-about-section-for-2024/"><u>Streamlined Approach to Add Linktree in TikTok About Section for 2024</u></a></li>
<li><a href="https://win-web.techidaily.com/troubleshooting-and-resolving-sound-issues-in-windows-a-step-by-step-fix-for-a-nonfunctional-sound-card-digitalexpertise/"><u>Troubleshooting and Resolving Sound Issues in Windows: A Step-by-Step Fix for a Nonfunctional Sound Card – DigitalExpertise</u></a></li>
<li><a href="https://win-superb.techidaily.com/unraveling-the-mystery-why-might-a-samsung-ssd-remain-undetected-by-your-systems-bios/"><u>Unraveling the Mystery: Why Might a Samsung SSD Remain Undetected by Your System's BIOS?</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/visionaryvideoeditor-thorough-breakdown-and-opinions-for-2024/"><u>VisionaryVideoEditor Thorough Breakdown & Opinions for 2024</u></a></li>
<li><a href="https://win-webster.techidaily.com/yl-computings-ultimate-guide-how-to-efficiently-launch-and-access-microsoft-word-files/"><u>YL Computing's Ultimate Guide: How to Efficiently Launch and Access Microsoft Word Files</u></a></li>
<li><a href="https://win-web.techidaily.com/yl-software-tutorial-simple-steps-for-modifying-file-types-on-your-pc/"><u>YL Software Tutorial: Simple Steps for Modifying File Types on Your PC</u></a></li>
<li><a href="https://win-web.techidaily.com/yl-softwares-ultra-hd-themed-background-images-for-a-stunning-weekly-visual-refresh/"><u>YL Software's Ultra-HD Themed Background Images for a Stunning Weekly Visual Refresh</u></a></li>
</ul></div>

