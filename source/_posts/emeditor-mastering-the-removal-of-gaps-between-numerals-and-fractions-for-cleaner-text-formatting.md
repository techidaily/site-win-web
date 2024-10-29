---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2024-10-25T19:40:09.627Z
updated: 2024-10-28T23:39:31.610Z
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
<li><a href="https://instagram-video-recordings.techidaily.com/new-2024-approved-diving-into-the-essence-of-verified-instagramselfies/"><u>[New] 2024 Approved Diving Into the Essence of Verified Instagramselfies</u></a></li>
<li><a href="https://tiktok-videos.techidaily.com/new-bold-framing-integrating-large-headscapes-into-tiktok/"><u>[New] Bold Framing Integrating Large Headscapes Into TikTok</u></a></li>
<li><a href="https://screen-sharing-recording.techidaily.com/new-in-2024-direct-screen-capture-chrome-os-tool/"><u>[New] In 2024, Direct Screen Capture Chrome OS Tool</u></a></li>
<li><a href="https://fox-boxes.techidaily.com/updated-in-2024-from-basic-to-advanced-usage-maximize-your-experience-with-macs-preview/"><u>[Updated] In 2024, From Basic to Advanced Usage Maximize Your Experience with Mac's Preview</u></a></li>
<li><a href="https://screen-capture.techidaily.com/updated-ultimate-low-cost-gaming-setups-keyboard-picks-for-2024/"><u>[Updated] Ultimate Low-Cost Gaming Setups Keyboard Picks for 2024</u></a></li>
<li><a href="https://win-web.techidaily.com/nas-buffalo-linkstation/"><u>「他のNASデバイスに容易に移行! Buffalo LinkStationバックアップガイド」</u></a></li>
<li><a href="https://tech-haven.techidaily.com/chatgpt-revolutionizing-office-writing-the-new-norm-in-word/"><u>ChatGPT Revolutionizing Office Writing: The New Norm in Word</u></a></li>
<li><a href="https://win-howtos.techidaily.com/error-code-0x800f081f-on-your-mind-solving-the-dotnet-35-install-problems/"><u>Error Code 0X800F081F on Your Mind? Solving the DotNet 3.5 Install Problems!</u></a></li>
<li><a href="https://win-web.techidaily.com/essential-system-specifications-for-optimal-performance/"><u>Essential System Specifications for Optimal Performance</u></a></li>
<li><a href="https://win-web.techidaily.com/fix-fur-automatically-add-to-itunes-feature-behoben/"><u>Fix Für 'Automatically Add to iTunes' Feature - Behoben</u></a></li>
<li><a href="https://win-web.techidaily.com/guida-passo-passo-alla-risoluzione-della-mancata-localizzazione-del-testo-nel-backup-di-sistema/"><u>Guida Passo-Passo Alla Risoluzione Della Mancata Localizzazione Del Testo Nel Backup Di Sistema</u></a></li>
<li><a href="https://data-wizards.techidaily.com/reversing-the-impact-of-rare-video-formats/"><u>Reversing the Impact of Rare Video Formats</u></a></li>
<li><a href="https://extra-resources.techidaily.com/secrets-to-mastering-canva-10-insider-tips-for-editors/"><u>Secrets to Mastering Canva 10 Insider Tips for Editors</u></a></li>
<li><a href="https://win-web.techidaily.com/successfully-addressed-highest-priority-level-errors-in-windows-11-irqlnotlessorequal/"><u>Successfully Addressed Highest Priority Level Errors in Windows 11 (IRQL_NOT_LESS_OR_EQUAL)</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://wigfever.sjv.io/c/5597632/2005183/22899" target="_top" id="2005183">
  <img src="//a.impactradius-go.com/display-ad/22899-2005183" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://wigfever.sjv.io/i/5597632/2005183/22899" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

