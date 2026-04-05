# TryHackMe: Digital Footprint - OSINT Write-up

## Task 1: The Leaked Photo (Geolocation & EXIF Analysis)

**Objective:** Figure out where a leaked photo of a residential property—believed to be linked to ACME Jet's early operations—was taken.

<img width="980" height="628" alt="image" src="https://github.com/user-attachments/assets/e00c0dc2-3c74-4ecb-a827-9bf28e82e3d4" />

### Methodology
Initial reconnaissance involved searching for "ACME Jet Solutions" to establish context. I discovered they are a company providing affordable private air travel solutions.

<img width="980" height="506" alt="image" src="https://github.com/user-attachments/assets/6ee85a42-aa98-4da2-bdde-179ba22f0233" />

Moving to the provided image, I checked the photo's properties to see if I could find any EXIF information. The metadata was mostly scrubbed, leaving only the raw GPS coordinates intact:

<img width="633" height="795" alt="image" src="https://github.com/user-attachments/assets/e2bf189e-7ac8-4ad1-a561-ff042b05f170" />

* Latitude: `26; 12; 14.76`
* Longitude: `28; 2; 50.28`

Since the hemispheric references (N/S, E/W) were missing, I brute-forced the four possible coordinate types: N-W, S-W, N-E, and S-E. I found out that only the S-E combination was in a metropolitan area (the others were in the desert or the ocean). Searching the coordinates on Google Maps revealed a town in South Africa.

<img width="980" height="488" alt="image" src="https://github.com/user-attachments/assets/a3de005b-da74-4fee-b0c4-8a8ac175cacc" />

After a few checks, the logo in the photo showed a security company from that area. This confirmed that we were in the correct spot, as the logo matched perfectly. 

<img width="419" height="541" alt="image" src="https://github.com/user-attachments/assets/96f7f85b-e5d7-412b-8f80-1dc3e0cfb5fb" />
<img width="980" height="505" alt="image" src="https://github.com/user-attachments/assets/791dd50b-bb19-4eaa-b1d5-89d8e52c6199" />

**Result:** The city associated with the coordinates is Johannesburg.
<img width="602" height="364" alt="image" src="https://github.com/user-attachments/assets/aab1f178-7ffc-486c-8c63-c036289046bb" />

> **Flag:** `THM{Johannesburg}`

---

### Uncovering the Spoofed Location
I did not want to stop just here; I wanted to find the exact location where the photo was taken, not just the city. 

**Visual Intelligence (IMINT) & Logic:**
1. From the original photo, there can be seen a sign where it says "The Rectory", so there must be a priest or minister’s house.
2. Also, in the image the road is inclined at 10-15 degrees, so the house must be in a hill area.
3. When searching for all the Rectories in Johannesburg, none were actually good because the architecture did not match. Most of the roads did not have trees at all, and all the buildings were too big for the description. Also, where I was able to actually find some trees, they were partly in front of the fence, not behind it.

Because of this, I thought that maybe the person who took the photo did some EXIF spoofing, hiding the exact location where the photo had been taken. Because of the security company (ADT) and the writing being in English, it meant that the photo was still taken in South Africa but in a totally different area.

The image reverse search on Yandex did not return anything useful.

<img width="980" height="490" alt="image" src="https://github.com/user-attachments/assets/b44ccae4-1e95-4550-9446-2fd6a45f1f4a" />


I tried it again on Google Images and found out that there are some Rectories in Simon’s Town that are pretty similar to the one in the image. Another aspect that I had seen in the image was a small watermark from Google Maps. This meant that the picture was actually a screenshot taken from Google Maps and the EXIF information was indeed spoofed.

<img width="386" height="128" alt="image" src="https://github.com/user-attachments/assets/71534857-4b0c-4797-a4eb-a4b75feaf9bf" />

The watermark said "2018 Google", which meant that even when searching Google Maps, I had to be careful to actually match the year with this one, because there could be some modifications to the appearance of the house. After searching all the Rectories in the area, I found one that matched the structure of the house in the image.

<img width="980" height="505" alt="image" src="https://github.com/user-attachments/assets/2dcc66f2-8289-4147-a142-2590a1db4936" />

If I changed the date of the Street View to 2017/2018, the photo matched perfectly.

<img width="980" height="505" alt="image" src="https://github.com/user-attachments/assets/80032a8d-5013-4a76-8a8c-75f0198f8dea" />


**True Location:** So the screenshot was taken of a version from 2018 of Google Street View containing the following exact address: 11 Runciman Dr, Simon's Town, Cape Town, 7995, South Africa.

---

## Task 2: Company Origins (Web Archiving)

**Objective:** Verify the true founding date of ACME Jet Solutions using only public information, despite claims that they were founded in 2025.
**Target:** `warc-acme.com/jef/`

### Methodology
Because in the provided link the "warc" stands for web archive, this meant that I should search the Internet Archive. 

