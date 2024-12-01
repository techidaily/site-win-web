---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-11-26T19:54:46.879Z
updated: 2024-12-01T02:26:28.816Z
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
<li><a href="https://instagram-clips.techidaily.com/updated-in-2024-the-instagram-elite-discover-the-leading-25-influential-souls/"><u>[Updated] In 2024, The Instagram Elite Discover the Leading 25 Influential Souls</u></a></li>
<li><a href="https://youtube-videos.techidaily.com/detailed-instructions-for-embedding-and-displaying-youtube-playlists-online-for-2024/"><u>Detailed Instructions for Embedding and Displaying YouTube Playlists Online for 2024</u></a></li>
<li><a href="https://win-web.techidaily.com/discover-the-top-rated-no-cost-saving-software-for-windows-7-32-and-t-64-bits/"><u>Discover the Top Rated No-Cost Saving Software for Windows 7 (32 & T; 64 Bits)</u></a></li>
<li><a href="https://win-web.techidaily.com/ensuring-safety-with-every-save-how-to-efficiently-backup-windows-11-folders-to-an-external-hard-drive-unveiling-three-techniques/"><u>Ensuring Safety with Every Save: How to Efficiently Backup Windows 11 Folders to an External Hard Drive – Unveiling Three Techniques</u></a></li>
<li><a href="https://vp-tips.techidaily.com/image-illumination-incor-writings-on-visual-canvases-online/"><u>Image Illumination Incor Writings on Visual Canvases Online</u></a></li>
<li><a href="https://pokemon-go-android.techidaily.com/in-2024-how-does-the-stardust-trade-cost-in-pokemon-go-on-honor-x50i-drfone-by-drfone-virtual-android/"><u>In 2024, How does the stardust trade cost In pokemon go On Honor X50i? | Dr.fone</u></a></li>
<li><a href="https://some-guidance.techidaily.com/in-2024-unleashing-potential-with-the-vida-editing-suite/"><u>In 2024, Unleashing Potential with the Vida Editing Suite</u></a></li>
<li><a href="https://screen-mirroring-recording.techidaily.com/live-stream-to-instagram-from-obs-for-2024/"><u>Live Stream to Instagram From OBS for 2024</u></a></li>
<li><a href="https://fake-location.techidaily.com/methods-to-change-gps-location-on-oppo-k11-5g-drfone-by-drfone-virtual-android/"><u>Methods to Change GPS Location On Oppo K11 5G | Dr.fone</u></a></li>
<li><a href="https://win-web.techidaily.com/pcie-ssdhdd-2024/"><u>PCIe SSDへのHDD変換 - 最新手順：2024年の簡単なチェインワークフロー</u></a></li>
<li><a href="https://win-web.techidaily.com/revive-your-lost-files-restore-accidentally-deleted-documents/"><u>Revive Your Lost Files – Restore Accidentally Deleted Documents</u></a></li>
<li><a href="https://facebook.techidaily.com/streaming-on-ig-live-with-no-media-required/"><u>Streaming On IG Live With No Media Required</u></a></li>
<li><a href="https://win-web.techidaily.com/ungkapan-cukup-wajar-bagaimana-restorasi-gagal-pencabut-file-yang-tidak-terkausat-sekalian-dasar-dasar-memang-kejam/"><u>Ungkapan Cukup Wajar? Bagaimana Restorasi Gagal Pencabut File Yang Tidak Terkausat Sekalian [Dasar-Dasar Memang Kejam!]</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<iframe width="560" height="315" src="https://www.youtube.com/embed/aknYnDfODro?si=zONIVzA9FFq0rLOD" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
<!-- affiliate ads end -->

