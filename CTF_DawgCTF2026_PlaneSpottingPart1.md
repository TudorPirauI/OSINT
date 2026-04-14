# DawgCTF: Plane Spotting Part 1

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

### Information:
This photo was transmitted from a cyberdawg documenting their travel right before they went missing.
We didn't have a GPS tracker and it's imperative you identify the location the photo was taken.
Flag Format: DawgCTF{IATA}Make sure you have the proper format.

<img width="980" height="552" alt="image" src="https://github.com/user-attachments/assets/131475d1-a7f4-4cf1-8fed-e67f376787f1" />

---

### Solution:
First I reversed searched the whole image on Yandex and then only snippets of it (such as the Car besides the plane, the plane or the background) but nothing relevant showed up.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/c3f3ab97-472d-4f8f-b932-bedda244141c" />

Because the only thing that showed up were planes from the same provider Southwest, but on different airports, the information was irrelevant to me.

<img width="980" height="513" alt="image" src="https://github.com/user-attachments/assets/964b7646-6ab4-4530-9d41-526b126517a4" />

After that, I searched for the exact flight support provider seen in the image “US Airports”.
By entering the first link that showed up, I ended on the following page:

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/2cc8399c-55d1-478f-bd6d-9a2d960eeaa5" />

In the page description it was stated that the company was located at Frederick Douglass-Greater Rochester International Airport.

<img width="980" height="126" alt="image" src="https://github.com/user-attachments/assets/4baf2280-b719-4808-bcef-505992b834b5" />

I searched on the internet for the exact iata code of the airport:

<img width="1067" height="573" alt="image" src="https://github.com/user-attachments/assets/e3124a4a-7e91-435f-a1da-6d1d85f5a737" />

The IATA code of the airport is “ROC”.
This means that the flag is: DawgCTF{ROC}
