---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-10-25T17:43:57.277Z
updated: 2024-10-29T03:46:24.352Z
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
<li><a href="https://on-screen-recording.techidaily.com/new-2024-approved-impeccablecapture-studio-suite-windows-10-edition/"><u>[New] 2024 Approved ImpeccableCapture Studio Suite (Windows 10 Edition)</u></a></li>
<li><a href="https://youtube-data.techidaily.com/ed-in-2024-the-best-budget-friendly-closer-tutorials-top-6-edition/"><u>[Updated] In 2024, The Best Budget-Friendly Closer Tutorials Top 6 Edition</u></a></li>
<li><a href="https://screen-recording.techidaily.com/updated-leveraging-tech-for-better-facebook-live-records/"><u>[Updated] Leveraging Tech for Better Facebook Live Records</u></a></li>
<li><a href="https://win-web.techidaily.com/acquire-aomei-system-recovery-expert-and-advanced-aomei-secure-backup-solutions-for-multiple-pcs/"><u>Acquire AOMEI System Recovery Expert & Advanced AOMEI Secure Backup Solutions for Multiple PCs</u></a></li>
<li><a href="https://win-web.techidaily.com/clone-prozess-von-festplatten-auf-ssds-mit-clonezilla-eine-einfache-und-effiziente-methode/"><u>Clone-Prozess Von Festplatten Auf SSDs Mit Clonezilla: Eine Einfache Und Effiziente Methode</u></a></li>
<li><a href="https://win-web.techidaily.com/comment-restaurer-vos-fichiers-avec-les-meilleures-solutions-de-sauvegarde-externe-western-digital/"><u>Comment Restaurer Vos Fichiers Avec Les Meilleures Solutions De Sauvegarde Externe Western Digital</u></a></li>
<li><a href="https://win-web.techidaily.com/how-to-retrieve-past-drafts-and-editions-in-word-documents/"><u>How to Retrieve Past Drafts and Editions in Word Documents</u></a></li>
<li><a href="https://change-location.techidaily.com/how-to-watch-hulu-outside-us-on-oppo-a38-drfone-by-drfone-virtual-android/"><u>How to Watch Hulu Outside US On Oppo A38 | Dr.fone</u></a></li>
<li><a href="https://change-location.techidaily.com/in-2024-catchemall-celebrate-national-pokemon-day-with-virtual-location-on-vivo-t2-pro-5g-drfone-by-drfone-virtual-android/"><u>In 2024, CatchEmAll Celebrate National Pokémon Day with Virtual Location On Vivo T2 Pro 5G | Dr.fone</u></a></li>
<li><a href="https://youtube-stream.techidaily.com/in-2024-growth-hurdle-cleared-500-subscribers-win/"><u>In 2024, Growth Hurdle Cleared 500 Subscribers Win</u></a></li>
<li><a href="https://win-web.techidaily.com/methode-zur-wiederherstellung-alteren-powerpoint-formats-erfolgreich-befolgen/"><u>Methode Zur Wiederherstellung Alteren PowerPoint-Formats Erfolgreich Befolgen</u></a></li>
<li><a href="https://fake-location.techidaily.com/read-this-guide-to-find-a-reliable-alternative-to-fake-gps-on-itel-a60-drfone-by-drfone-virtual-android/"><u>Read This Guide to Find a Reliable Alternative to Fake GPS On Itel A60 | Dr.fone</u></a></li>
<li><a href="https://win-web.techidaily.com/resoudre-les-problemes-de-fausses-limitations-de-stockage-apres-avoir-clone-un-disque-dur-explication-claire-et-pratique/"><u>Résoudre Les Problèmes De Fausses Limitations De Stockage Après Avoir Cloné Un Disque Dur : Explication Claire Et Pratique</u></a></li>
<li><a href="https://win-web.techidaily.com/schritt-fur-schritt-anleitung-grundlegende-datensynchronisierung-mit-der-software-aomei-backupper/"><u>Schritt-Für-Schritt-Anleitung: Grundlegende Datensynchronisierung Mit Der Software AOMEI Backupper</u></a></li>
<li><a href="https://fox-http.techidaily.com/soundbite-strategies-transform-your-voice-records/"><u>Soundbite Strategies Transform Your Voice Records</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://ephamedtechinc.pxf.io/c/5597632/2137205/26400" target="_top" id="2137205">
  <img src="//a.impactradius-go.com/display-ad/26400-2137205" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://ephamedtechinc.pxf.io/i/5597632/2137205/26400" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

