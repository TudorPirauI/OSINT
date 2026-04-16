# DawgCTF: Locksmith 

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description 

**Information:**

I saw this weird lock at the escape room I work at. Can you figure out what series it is, and how tall the lock body is? 
The flag will be in the following format: `DawgCTF{BEST500_95MM}` 

<img width="405" height="540" alt="image" src="https://github.com/user-attachments/assets/809ca22e-b551-46fb-a8c0-d8f4a4f4d933" />


---

## Solution

I began by running the picture through Google's reverse image search to identify the lock from the original photo. After searching, I found several websites selling this lock. So, I visited the first webpage, `Door Controls Direct`.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/9a00c365-09bf-4038-afaf-2692a629baa6" />

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/b53b7aac-1b7e-4512-93fb-4f30a0e80b9b" />


Afterward, I carefully checked if the product page displayed technical specifications from which I could find its height. 


<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/53214954-ae54-4760-9a51-cafd6903063e" />

At the bottom of the webpage, I found a PDF with the lock's technical specifications. I opened that PDF, and on the last page, I discovered that the height of this specific lock is `95mm`. 

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/7874ca57-c83b-4c25-bb22-13dc6c52917c" />

However, from my Google searches, I noticed that this lock is referred to as `Simplex` on multiple websites, and its base series is `900`. 

<img width="439" height="914" alt="image" src="https://github.com/user-attachments/assets/10b4e3ab-27ad-4158-af19-7a3f3ed96219" />

Therefore, I initially submitted the flag: `DawgCTF{900_95MM}`. Since this was incorrect, I added `SIMPLEX` in front of it. 

**In conclusion, the flag is:** `DawgCTF{SIMPLEX900_95MM}` 
