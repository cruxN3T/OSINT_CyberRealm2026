Author: Juan Ford

# Challenge 1: Ghostwritten (OSINT)


Description: Cyber Realm a Trading Card Game on Cybersecurity has developed a following within specialized security communities, where credibility is built on contribution and trust.
Recently, an individual using the name "Ghost" (profile name: Mr. Ghost) has been actively sharing what they claim are "leaked" or "exclusive" rulebook updates for the game.
These documents are being presented as official or insider materials, and the individual appears to be leveraging them to establish credibility and authority within the community.
Intelligence suggests that this "Ghost" account on LinkedIn claims a connection to the legitimate creator of Cyber Realm.

Your task: Identify the true creator of Cyber Realm, investigate the nature of "Ghost's" claimed connection, 
trace how the materials are being redistributed, and uncover any hidden intelligence within the leaked digital artifacts themselves.
The documents may seem unremarkable at first but thorough examination often reveals more than meets the eye.
The flag is embedded in one of the rulebooks.

Hint1: A quick web search for "Cyber Realm trading card game" or "Cyber Realm TCG" will lead you to the official website, where you can confirm the legitimate creator and learn more about the game.
Hint2: The leaked rulebooks are available for download directly via LinkedIn.
Hint3: Check the documents EXIF Metadata



# Ghostwritten Solution

Research the game
Google "Cyber Realm trading card game" or "Cyber Realm TCG".
The top result is the official website (cyberrealmtcg.com). Visit it and confirm the creator is Juan Ford.
Locate the suspicious account
Go to the LinkedIn profile of Juan Ford: https://www.linkedin.com/in/juanford/
look at connections look for user Mr. Ghost
Look at Mr. Ghost’s recent posts. You’ll see claims of being connected to or sharing “exclusive” Cyber Realm rulebook updates (v2.0 and v2.1).
Download the rulebooks
In the posts, click the gofile.io mirror links (or scan the QR code if shown).
Download both v2.1.pdf and v2.0.pdf. No account or login required.
Inspect the first document (v2.1)
Open v2.1.pdf → Read the rules (nothing obvious) → Check file metadata/properties
Or use an online metadata viewer/exiftool
You’ll find a fake/teaser flag like SC6{try_harder} — this tells you to keep looking.
![[Screenshot 2026-02-10 191648.png]]
Inspect the second document (v2.0)
Repeat the metadata check on v2.0.pdf
The real flag is hidden there (e.g., in Author, Comments, or custom properties)
Flag1:
![[Screenshot 2026-02-10 191821.png]]






# Challenge 2: Where Signals Converge (OSINT)


