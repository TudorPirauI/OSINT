# DawgCTF: owo?

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

**Information:**
Took this photo on a road trip a while back and want to go back to this Pizza Hut, but I forgot where it was.
Do you think you could find me the ZIP code of the town this was in?

<img width="586" height="1042" alt="image" src="https://github.com/user-attachments/assets/8b402b03-4659-4b83-88d9-c4e4c386a86b" />


## Solution

As a first step, I decided to perform a reverse image search using Yandex Images. The initial search didn't return any similar photos or lead to further clues. Additionally, other elements in the photo, such as the banner on the pole or the blue rooster in the background, were not found either.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/af039a88-72b4-45c3-8e77-e428d809d29d" />

After that, I thought the quote on the sign under the Pizza Hut logo might be relevant: `WINGS ARE BACK GET SOME TATSY CRIꙄPY WINGS OꙍO`. Therefore, I searched using Google Dorking filters for `pizza hut "OꙍO" meme`, but no results showed this exact picture or provided helpful information.

<img width="975" height="461" alt="image" src="https://github.com/user-attachments/assets/02a2d11c-84c1-41f7-a1c3-fc69e72cb547" />

Next, I focused on other visual elements in the image and moved on to the banner on the pole. Because it wasn't very clear in the original photo, I used the website `pokecut.com` to upscale the image. After adjusting the photo, I noticed the face was clearer, but the text was still indecipherable.

<img width="190" height="374" alt="image" src="https://github.com/user-attachments/assets/c747bdaa-ed07-44ba-b954-0891ba6bfb4f" />

<img width="975" height="497" alt="image" src="https://github.com/user-attachments/assets/c3568273-30b6-4279-a682-bc3789dc927a" />


I also did a reverse image search on Yandex Images for this banner and discovered that these types of banners are made to commemorate American veterans. However, this search didn't help me find the exact banner or the name of the town either.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/eb39a41e-5937-4a75-a2b1-c58a44bc7ce8" />

I then decided to inspect the blue rooster from the original picture. After cropping specifically on this element, I noticed it appeared to have two initials written on it: `W` and `V`. Consequently, I searched for the initials `WV`.

<img width="727" height="1170" alt="image" src="https://github.com/user-attachments/assets/e7caa5d5-2e6f-477c-bff5-89ae45c42c3e" />

The search results indicated that these are the initials for the US state of West Virginia. As a result, I searched Google Maps for Pizza Hut locations in West Virginia.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/b33c561b-08ad-4a7d-99bf-a82624e17a02" />

I started checking each location individually, using Street View to clearly see the area and surrounding elements. After checking several locations, I reached the town of Petersburg and found the exact spot from the original photo. 

<img width="975" height="465" alt="image" src="https://github.com/user-attachments/assets/5e5bd832-8e7f-49db-a8dd-979a603d9540" />

<img width="975" height="464" alt="image" src="https://github.com/user-attachments/assets/88159004-532c-4ada-902a-f4c017255057" />


I then looked up the ZIP code, which was 26847.

<img width="975" height="463" alt="image" src="https://github.com/user-attachments/assets/b6ecaa2c-2fd6-4bbc-85f6-90be441ba2fc" />

<img width="975" height="461" alt="image" src="https://github.com/user-attachments/assets/708a9e43-bd68-4adc-a589-3faa658af51f" />

<img width="975" height="463" alt="image" src="https://github.com/user-attachments/assets/76306981-1297-4cda-a5f2-4894c87855f3" />

**The correct flag is:** `26847`
