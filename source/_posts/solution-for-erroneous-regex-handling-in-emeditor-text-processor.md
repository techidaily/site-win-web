---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-11-07T16:21:04.853Z
updated: 2024-11-12T21:38:56.437Z
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
<li><a href="https://android-location.techidaily.com/10-free-location-spoofers-to-fake-gps-location-on-your-realme-12-pro-5g-drfone-by-drfone-virtual/"><u>10 Free Location Spoofers to Fake GPS Location on your Realme 12 Pro 5G | Dr.fone</u></a></li>
<li><a href="https://vp-tips.techidaily.com/2024-approved-mememorph-machine-20/"><u>2024 Approved MemeMorph Machine 2.0</u></a></li>
<li><a href="https://win-web.techidaily.com/5-techniques-to-restore-unformatted-sd-cards-in-raw-mode/"><u>5 Techniques to Restore Unformatted SD Cards in RAW Mode</u></a></li>
<li><a href="https://win-web.techidaily.com/1728491619560-windows/"><u>發現Windows系列內損失分割區文件的最有效恢復方法</u></a></li>
<li><a href="https://hardware-tips.techidaily.com/1723125190814-discover-the-best-deal-on-eleegoo-neptune-4-pro-3d-printer-unbeatable-price-of-240-at-newegg/"><u>Discover the Best Deal on Eleegoo Neptune 4 Pro 3D Printer: Unbeatable Price of $240 at Newegg</u></a></li>
<li><a href="https://win-web.techidaily.com/expert-guide-to-forensic-data-retrieval-restoring-deleted-files-for-court-use/"><u>Expert Guide to Forensic Data Retrieval: Restoring Deleted Files for Court Use</u></a></li>
<li><a href="https://techidaily.com/how-to-downgrade-apple-iphone-6-without-data-loss-drfone-by-drfone-ios-system-repair-ios-system-repair/"><u>How to Downgrade Apple iPhone 6 without Data Loss? | Dr.fone</u></a></li>
<li><a href="https://sound-issues.techidaily.com/how-to-resolve-overwatch-talk-on-demand-tod-connection-problems/"><u>How to Resolve Overwatch Talk-On-Demand (TOD) Connection Problems</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/karaoke-usa-review-fun-filled-melodies-under-150-perfect-night-in-entertainment/"><u>Karaoke USA Review: Fun-Filled Melodies Under $150 – Perfect Night In Entertainment!</u></a></li>
<li><a href="https://win-web.techidaily.com/mastering-systemklon-und-systemmigration-eine-schrittweise-anleitung-zur-erfolgreichen-umsetzung/"><u>Mastering Systemklon Und Systemmigration: Eine Schrittweise Anleitung Zur Erfolgreichen Umsetzung</u></a></li>
<li><a href="https://win-web.techidaily.com/meilleur-logiciel-de-duplication-ssd-optimise-pour-lexar-avec-un-manuel-dutilisation-detaille-a-linterieur/"><u>Meilleur Logiciel De Duplication SSD - Optimisé Pour Lexar Avec Un Manuel D'Utilisation Détaillé À L'Intérieur</u></a></li>
<li><a href="https://win-web.techidaily.com/problemi-con-windows-10-center-sync-scopri-come-risolvere-i-problemi-comuni-del-centro-sincronizzazione/"><u>Problemi Con Windows 10 Center Sync? Scopri Come Risolvere I Problemi Comuni Del Centro Sincronizzazione</u></a></li>
<li><a href="https://win-cloud.techidaily.com/quick-and-simple-methods-for-shifting-pdf-files-from-pc-to-ios-devices/"><u>Quick & Simple Methods for Shifting PDF Files From PC to iOS Devices</u></a></li>
<li><a href="https://win-web.techidaily.com/quick-fix-finding-and-recovering-lost-downloads-from-your-pc/"><u>Quick Fix: Finding and Recovering Lost Downloads From Your PC</u></a></li>
<li><a href="https://win-web.techidaily.com/schritt-fur-schritt-anleitung-zur-wiederherstellung-geloschter-kurznotes/"><u>Schritt-Für-Schritt-Anleitung Zur Wiederherstellung Gelöschter Kurznotes</u></a></li>
<li><a href="https://fox-web3.techidaily.com/step-by-step-guide-upgrading-your-pcs-hard-drive-from-hdd-to-ssd-on-windows-os/"><u>Step-by-Step Guide: Upgrading Your PC's Hard Drive From HDD to SSD on Windows OS</u></a></li>
<li><a href="https://win-answers.techidaily.com/xboxpc-fixes-for-warzone-memory-error-understanding-and-resolving-code-0-1766/"><u>Xbox/PC Fixes for 'Warzone' Memory Error: Understanding and Resolving Code 0-1766</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://appsumo.8odi.net/c/5597632/2144280/7443" target="_top" id="2144280">
  <img src="//a.impactradius-go.com/display-ad/7443-2144280" border="0" alt="https://techidaily.com" width="600" height="90"/>
</a>
<img height="0" width="0" src="https://appsumo.8odi.net/i/5597632/2144280/7443" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

