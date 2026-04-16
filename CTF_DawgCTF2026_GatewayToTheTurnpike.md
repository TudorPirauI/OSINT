# DawgCTF: Gateway to the Turnpike

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

**Information:**

They say all roads lead to Rome, but in this part of the mid-Atlantic, all roads lead to a very confusing set of gas stations. I snapped this photo on a road trip a while back. Do you think you could tell me the ZIP code of the place this was taken?

![image](https://github.com/user-attachments/assets/ab980f4f-3d8a-4f69-9b55-bfefe2412e7d)
 
---

## Solution

To identify the road intersection, the first step was to perform a reverse image search. Using Yandex Images yielded several exact matches of the distinct elements seen in the original photo.

![image](https://github.com/user-attachments/assets/1a9c293a-2ccd-461f-9ae2-5a6f675d18a9)

Because there were multiple photos of this specific location, I selected the most detailed one. Upon opening the image source, the first detail that caught my eye was the page link containing the text `Pennsylvania-2023`.

![image](https://github.com/user-attachments/assets/f289cd7e-0ca6-4fcb-a0e8-748246792dbc)

Clicking the link redirected me to a photo posted by a user on Flickr. The image description clearly specified that the location was Breezewood, Pennsylvania, and noted that this famous turnpike is widely known `as a tourist trap`.

![image](https://github.com/user-attachments/assets/1c53bd12-74fb-47ad-ac3d-820753bf044e)

Finally, I opened Google Maps and searched for the McDonald's in Breezewood. By comparing the map view to the original photo, I verified it was the exact same intersection. Google Maps then provided the ZIP code for that specific area.

**The flag was:** `DawgCTF{15533}`
