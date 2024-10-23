---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-10-17T20:58:20.220Z
updated: 2024-10-22T20:23:33.231Z
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
<li><a href="https://youtube-zero.techidaily.com/ed-easy-guide-to-youtube-livestreaming-from-google-meet-for-2024/"><u>[Updated] Easy Guide to YouTube Livestreaming From Google Meet for 2024</u></a></li>
<li><a href="https://some-skills.techidaily.com/2024-approved-transfer-tactics-efficiently-getting-data-on-your-computer/"><u>2024 Approved Transfer Tactics Efficiently Getting Data On Your Computer</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/5-ways-to-restart-poco-c50-without-power-button-drfone-by-drfone-reset-android-reset-android/"><u>5 Ways to Restart Poco C50 Without Power Button | Dr.fone</u></a></li>
<li><a href="https://program-issues.techidaily.com/1723011069007-assassins-creed-odyssey-quick-fixes-for-seamless-gameplay-without-any-more-pc-crashes/"><u>Assassin's Creed Odyssey - Quick Fixes for Seamless Gameplay Without Any More PC Crashes!</u></a></li>
<li><a href="https://win-web.techidaily.com/discover-the-top-rated-no-cost-saving-software-for-windows-7-32-and-t-64-bits/"><u>Discover the Top Rated No-Cost Saving Software for Windows 7 (32 & T; 64 Bits)</u></a></li>
<li><a href="https://win-web.techidaily.com/ensuring-safety-with-every-save-how-to-efficiently-backup-windows-11-folders-to-an-external-hard-drive-unveiling-three-techniques/"><u>Ensuring Safety with Every Save: How to Efficiently Backup Windows 11 Folders to an External Hard Drive – Unveiling Three Techniques</u></a></li>
<li><a href="https://win-amazing.techidaily.com/getting-started-with-asus-mousepad-fresh-downloads-of-windows-compatible-drivers/"><u>Getting Started with ASUS Mousepad: Fresh Downloads of Windows-Compatible Drivers</u></a></li>
<li><a href="https://android-location.techidaily.com/getting-the-pokemon-go-gps-signal-not-found-11-error-in-realme-gt-5-240w-drfone-by-drfone-virtual/"><u>Getting the Pokemon Go GPS Signal Not Found 11 Error in Realme GT 5 (240W) | Dr.fone</u></a></li>
<li><a href="https://youtube-data.techidaily.com/24-adrevenue-on-youtube-unpacked-average-income-from-1000-viewers-engagement/"><u>In 2024, AdRevenue on YouTube Unpacked Average Income From 1,000 Viewers' Engagement</u></a></li>
<li><a href="https://win-web.techidaily.com/1728475032768-nas/"><u>NASデータ失われたら速やかに復元！バッファローを使ってみる方法</u></a></li>
<li><a href="https://win-web.techidaily.com/outlook-2010and/"><u>Outlook 2010のメールアカウントを安全にエクスポート&バックアップする詳細ガイド</u></a></li>
<li><a href="https://techtrends.techidaily.com/overcome-androids-parsing-challenges-8-effective-fixes/"><u>Overcome Android's Parsing Challenges: 8 Effective Fixes</u></a></li>
<li><a href="https://win-web.techidaily.com/pcie-ssdhdd-2024/"><u>PCIe SSDへのHDD変換 - 最新手順：2024年の簡単なチェインワークフロー</u></a></li>
<li><a href="https://discover-hacks.techidaily.com/transformez-vos-fichiers-avi-en-mp3-sans-frais-haute-definition-assuree/"><u>Transformez Vos Fichiers AVI en MP3 Sans Frais - Haute Définition Assurée</u></a></li>
<li><a href="https://win-web.techidaily.com/1728504019733-windows-11/"><u>Windows 11 系统防护功能显示为灰色的问题及其修复方法</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<span id="1993645">
					<video width="576" height="240" style="cursor:pointer"
           poster="//a.impactradius-go.com/display-clicktoplayimage/1993645.png"
           onclick="if(!this.playClicked){this.play();this.setAttribute('controls',true);this.playClicked=true;}">
	   <source src="//a.impactradius-go.com/display-ad/22993-1993645">
	   <img src="//a.impactradius-go.com/display-clicktoplayimage/1993645.png" style="border: none; height: 100%; width: 100%; object-fit: contain">
	</video>
	<div style="width:360px;text-align:center"><a href="javascript:window.open(decodeURIComponent('https%3A%2F%2Fhomestyler.sjv.io%2Fc%2F5597632%2F1993645%2F22993'), '_blank');void(0);">Click here</a></div>
</span>
<img height="0" width="0" src="https://imp.pxf.io/i/5597632/1993645/22993" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

