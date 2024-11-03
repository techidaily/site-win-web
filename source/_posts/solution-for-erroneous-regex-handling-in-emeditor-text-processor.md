---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-11-02T22:54:50.643Z
updated: 2024-11-03T16:45:47.442Z
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
<li><a href="https://fox-hovers.techidaily.com/new-disable-youtubes-automatic-video-playback-trigger/"><u>[New] Disable YouTube's Automatic Video Playback Trigger</u></a></li>
<li><a href="https://youtube-web.techidaily.com/xpert-roundup-of-platforms-for-video-intro-acquisition-for-2024/"><u>[New] Expert Roundup of Platforms for Video Intro Acquisition for 2024</u></a></li>
<li><a href="https://remote-screen-capture.techidaily.com/updated-in-2024-highlighting-the-best-practices-in-screen-recording-facetime-calls/"><u>[Updated] In 2024, Highlighting the Best Practices in Screen Recording FaceTime Calls</u></a></li>
<li><a href="https://win-web.techidaily.com/cloning-a-dynamic-drive-on-windows-11-two-effective-methods-explained/"><u>Cloning a Dynamic Drive on Windows 11: Two Effective Methods Explained</u></a></li>
<li><a href="https://iphone-unlock.techidaily.com/how-to-turn-off-find-my-apple-iphone-se-when-phone-is-broken-drfone-by-drfone-ios/"><u>How to Turn Off Find My Apple iPhone SE when Phone is Broken? | Dr.fone</u></a></li>
<li><a href="https://activate-lock.techidaily.com/in-2024-how-to-remove-iphone-6-plus-activation-lock-by-drfone-ios/"><u>In 2024, How to Remove iPhone 6 Plus Activation Lock</u></a></li>
<li><a href="https://location-social.techidaily.com/in-2024-set-your-preferred-job-location-on-linkedin-app-of-your-apple-iphone-11-pro-drfone-by-drfone-virtual-ios/"><u>In 2024, Set Your Preferred Job Location on LinkedIn App of your Apple iPhone 11 Pro | Dr.fone</u></a></li>
<li><a href="https://tech-savvy.techidaily.com/quick-fix-techniques-resolving-errors-in-windows-11-computers/"><u>Quick Fix Techniques: Resolving Errors in Windows 11 Computers</u></a></li>
<li><a href="https://tech-revival.techidaily.com/say-it-like-you-mean-it-androids-voicegpt-guide/"><u>Say It Like You Mean It: Android’s VoiceGPT Guide</u></a></li>
<li><a href="https://win-web.techidaily.com/simplify-your-network-storage-aomeis-ultimate-guide-to-backing-up-your-buffalo-nas-on-pc/"><u>Simplify Your Network Storage: AOMEI's Ultimate Guide to Backing Up Your Buffalo NAS on PC</u></a></li>
<li><a href="https://win-web.techidaily.com/solving-issues-with-acers-erecovery-management-functionality-comprehensive-tips/"><u>Solving Issues With Acer's eRecovery Management Functionality - Comprehensive Tips</u></a></li>
<li><a href="https://win-web.techidaily.com/tutorial-completo-para-crear-una-imagen-de-disco-con-cloner-y-clonezilla-usando-gpt/"><u>Tutorial Completo Para Crear Una Imagen De Disco Con Cloner Y Clonezilla Usando GPT技術</u></a></li>
<li><a href="https://win-web.techidaily.com/aomei-backupper/"><u>データを失わないために! AOMEI Backupper：プロフェッショナルなバックアップソリューションのお歳暮無料版</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://aligracehair.sjv.io/c/5597632/2115946/19272" target="_top" id="2115946">
  <img src="//a.impactradius-go.com/display-ad/19272-2115946" border="0" alt="https://techidaily.com" width="300" height="90"/>
</a>
<img height="0" width="0" src="https://aligracehair.sjv.io/i/5597632/2115946/19272" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