<img width="980" height="507" alt="image" src="https://github.com/user-attachments/assets/8f71a677-b6ba-4f7c-be6b-5f12f45739c1" />

I searched for the provided identifier and located the raw `.warc` package. By inspecting the archive's metadata, I extracted the `Firstfiledate` timestamp.

**Result:** Here, the first file date is `20160210224602`.
> **Flag:** `THM{20160210224602}`

*(Note: Furthermore, following this snapshot on Wayback Machine opens Jef Poskanzer's web page, a fun easter egg left by the challenge creator).*

<img width="980" height="503" alt="image" src="https://github.com/user-attachments/assets/99564acb-ceb2-40c3-a924-e739c62fd920" />


---

## Task 3: International Expansion (Landmark Identification)

**Objective:** Identify the building to the right of an iconic landmark in a provided image, which played a big role in the fight for independence of a particular country.

<img width="980" height="1306" alt="image" src="https://github.com/user-attachments/assets/c8608193-afca-49c5-b9c7-f0de423c6886" />

### Methodology
Visual analysis of the poster on the left side of the image says something about Dublin, meaning that possibly the picture is from Dublin. 

<img width="192" height="752" alt="image" src="https://github.com/user-attachments/assets/215e9acb-cd4a-4b13-9105-57f068912bba" />


After a quick reverse image search on Yandex, I found the exact name of the place. The name of the "Stick" is "The Spire of Dublin". I searched for it in Google Maps to check if it matches the picture, and it does.

<img width="980" height="503" alt="image" src="https://github.com/user-attachments/assets/43b354a8-ccce-4267-a930-92cf7091b21c" />
<img width="980" height="503" alt="image" src="https://github.com/user-attachments/assets/17f3ebe6-76fc-45c6-a4b2-f9d4674c97a2" />


Now I just needed to match the orientation of the picture to the one on Google Maps. A particular thing from the picture I got that stood up is the shape of the roof on the left side of the picture. 

<img width="164" height="233" alt="image" src="https://github.com/user-attachments/assets/60e42578-e64e-48d3-ab56-e84f5dd3c26f" />


So I oriented the map in a way where it stands in the same place, ensuring the roof is on the same side. 

<img width="980" height="501" alt="image" src="https://github.com/user-attachments/assets/1d0b0820-c5f9-4511-ad4f-5893d8956fb3" />

The roof had the same orientation now: 

<img width="184" height="170" alt="image" src="https://github.com/user-attachments/assets/ea37a5b8-77a2-4c54-af07-095c712cb184" />


Now I had to look for the name of the building on the right side of the Spire. The building is the General Post Office. 

<img width="980" height="384" alt="image" src="https://github.com/user-attachments/assets/e8c40065-b182-4d0b-a450-d9b098864191" />

**Result:** The address of it is O'Connell Street Lower, North City, Dublin 1, D01 F5P2, Ireland.

<img width="333" height="322" alt="image" src="https://github.com/user-attachments/assets/6029d8f3-64d6-47d8-9bb7-c2f5e97e1753" />


> **Flag:** `THM{General Post Office}`

---

## Task 4: The Internal Document (Metadata Forensics)

**Objective:** Investigators believe that an internal document was accidentally leaked by one of the company's developers. The document may contain crucial information about the individual responsible for maintaining their systems.

### Methodology
The leaked document was a memo from "Mark" to "Robin". It outlined recent updates made to the internal tracking system, listing improvements like optimized database queries, improved user authentication logging, and minor bug fixes. The document explicitly stated: *"I will be releasing a video very soon, I implore everyone to watch it!"*.

<img width="980" height="1053" alt="image" src="https://github.com/user-attachments/assets/4b9296dd-3a11-4a87-bcc1-5432fe45f40e" />


The first thing I did was to look for the EXIF/metadata information of the file. 

<img width="980" height="740" alt="image" src="https://github.com/user-attachments/assets/beebf668-bbcd-4fbc-ba2b-8caaa4cc28f9" />


The metadata revealed a crucial piece of information. The `User-Defined` field for the file was `markwilliams7243`. Because the file stated he would be releasing a video soon, this meant that a user with the name `markwilliams7243` would post a video about it.

So, I searched the web for this user.

<img width="980" height="503" alt="image" src="https://github.com/user-attachments/assets/f9e4e7a3-473c-4a9c-bfe2-48b22681909c" />


I found his YouTube channel where he had a single post. The post read: *"I'll be uploading a video on the key changes made to our internal tracking system..."* and included the final flag at the bottom.

<img width="969" height="420" alt="image" src="https://github.com/user-attachments/assets/cc785396-8d62-4808-ad40-a7592e59b0e5" />

**Result:** The maintainer's handle was tracked to a YouTube community post.
> **Flag:** `THM{Y0u_f0und_7h3_fin4l_fl4g!}`
