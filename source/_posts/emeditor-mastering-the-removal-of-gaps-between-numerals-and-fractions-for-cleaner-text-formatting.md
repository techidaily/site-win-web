---
title: "EmEditor: Mastering the Removal of Gaps Between Numerals and Fractions for Cleaner Text Formatting"
date: 2025-01-07T19:58:55.049Z
updated: 2025-01-14T21:10:29.868Z
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
<li><a href="https://instagram-videos.techidaily.com/updated-2024-approved-imovie-skills-producing-engaging-and-profitable-square-video-feeds/"><u>[Updated] 2024 Approved IMovie Skills Producing Engaging and Profitable Square Video Feeds</u></a></li>
<li><a href="https://fox-hovers.techidaily.com/updated-creating-breathtaking-slow-motion-photo-editing-techniques-explored/"><u>[Updated] Creating Breathtaking Slow Motion Photo Editing Techniques Explored</u></a></li>
<li><a href="https://facebook-record-videos.techidaily.com/updated-in-2024-a-comprehensive-look-at-youtubes-adsense-mechanisms/"><u>[Updated] In 2024, A Comprehensive Look at YouTube's AdSense Mechanisms</u></a></li>
<li><a href="https://video-capture.techidaily.com/windowsyoutube/"><u>「WindowsパソコンでYouTubeアクセス課題：ビデオ鑑賞・再生対策方法」</u></a></li>
<li><a href="https://techtrends.techidaily.com/15-best-windows-11-themes-to-download-for-free/"><u>15 Best Windows 11 Themes to Download for Free</u></a></li>
<li><a href="https://win-web.techidaily.com/5-effective-techniques-for-retrieving-erased-browsing-data-from-google-chrome/"><u>5 Effective Techniques for Retrieving Erased Browsing Data From Google Chrome</u></a></li>
<li><a href="https://win-web.techidaily.com/windows-1087ssd/"><u>簡單指南：在Windows 10/8/7系统下轻松转移SSD到容器</u></a></li>
<li><a href="https://win-web.techidaily.com/1728501228646-aomei-backupper/"><u>AOMEI Backupper 工具指南：完整备份和系统还原教程</u></a></li>
<li><a href="https://win-web.techidaily.com/1728510133745-aomei-backupper-windows/"><u>AOMEI Backupperのインストールと利用手順 - Windowsコマンドラインで</u></a></li>
<li><a href="https://win-superb.techidaily.com/gina-raimondo-and-wang-wentao-pledge-joint-effort-in-commerce-through-bilateral-working-group-and-data-sharing-on-export-enforcement-insights-by-yl-computin54/"><u>Gina Raimondo and Wang Wentao Pledge Joint Effort in Commerce Through Bilateral Working Group & Data Sharing on Export Enforcement – Insights by YL Computing | YL Software</u></a></li>
<li><a href="https://media-tips.techidaily.com/improving-spotifys-ai-dj-with-local-news-integration-a-next-level-music-experience/"><u>Improving Spotify's AI DJ with Local News Integration: A Next-Level Music Experience</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/in-depth-analysis-samsungs-galaxy-chromebook-version-2-a-game-changer-for-on-the-go-workers/"><u>In-Depth Analysis: Samsung's Galaxy Chromebook Version 2 - A Game-Changer for On-the-Go Workers</u></a></li>
<li><a href="https://win-web.techidaily.com/le-due-tecniche-ottimali-per-eliminare-gli-spazi-neri-su-windows-11/"><u>Le Due Tecniche Ottimali per Eliminare Gli Spazi Neri Su Windows 11</u></a></li>
<li><a href="https://win-web.techidaily.com/recuperacion-efectiva-de-datos-desaparecidos-en-un-portatil-dell/"><u>Recuperación Efectiva De Datos Desaparecidos en Un Portátil Dell</u></a></li>
<li><a href="https://win-web.techidaily.com/schritt-fur-schritt-anleitung-zum-erfolgreichen-klonen-einer-ubuntu-festplatte/"><u>Schritt-Für-Schritt Anleitung Zum Erfolgreichen Klonen Einer Ubuntu-Festplatte</u></a></li>
<li><a href="https://win-web.techidaily.com/tackle-the-dell-boot-loop-top-3-proven-methods-for-windows-11-troubleshooting/"><u>Tackle the Dell Boot Loop: Top 3 Proven Methods for Windows 11 Troubleshooting</u></a></li>
<li><a href="https://digital-screen-recording.techidaily.com/top-10-affectionate-emulators-for-android-and-3ds-for-2024/"><u>Top 10 Affectionate Emulators for Android and 3DS for 2024</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/top-10-password-cracking-tools-for-oneplus-ace-3-by-drfone-android/"><u>Top 10 Password Cracking Tools For OnePlus Ace 3</u></a></li>
<li><a href="https://win-web.techidaily.com/ultimate-guide-top-three-methods-for-factory-resetting-a-damaged-iphone-display/"><u>Ultimate Guide: Top Three Methods for Factory Resetting a Damaged iPhone Display</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/2ipTu54inBo?si=gRegjvtVq5gm_PHo" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

