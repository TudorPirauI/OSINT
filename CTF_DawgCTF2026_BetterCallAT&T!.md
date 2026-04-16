# DawgCTF: Better Call AT&T!

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

**Information:**

I was watching my favorite show Better Call Saul recently and noticed something peculiar, can you figure out what the phone number for this parking garage is? I wanna recreate the shot... Your flag will be the number for the garage without dashes, e.g. DawgCTF{2015552124}.

<img width="975" height="540" alt="image" src="https://github.com/user-attachments/assets/2461ee7c-07d0-49f2-bd88-12bd39021e2d" />


---

## Solution

I began by running the picture through Google's reverse image search to identify the parking garage. The results quickly showed that the image was taken from an episode of Better Call Saul (Season 1, Episode 9).

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/9efdc64c-ebed-46b0-9a26-b4f7ebb4e87c" />


<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/41533fec-5205-4068-839d-e73e000d201b" />




After finding the episode in which the parking garage scene was filmed, I searched for the filming locations of this episode. Following the search, I discovered a webpage called "Breaking Bad Locations" and accessed it.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/09c28f5c-31fc-4cc3-9208-985c516f4917" />

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/ef817611-f095-475c-8962-e5d797a65c7d" />


After entering the webpage, I scrolled down until I found a section with a picture that appeared to be taken in a parking garage; the description matched because it described a meeting in a parking garage.

<img width="975" height="140" alt="image" src="https://github.com/user-attachments/assets/a72bcf2b-b3f5-4278-b8d3-f52ba1105ac6" />

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/e6c2bdaf-c755-40ff-b042-3f5660cba46b" />


Therefore, after clicking on the parking garage section, I discovered that the real-life location was `Tijeras Ave NW, Albuquerque`.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/8d749995-844b-4137-be3c-74e2e27e6add" />


Checking Google Maps, I noticed that this location was incorrect, as it did not correspond with the elements in the original image. Next, I switched to another browser, DuckDuckGo, and found a site that similarly described the locations where the show was filmed.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/256a970f-ed8a-40eb-b349-0b6c1a051871" />


Here, I found that the name of the parking garage was `Albuquerque Convention Center Parking`.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/5d7aebf6-8025-4536-a233-d2ea395d9441" />


As a final step, I searched for the parking garage and found the requested phone number.

**The flag is:** `DawgCTF{5057684575}`
