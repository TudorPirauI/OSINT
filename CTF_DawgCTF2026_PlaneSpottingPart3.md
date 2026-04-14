# DawgCTF: Plane Spotting Part 3

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

### Information:
You managed to snap this photo just after takeoff. (The password is the flag from Plane Spotting Pt. 2.) The view looked familiar... but you didn’t think much of it at the time. 
Now you’re curious, what aircraft were you actually on? Find the registration number of this aircraft. 

<img width="980" height="551" alt="image" src="https://github.com/user-attachments/assets/139503ec-bb0f-4397-9d4c-69be09c05047" />

---

### Solution: 
First, after I downloaded the folder, I extracted the image using the password from Plane Spotting Part 2 (`DawgCTF{NAS}`). 

Next, I extracted the EXIF information for the downloaded image: 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/49c40dcd-c39b-42d2-9959-3ad35301e7ad" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/6085e931-a182-4008-a207-d59b2e258fb4" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/b690bd32-7436-4913-b5d0-6830d3768b12" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/c912eccd-a26b-4e46-a9bc-1236e9a2bab3" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/1129bcea-ae60-4667-8915-0276317723e5" />


The highlighted `MCCData` clearly states that the image was taken in America. 
This reduces the search area quite a lot. 

<img width="980" height="207" alt="image" src="https://github.com/user-attachments/assets/eb495383-862f-4e3b-8bc3-dc361af42afb" />

The offset of UTC -7 corresponds to Pacific Daylight Time (PDT). 
The highlighted timestamp shows that the picture is pretty old, from 18.07.2023. 
The picture was taken on the West Coast: Washington, Oregon, Nevada, or California. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/f79664ec-7878-4a5b-9581-f92abc8ae755" />

Searching for the image with Google Images suggested that it might actually be Seattle. 
I searched for ADS-B Exchange to look up the flight history (I did not use Flightradar24 this time because it requires a premium account for flight history older than a week). 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/087829e4-866a-4b5c-bce3-2e08bda71ccb" />

Zooming in on the coast side of the image and taking a closer look at the river that flows into the ocean from the land (around the middle of the picture), I compared it to the coastline seen on ADS-B Exchange, and it had the exact same shape. 
This exact shape confirms that the place I am looking for is Seattle for sure. 

<img width="922" height="1183" alt="image" src="https://github.com/user-attachments/assets/d35c9df1-9099-4e52-ab9c-0613306fd4d7" />
<img width="348" height="584" alt="image" src="https://github.com/user-attachments/assets/ad14f944-5e10-4be6-8b04-83b47d29ce53" />

After entering history mode and filling in the known information: 
* Time: 06:54:49.512 with a -07:00 offset, on the date 18.07.2023. 
* I converted the hour to universal time (UTC), which means: 13:54:49. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/0b5c12e4-6c72-4a0c-81b5-cc1d55803098" />

Judging by the position of the plane relative to the land, it must be one traveling from east to west (I compared the coastline from the two pictures above—the photo was taken from the right side of the plane). 

<img width="1024" height="550" alt="image" src="https://github.com/user-attachments/assets/4f92710f-1a40-403e-b78a-79eea770b1f5" />

Looking through the options available on this route, the plane ASA195 was the only possible option at that exact time. 
Also, the altitude of around 7000ft confirms that the plane had just departed. 

This means that the flag is: 
**DawgCTF{N609AS}**