Description: A community of Cyber Realm trading card game enthusiasts in the Spokane/PNW area frequently organizes in-person meetups, often overlapping with local hacker groups like DC509 (Spokane's DEF CON group).
The Mastodon account @Ghostinthewires (the same individual from Challenge 1) follows the official @cyberrealm account and has been posting about recent gatherings including visible WiFi BSSIDs from the locations and photos of gameplay sessions.
Some of these photos appear to be reposts or "borrowed" from other sources, and one matching image contains valuable intelligence in its comments section.
Your task: investigate Ghosts Mastodon posts and see what is odd about his postings. 
The primary flag is hidden in the comments of the original (stolen) image.
Everything required is publicly available through social media, posts, images, WiFi databases, and web archives.
No active scanning or interaction beyond public browsing is needed.

Hint1: Start with the known @Ghostinthewires Mastodon account and its activity related to Cyber Realm gatherings.
Hint2: Ghost has shared photos of Cyber Realm card games that match images from other sources.
Hint3: The red herring is the wifi BSSIDs do not rely on these for the flag. 
Hint4: the key is the deleted post, use the wayback machine and view the screenshot.


# Where Signal Converge Solution

Connect the persona from Challenge 1
You already know "Mr. Ghost" from the LinkedIn profile.
The challenge mentions his Mastodon handle @Ghostinthewires (or you can search Mastodon directly for "Ghostinthewires" + "Cyber Realm").
Visit Ghost's Mastodon profile
Go to his profile page on the relevant Mastodon instance
Scroll through his recent posts. You will see:
Posts about Cyber Realm meetups.
Reposted photos of people playing Cyber Realm cards. Posts about him bragging about his fake creds. investigate those posts does anything stand out?
One very recent post saying:
"Weird, my comment from earlier vanished must be a glitch in the matrix."

Identify the post with the "vanished" comment
Use the Wayback Machine to recover the deleted comment
Go to https://archive.org/web/
Paste the direct Mastodon post URL into the search bar.![[Screenshot 2026-02-10 191512.png]]
 you’ll see a captured snapshot.
"Flag 2 was just leaked in the comments section of the photo I stole from Cyber Realms Instagram page.![[Screenshot 2026-02-10 191440.png]]
go to cyber realms instagram page
No account is needed, if you go into incognito mode and right click the image or post into a new page it bypasses that and allows you to view comments![[Screenshot 2026-02-10 191914.png]]
![[Screenshot 2026-02-10 192011.png]]Read the comment


![[Screenshot 2026-02-10 192036.png]]


# Challenge 3: Forbidden Card (OSINT)



Think you are ready to play Cyber Realm TCG?
Everything you need is exposed through public channels such as social media profiles, images, posts, and web assets. No exploitation, scanning, authentication bypass, or interaction beyond normal browsing is required or permitted.
True intelligence hides in plain sight but only for those who know where to look. 
Elite practitioners inspect every artifact: metadata, archives, source code, developer tools, network traces, and structural anomalies. Surface-level observation yields nothing. The masters go deeper.
"The Basics" are anything but basic.
Your objective: Locate a hidden flag embedded within the Cyber Realm card deck.
The flag exists in the open, but it is not immediately visible.

Hint1:Begin at the official Cyber Realm TCG website cyberrealmtcg.com
Hint2: Pay close attention to navigation menus, page titles, and console messages. The challenge mentions "The Basics"
Hint3: use dev tools to inspect that page
Hint4: *Flag1 and Flag2 both had base64 at the end of their flags these are needed to get Flag3


# Forbidden Card Solution

Start at the official website
Go to https://cyberrealmtcg.com (discovered or reinforced from prior challenges and the description's emphasis on "The Basics").
Explore the site normally first
Navigate through the menus: Home, The Basics, Training Scenarios, Products.
Read the content nothing obvious jumps out with a flag or digital deck.
go to the basics page and Open Developer Tools
Press F12 or Ctrl+Shift+I (Chrome/Firefox) to open Dev Tools.
Switch to the Console tab.
You will see a special message:
"Welcome to the Cyber Realm! Spokane Cyber Cup explorers only. (Hint: follow the path to cyberrealmtcg.com/osint) I see you poking around... see you IRL."
Follow the hidden path
Visit the hinted URL: https://cyberrealmtcg.com/osint
![[Screenshot 2026-02-10 190928.png]]

The page displays:
"SC6 OSINT Challenge 3 (OSINT)"
"A digital Cyber Realm deck once existed. Most of it is gone but traces remain. Join in the Game! Hunt the forbidden card value and assemble the master flag from leaks"
An iframe embedding a playable digital version of Cyber Realm TCG.
There are two games one that is built out in case tabletopia is full
to get flag3 the base64 that are appended at the end values from Flag1 and Flag2 are needed to get flag3 

![[Screenshot 2026-02-10 191011.png]]

Enter the digital game
Click Play (or whatever button starts the game) inside the iframe.
You now have access to a full 60-card digital deck you can browse.
Search the deck thoroughly
Flip through all 60 cards carefully.
Most cards look normal, but 8 special/anomalous cards stand out they have unusual "value" fields, alt text, or hidden attributes containing Base64 strings.
Collect the Base64 fragments
Note down the 8 strings you find:
dvX3RyeV9hZ2Fpbn0=
RvbnRfZ2l2ZV91cCF9
Nsb3NlX2J1dF9ub3RfY29ycmVjdCF9
FsbW9zdCF9
hhcmRlclRyeVlvdU11c3QhfQ==
tlZXBMb29raW5nIX0=
NvdW50TW9yZUNhcmRzX1RyeUFnYWluIX0=
NvbXBsZXRlIX0= ← this is the correct one (the "forbidden card" value)
(The first 7 are red herrings that decode to teasing messages like "Go try again", "Almost!", "Keep Looking!", etc.)
![[Screenshot 2026-02-10 191255.png]]

Assemble the master flag
Combine the correct fragment with the partial components you collected from Challenges 1 and 2:
Full Base64 string:
U0M2e0N5YmVyUmVhbG1UQ0dfRmxhZ18zX0NvbXBsZXRlIX0=
(The prefix comes from piecing prior flag parts — e.g., something like U0M2e0N5YmVyUmVhbG1UQ0dfRmxhZ18zX0 + NvbXBsZXRlIX0=)
Decode the final Base64
Decode U0M2e0N5YmVyUmVhbG1UQ0dfRmxhZ18zX0NvbXBsZXRlIX0=
SC6{CyberRealmTCG_Flag_3_Complete!}



![[Screenshot 2026-02-10 192602.png]]


