---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-11-17T02:15:49.608Z
updated: 2024-11-23T00:25:45.525Z
tags:
  - product
categories:
  - emeditor
thumbnail: https://thmb.techidaily.com/6a8b7b3cdb25a03e07ba1819bb3940ce3cb079bf3680cebd2f9e48a956c136d3.jpg
---

## Solution For Erroneous Regex Handling In EmEditor Text Processor

April 9, 2009 at 9:40 pm [#7138](https://tools.techidaily.com/emeditor/products/) 

[![](https://secure.gravatar.com/avatar/a0a6377144ed3636f985d87303f65ed2?s=80&d=identicon&r=g)Yutaka Emura](https://www.emeditor.com/forums/users/yemura/ "View Yutaka Emura's profile")

Keymaster

> Flint wrote:  
> I noticed strange problems in how EE processes regular expressions.
> 
> **1.** Start the portable version of EE 8.04 with clean settings and open a text file with the following contents:
> 
>> MDB  
> 
> >NSCopy +  
> 
> >Resourse Extractor +
> 
> **2.** Press Ctrl+H, enter the Find expression:  
> ^(\[^n\])  
> and Replace with expression:  
> \>1
> 
> **3.** Check the **Use Regular Expressions** checkbox, press **Replace All**.
> 
> **4.** The result is:
> 
>>> MDB  
> 
> >>>N>SCopy +  
> 
> >>Resourse Extractor +
> 
> You can see that the second line is processed incorrectly.
> 
> If I perform the same find-replace step-by-step, I get the same result (in the “NSCopy” string the letters N and S are found and replaced as if they were located at the beginning of the line), though they are not.

 I reproduced your issue, and I will fix this issue soon. Thanks!

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
<li><a href="https://tech-haven.techidaily.com/how-the-synergy-of-onlyoffice-docspace-and-chatgpt-revolutionizes-task-management/"><u>How the Synergy of ONLYOFFICE DocSpace and ChatGPT Revolutionizes Task Management</u></a></li>
<li><a href="https://blog-min.techidaily.com/how-to-restore-missing-photos-files-from-nubia-red-magic-8s-pro-by-fonelab-android-recover-photos/"><u>How To Restore Missing Photos Files from Nubia Red Magic 8S Pro.</u></a></li>
<li><a href="https://extra-skills.techidaily.com/in-2024-key-approaches-converting-visual-content-on-pinterest-to-audio/"><u>In 2024, Key Approaches Converting Visual Content on Pinterest To Audio</u></a></li>
<li><a href="https://article-helps.techidaily.com/in-2024-navigating-the-maze-of-tiktoks-bulk-video-transfer/"><u>In 2024, Navigating the Maze of TikTok's Bulk Video Transfer</u></a></li>
<li><a href="https://extra-lessons.techidaily.com/mobile-magic-booster-free-high-quality-photo-amplification/"><u>Mobile Magic Booster Free, High-Quality Photo Amplification</u></a></li>
<li><a href="https://win-blog.techidaily.com/no-more-interruptions-overcoming-metro-exodus-on-pc-crashes-for-smooth-gaming/"><u>No More Interruptions: Overcoming Metro Exodus on PC Crashes for Smooth Gaming</u></a></li>
<li><a href="https://win-web.techidaily.com/professionelle-tipps-zur-sofortigen-absicherung-ihres-gmail-profils-gegen-das-loschen/"><u>Professionelle Tipps Zur Sofortigen Absicherung Ihres Gmail-Profils Gegen Das Löschen</u></a></li>
<li><a href="https://article-posts.techidaily.com/prove-youre-a-pro-lightning-fast-editing-in-windows-11-videos/"><u>Prove You're a Pro Lightning-Fast Editing in Windows 11 Videos</u></a></li>
<li><a href="https://win-web.techidaily.com/resolving-the-issue-uninstalling-and-re-installing-ipod-driver-on-windows-11/"><u>Resolving the Issue: Uninstalling and Re-Installing iPod Driver on Windows 11</u></a></li>
<li><a href="https://tech-renaissance.techidaily.com/steps-to-take-when-the-mail-app-stops-working-on-iphone/"><u>Steps to Take When the Mail App Stops Working on iPhone</u></a></li>
<li><a href="https://win-web.techidaily.com/techniques-securisees-pour-cloner-le-systeme-dexploitation-en-direct-sur-un-ssd-samsung-850-evo-sous-windows/"><u>Techniques Sécurisées Pour Cloner Le Système D'Exploitation en Direct Sur Un SSD Samsung 850 EVO Sous Windows</u></a></li>
<li><a href="https://win-web.techidaily.com/trouble-with-duplicating-data-problems-using-an-alternative-apricorn-ez-gig-iv-clone/"><u>Trouble with Duplicating Data: Problems Using an Alternative Apricorn EZ Gig IV Clone</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/qfCSLAhd4FY?si=CUBztmilaeAwl1lw&autoplay=1" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

