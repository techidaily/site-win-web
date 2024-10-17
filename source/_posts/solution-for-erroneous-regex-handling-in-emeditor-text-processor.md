---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-10-10T16:25:12.668Z
updated: 2024-10-17T08:09:26.602Z
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
<li><a href="https://facebook-video-share.techidaily.com/new-2024-approved-directing-the-flow-of-digital-storytelling-through-youtube-fusion/"><u>[New] 2024 Approved Directing the Flow of Digital Storytelling Through Youtube Fusion</u></a></li>
<li><a href="https://desktop-recording.techidaily.com/new-in-2024-selecting-the-best-screen-recorder-apps-for-mac/"><u>[New] In 2024, Selecting the Best Screen Recorder Apps for Mac</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/updated-2024-approved-peervid-grabber-fb-live/"><u>[Updated] 2024 Approved PeerVid Grabber FB Live</u></a></li>
<li><a href="https://article-tips.techidaily.com/updated-in-2024-windows-11-video-mastery-utilizing-the-movie-maker-interface/"><u>[Updated] In 2024, Windows 11 Video Mastery Utilizing the Movie Maker Interface</u></a></li>
<li><a href="https://youtube-docs.techidaily.com/ed-skyline-your-videos-reach-writing-captivating-youtube-descs-using-templates/"><u>[Updated] Skyline Your Video's Reach Writing Captivating Youtube Descs Using Templates</u></a></li>
<li><a href="https://fox-cloud.techidaily.com/2024-approved-xsplit-assortment-comprehensive-gaming-evaluations/"><u>2024 Approved XSplit Assortment Comprehensive Gaming Evaluations</u></a></li>
<li><a href="https://win-web.techidaily.com/t7/"><u>容易なサムスンT7ドライブ形式変更手順をご紹介</u></a></li>
<li><a href="https://win-web.techidaily.com/1728493551412-ssd5/"><u>外部SSD上のデータ不足？失われたフォルダ・ファイルを回復するための5つの方法</u></a></li>
<li><a href="https://win-web.techidaily.com/acquire-aomei-system-recovery-expert-and-advanced-aomei-secure-backup-solutions-for-multiple-pcs/"><u>Acquire AOMEI System Recovery Expert & Advanced AOMEI Secure Backup Solutions for Multiple PCs</u></a></li>
<li><a href="https://win-web.techidaily.com/comment-restaurer-vos-fichiers-avec-les-meilleures-solutions-de-sauvegarde-externe-western-digital/"><u>Comment Restaurer Vos Fichiers Avec Les Meilleures Solutions De Sauvegarde Externe Western Digital</u></a></li>
<li><a href="https://win-solutions.techidaily.com/fixing-cod-modern-warfare-2-directx-errors-a-comprehensive-tutorial/"><u>Fixing COD Modern Warfare 2 DirectX Errors: A Comprehensive Tutorial</u></a></li>
<li><a href="https://win-web.techidaily.com/how-to-retrieve-past-drafts-and-editions-in-word-documents/"><u>How to Retrieve Past Drafts and Editions in Word Documents</u></a></li>
<li><a href="https://android-transfer.techidaily.com/how-to-transfer-data-after-switching-from-samsung-galaxy-a54-5g-to-latest-samsung-drfone-by-drfone-transfer-from-android-transfer-from-android/"><u>How to Transfer Data After Switching From Samsung Galaxy A54 5G to Latest Samsung | Dr.fone</u></a></li>
<li><a href="https://android-frp.techidaily.com/in-2024-how-can-we-bypass-asus-rog-phone-7-frp-by-drfone-android/"><u>In 2024, How Can We Bypass Asus ROG Phone 7 FRP?</u></a></li>
<li><a href="https://review-topics.techidaily.com/in-2024-how-to-fix-life360-shows-wrong-location-on-motorola-moto-g73-5g-drfone-by-drfone-virtual-android/"><u>In 2024, How to Fix Life360 Shows Wrong Location On Motorola Moto G73 5G? | Dr.fone</u></a></li>
<li><a href="https://win-web.techidaily.com/methode-zur-wiederherstellung-alteren-powerpoint-formats-erfolgreich-befolgen/"><u>Methode Zur Wiederherstellung Alteren PowerPoint-Formats Erfolgreich Befolgen</u></a></li>
<li><a href="https://win-web.techidaily.com/profi-tipps-fur-das-seamless-cloning-und-transfer-von-vms-mit-microsoft-hyper-v-methoden-zum-importieren-und-exportieren-erlautert/"><u>Profi-Tipps Für Das Seamless Cloning Und Transfer Von VMs Mit Microsoft Hyper-V: Methoden Zum Importieren Und Exportieren Erläutert</u></a></li>
<li><a href="https://win-web.techidaily.com/schritt-fur-schritt-anleitung-grundlegende-datensynchronisierung-mit-der-software-aomei-backupper/"><u>Schritt-Für-Schritt-Anleitung: Grundlegende Datensynchronisierung Mit Der Software AOMEI Backupper</u></a></li>
<li><a href="https://win-web.techidaily.com/windows-11ssdtrim/"><u>Windows 11中启动和禁用SSD优化TRIM功能的步骤解析</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2037359/7443" target="_top" id="2037359">
  <img src="//a.impactradius-go.com/display-ad/7443-2037359" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2037359/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

