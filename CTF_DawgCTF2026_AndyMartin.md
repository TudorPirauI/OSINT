# DawgCTF: Andy Martin

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

### Information:
You may think you know an Andy Martin, but do you really? This Andy Martin is a Londoner who loves to travel. He's been to places like Mauritius and Portugal. There is a somewhat unorthodox trail of his travels. But the real question is: where did he go out to eat in his hometown on Thursday, July 12, 2018?

---

### Solution:

At first, I searched the internet to see how many people named Andy Martin live in London. It turns out there are quite a few (architects, filmmakers, IT specialists, etc.).

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/a7d60b1f-5a55-4b69-afd9-0a17d5cd693f" />

Given his love for travel, I searched for his name on travel and review platforms like Yelp, TripAdvisor, Google Maps, and Strava. Google Maps was the only one that returned a relevant account:

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/b1ae5ecc-acfb-493f-ba02-5bb303031174" />

Upon checking his Google Maps profile, I discovered he is actually a Top 100 Local Guide. Looking at his contributions, I saw he had written over 600 reviews.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/f9e8b420-7cf5-411b-b685-09e65ce5d66a" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/d14f624e-54f2-44da-a195-024226634932" />

To confirm this was the correct Andy Martin and not just a coincidence, I checked if he had any reviews in Portugal and Mauritius. As shown below, he indeed had multiple reviews in both locations:

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/3510c222-712e-452e-85b5-4a869a43b7f4" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/12bc3ad5-1171-44c0-b71b-494d3137f6c9" />

Since the target date was July 12, 2018, I narrowed my search to reviews made roughly 7 years ago (as 8 full years had not yet passed at the time of the CTF). 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/3dbd4fcd-d4d0-4b3a-a157-1de804a64fca" />

However, Google Maps only displays relative dates like "7 years ago," which spans an entire year. Furthermore, almost all of his reviews from that period were located in London.

<img width="983" height="528" alt="image" src="https://github.com/user-attachments/assets/eb6cfe71-9c60-4a4d-8fb9-e048590a2b4a" />

To find the exact dates, I opened the browser's Network tab to inspect the raw data requests made by Google Maps. This allowed me to look for the exact Unix timestamps of each review. Using an epoch converter, I determined that the timestamp for July 2018 starts with `1531`. For easier searching, I copied the raw response into a Word document and searched for `1531`.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/a9d9e585-bd13-4f0f-ad9f-94835cf32ff4" />

I found the timestamp `1531419749483000`. Converting this from microseconds confirmed it was the exact date I was looking for: July 12, 2018.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/40b6ccb1-27c3-420c-9ffd-f8177e7a8833" />
<img width="884" height="181" alt="image" src="https://github.com/user-attachments/assets/1a3dfefe-69a4-4432-a835-6fc688f8e2b1" />

Looking back at the raw data, the restaurant associated with this timestamp was labeled `"fish_and_chips_restaurant"`.

<img width="980" height="299" alt="image" src="https://github.com/user-attachments/assets/864bc37e-e6c7-4198-9c09-e5ead0a349f3" />

To confirm, I navigated back to the map and found his specific review for Poppies Fish & Chips.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/4bb4a928-8798-46cb-8bab-d851468399bd" />

This gave me the final flag:
**Poppies Fish & Chips**
