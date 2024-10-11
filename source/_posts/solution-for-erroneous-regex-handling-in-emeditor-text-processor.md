---
title: Solution For Erroneous Regex Handling In EmEditor Text Processor
date: 2024-10-09T01:31:31.515Z
updated: 2024-10-11T02:34:33.266Z
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
<li><a href="https://youtube-web.techidaily.com/n-2024-direct-from-spotify-to-youtube-best-apps-for-streaming-conversions/"><u>[New] In 2024, Direct From Spotify to YouTube Best Apps for Streaming Conversions</u></a></li>
<li><a href="https://win-web.techidaily.com/1-top-strategies-for-streaming-your-ipad-content-onto-television/"><u>1. Top Strategies for Streaming Your iPad Content Onto Television</u></a></li>
<li><a href="https://howto.techidaily.com/best-methods-for-honor-magic-5-lite-wont-turn-on-drfone-by-drfone-fix-android-problems-fix-android-problems/"><u>Best Methods for Honor Magic 5 Lite Wont Turn On | Dr.fone</u></a></li>
<li><a href="https://win-web.techidaily.com/best-methods-to-seamlessly-stream-your-mac-screen-to-a-television/"><u>Best Methods to Seamlessly Stream Your Mac Screen to a Television</u></a></li>
<li><a href="https://os-tips.techidaily.com/comprehensive-analysis-of-the-butterfly-two-in-one-charger-by-twelve-south-the-travelers-must-have-companion-with-magsafe-technology/"><u>Comprehensive Analysis of the ButterFly Two-in-One Charger by Twelve South: The Traveler's Must-Have Companion with MagSafe Technology</u></a></li>
<li><a href="https://buynow-reviews.techidaily.com/comprehensive-guide-to-the-asus-bw-16d1x-u-a-stylish-blu-ray-drive-with-notable-quirks/"><u>Comprehensive Guide to the Asus BW-16D1X-U: A Stylish Blu-Ray Drive with Notable Quirks</u></a></li>
<li><a href="https://win-web.techidaily.com/download-our-free-tool-transform-your-pdfs-into-professional-powerpoint-presentations/"><u>Download Our Free Tool – Transform Your PDFs Into Professional PowerPoint Presentations</u></a></li>
<li><a href="https://win-web.techidaily.com/effortless-techniques-for-capturing-high-quality-tidal-sounds/"><u>Effortless Techniques for Capturing High-Quality Tidal Sounds</u></a></li>
<li><a href="https://audio-editing.techidaily.com/elevating-audio-excellence-adjusting-pitch-in-audacity-without-compromising-quality-for-2024/"><u>Elevating Audio Excellence Adjusting Pitch in Audacity without Compromising Quality for 2024</u></a></li>
<li><a href="https://some-techniques.techidaily.com/in-2024-exclusive-exploration-superior-vr-games-on-google-cardboard/"><u>In 2024, Exclusive Exploration Superior VR Games on Google Cardboard</u></a></li>
<li><a href="https://facebook-clips.techidaily.com/in-2024-faceless-watchers-of-fb-flashbacks/"><u>In 2024, Faceless Watchers of Fb Flashbacks</u></a></li>
<li><a href="https://phone-solutions.techidaily.com/in-2024-will-the-ipogo-get-you-banned-and-how-to-solve-it-on-infinix-note-30-vip-drfone-by-drfone-virtual-android/"><u>In 2024, Will the iPogo Get You Banned and How to Solve It On Infinix Note 30 VIP | Dr.fone</u></a></li>
<li><a href="https://win-web.techidaily.com/instant-tips-how-to-enjoy-footage-in-a-snail-pace-with-these-simple-steps/"><u>Instant Tips: How to Enjoy Footage in a Snail-Pace with These Simple Steps</u></a></li>
<li><a href="https://easy-unlock-android.techidaily.com/mastering-android-device-manager-the-ultimate-guide-to-unlocking-your-realme-11x-5g-device-by-drfone-android/"><u>Mastering Android Device Manager The Ultimate Guide to Unlocking Your Realme 11X 5G Device</u></a></li>
<li><a href="https://win-web.techidaily.com/mastering-the-art-of-deleting-safari-bookmarks-with-these-quick-tips-for-ipad-users/"><u>Mastering the Art of Deleting Safari Bookmarks with These Quick Tips for iPad Users</u></a></li>
<li><a href="https://win-web.techidaily.com/quick-and-effortless-methods-to-import-blu-ray-content-onto-your-ios-device/"><u>Quick and Effortless Methods to Import Blu-Ray Content Onto Your iOS Device</u></a></li>
<li><a href="https://win-howtos.techidaily.com/razer-keyboard-trouble-heres-how-to-restore-the-backlit-functionality/"><u>Razer Keyboard Trouble? Here's How to Restore the Backlit Functionality</u></a></li>
<li><a href="https://win-web.techidaily.com/simple-steps-converting-your-youtube-videos-for-seamless-viewing-on-an-ipad/"><u>Simple Steps: Converting Your YouTube Videos for Seamless Viewing on an iPad</u></a></li>
<li><a href="https://win-web.techidaily.com/the-essential-handbook-for-navigating-and-optimizing-the-apowermanager-interface/"><u>The Essential Handbook for Navigating and Optimizing the ApowerManager Interface</u></a></li>
</ul></div>

<!-- affiliate ads begin -->
<a href="https://dhgate.sjv.io/c/5597632/1175223/12108" target="_top" id="1175223">
  <img src="//a.impactradius-go.com/display-ad/12108-1175223" border="0" alt="https://techidaily.com" width="728" height="90"/>
</a>
<img height="0" width="0" src="https://dhgate.sjv.io/i/5597632/1175223/12108" style="position:absolute;visibility:hidden;" border="0" />
<!-- affiliate ads end -->

