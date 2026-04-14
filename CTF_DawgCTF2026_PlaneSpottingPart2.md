# DawgCTF: Plane Spotting Part 2

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

### Information:
You saw this plane approaching; what airport was it coming from? 
Use the flag from Plane Spotting Pt. 1 to unlock the image. 
Flag format: DawgCTF{IATA}

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/56819644-8bc0-41ce-a58a-24fd7621c69a" />

---

### Solution:
First, I downloaded the file and entered the flag from Plane Spotting Part 1 to unlock the image. 

<img width="980" height="552" alt="image" src="https://github.com/user-attachments/assets/0b1a2544-994e-4151-b2a1-fbffe6d63d71" />

After extracting the image’s EXIF information, I got the following GPS coordinates. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/6cd12242-05e4-47f0-96d7-caa260be9d52" />

Once I had the coordinates, I entered them into Google Maps to check if they were close to an airport, because the plane in the image seemed close to the ground. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/ed8667f5-8015-4a6f-8b98-1e24584210f6" />

The location was very close to Baltimore/Washington International Thurgood Marshall Airport (BWI). 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/a3ba2ff8-b04f-42cb-84fc-a90a4631c7b1" />

Looking back at the EXIF information I extracted, I realized I had both the exact location and the time this picture was taken. 
This meant that in order to identify the exact plane in the air at that moment, I just needed to look up the flight history for that specific timeframe. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/d1165672-73a3-481e-b407-c9c1c0797042" />

Taking a closer look at the plane, I noticed three very important details: 
* The plane was from the same provider as in Plane Spotting Part 1 (Southwest). 
* The landing gear was deployed, meaning the plane was actively landing. 
* The flaps and brakes on the wings were fully engaged. 

<img width="980" height="567" alt="image" src="https://github.com/user-attachments/assets/6aec192e-bd6d-40e8-b8bd-8fa034a23f00" />

This meant I had all the information I needed: the location, the time, the flight direction, and the airline provider. 
I searched for Flightradar24 to access historical flight data. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/42bf3c26-372a-47e3-93c3-d6c6a9286642" />

After accessing the site, I inputted the specific date and location I was looking for into the app’s history. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/887774e2-fa73-4900-89f3-5a942b45e847" />

By filtering with this information, I narrowed it down to two possible planes, with a landing time difference of just 5 minutes (7:40 PM vs. 7:45 PM). 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/f90707c6-b2b2-4d7f-a814-02ce7654d4d4" />

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/cc129a2e-e819-4b82-94d9-a0d571b5a4ae" />

Since the flight descriptions displayed the IATA codes for both of their departure airports, I tried both options: 
* DawgCTF{ORF} 
* DawgCTF{NAS} 

The correct flag was: **DawgCTF{NAS}** ```
