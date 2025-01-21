---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2025-01-19T00:30:52.538Z
updated: 2025-01-21T07:25:07.131Z
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
<li><a href="https://desktop-recording.techidaily.com/new-mastering-zoom-discussion-essential-tactics-for-virtual-conversations-for-2024/"><u>[New] Mastering Zoom Discussion Essential Tactics for Virtual Conversations for 2024</u></a></li>
<li><a href="https://article-knowledge.techidaily.com/updated-5-esteemed-platforms-for-easy-text-effect-implementation-for-2024/"><u>[Updated] 5 Esteemed Platforms for Easy Text Effect Implementation for 2024</u></a></li>
<li><a href="https://screen-activity-recording.techidaily.com/updated-the-filmmakers-handbook-to-superior-voice-overseeing-for-2024/"><u>[Updated] The Filmmaker's Handbook to Superior Voice Overseeing for 2024</u></a></li>
<li><a href="https://win-web.techidaily.com/1-streamline-your-search-locate-any-file-in-bulk-with-text-editor-add-open-docs-feature/"><u>1. Streamline Your Search: Locate Any File in Bulk with Text Editor - Add Open Docs Feature</u></a></li>
<li><a href="https://win-web.techidaily.com/3-efektif-tekniks-buka-program-pada-operating-system-windows-incl-win-11-10-8-and-7/"><u>3 Efektif Tekniks Buka Program Pada Operating System Windows - Incl. Win 11, 10, 8 & 7</u></a></li>
<li><a href="https://data-wizards.techidaily.com/fixing-damaged-mp4mov-videos-with-ease-a-step-by-step-guide-using-vlc/"><u>Fixing Damaged MP4/MOV Videos with Ease: A Step-by-Step Guide Using VLC</u></a></li>
<li><a href="https://android-unlock.techidaily.com/how-to-unlock-oppo-find-n3-phone-with-broken-screen-by-drfone-android/"><u>How to Unlock Oppo Find N3 Phone with Broken Screen</u></a></li>
<li><a href="https://tech-revival.techidaily.com/navigating-the-world-of-edge-computing-with-on-device-ai-a-comprehensive-guide/"><u>Navigating the World of Edge Computing with On-Device AI: A Comprehensive Guide</u></a></li>
<li><a href="https://win-web.techidaily.com/probleme-mit-der-nachrichtensynchronisation-auf-iphone-ipad-und-mac-losungen-fur-den-icloud/"><u>Probleme Mit Der Nachrichtensynchronisation Auf IPhone, iPad Und Mac - Lösungen Für Den Icloud</u></a></li>
<li><a href="https://win-web.techidaily.com/reviving-your-sql-data-a-guide-to-recovering-from-a-bak-backup-using-three-techniques/"><u>Reviving Your SQL Data: A Guide to Recovering From a .BAK Backup Using Three Techniques</u></a></li>
<li><a href="https://win-web.techidaily.com/ultimate-tutorial-navigating-and-optimizing-file-search-in-windows-11/"><u>Ultimate Tutorial: Navigating and Optimizing File Search in Windows 11</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/gyGoQi7hsZk?si=8OcKcPUj2wSBmVZ1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

