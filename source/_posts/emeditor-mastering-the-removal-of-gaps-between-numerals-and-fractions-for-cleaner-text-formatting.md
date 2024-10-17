---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2024-10-13T10:43:27.730Z
updated: 2024-10-17T14:19:53.993Z
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
<li><a href="https://youtube-docs.techidaily.com/024-approved-a-step-by-step-approach-to-mastering-free-youtube-video-transcription/"><u>[New] 2024 Approved A Step-by-Step Approach to Mastering Free YouTube Video Transcription</u></a></li>
<li><a href="https://eaxpv-info.techidaily.com/new-in-2024-from-novice-to-vlogger-the-top-10-editing-techniques/"><u>[New] In 2024, From Novice to Vlogger The Top 10 Editing Techniques</u></a></li>
<li><a href="https://youtube-data.techidaily.com/ed-in-2024-step-by-step-video-creation-with-youtube-and-more/"><u>[Updated] In 2024, Step-by-Step Video Creation with YouTube and More</u></a></li>
<li><a href="https://extra-guidance.techidaily.com/updated-premiered-5-screen-options-for-ps5-gamers/"><u>[Updated] Premiered 5 Screen Options for PS5 Gamers</u></a></li>
<li><a href="https://win-web.techidaily.com/1728493551412-ssd5/"><u>外部SSD上のデータ不足？失われたフォルダ・ファイルを回復するための5つの方法</u></a></li>
<li><a href="https://win-web.techidaily.com/comment-restaurer-vos-fichiers-avec-les-meilleures-solutions-de-sauvegarde-externe-western-digital/"><u>Comment Restaurer Vos Fichiers Avec Les Meilleures Solutions De Sauvegarde Externe Western Digital</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-transfer-contacts-from-honor-magic-6-pro-to-outlook-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How to Transfer Contacts from Honor Magic 6 Pro to Outlook | Dr.fone</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/mastering-the-workplace-with-elegance-and-support-the-ultimate-guide-to-the-x-chair-x4-office-chair-review/"><u>Mastering the Workplace with Elegance and Support - The Ultimate Guide to the X-Chair X4 Office Chair Review</u></a></li>
<li><a href="https://win-web.techidaily.com/methode-zur-wiederherstellung-alteren-powerpoint-formats-erfolgreich-befolgen/"><u>Methode Zur Wiederherstellung Alteren PowerPoint-Formats Erfolgreich Befolgen</u></a></li>
<li><a href="https://techno-recovery.techidaily.com/pc-performance-basics-how-quickly-should-it-run/"><u>PC Performance Basics: How Quickly Should It Run?</u></a></li>
<li><a href="https://win-web.techidaily.com/profi-tipps-fur-das-seamless-cloning-und-transfer-von-vms-mit-microsoft-hyper-v-methoden-zum-importieren-und-exportieren-erlautert/"><u>Profi-Tipps Für Das Seamless Cloning Und Transfer Von VMs Mit Microsoft Hyper-V: Methoden Zum Importieren Und Exportieren Erläutert</u></a></li>
<li><a href="https://win-web.techidaily.com/schritt-fur-schritt-anleitung-grundlegende-datensynchronisierung-mit-der-software-aomei-backupper/"><u>Schritt-Für-Schritt-Anleitung: Grundlegende Datensynchronisierung Mit Der Software AOMEI Backupper</u></a></li>
<li><a href="https://win-web.techidaily.com/windows-11ssdtrim/"><u>Windows 11中启动和禁用SSD优化TRIM功能的步骤解析</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://oneplusfr.sjv.io/c/5597632/1622438/14044" target="_top" id="1622438">
  <img src="//a.impactradius-go.com/display-ad/14044-1622438" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://oneplusfr.sjv.io/i/5597632/1622438/14044" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

