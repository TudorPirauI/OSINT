# TryHackMe: OhSINT - OSINT Write-up

## Task 1: Avatar Identification

**Objective:** What is this user's avatar of?

<img width="980" height="551" alt="image" src="https://github.com/user-attachments/assets/bc8ea2f9-10a3-429a-a506-d9d7933d5401" />

### Methodology
I viewed the EXIF properties of the downloaded image to check for relevant information. 

<img width="980" height="502" alt="image" src="https://github.com/user-attachments/assets/03a4407d-d1a4-40ac-a700-0332d74fd5c6" />

<img width="980" height="505" alt="image" src="https://github.com/user-attachments/assets/896f0f9f-5a63-4ca1-9b1a-6433b9498a16" />


I found that the name of the person that owns the copyright is `OWoodflint`, so I searched for his name online to see what other accounts are created under this name:

<img width="980" height="499" alt="image" src="https://github.com/user-attachments/assets/f7f45073-59a0-461e-9bc2-4267142821a6" />


The first link was to his Twitter (X) account. By checking his profile, his avatar is clearly visible.

<img width="942" height="1105" alt="image" src="https://github.com/user-attachments/assets/fa978c50-71b4-4274-8890-a60bd80cf583" />


**Result:** The avatar is a picture of a cat.

> **Answer:** `Cat`

---

## Task 2: User Location

**Objective:** What city is this person in?

### Methodology
After searching for "OWoodflint", the second search result is his GitHub account.

<img width="980" height="254" alt="image" src="https://github.com/user-attachments/assets/dadc9186-e033-4526-9303-bdb84756ca15" />


Looking into his repositories, in his `README.md` file it states clearly that he is from London.

<img width="980" height="458" alt="image" src="https://github.com/user-attachments/assets/dc522976-acf3-4440-b857-ec21df1f5258" />


**Result:** The user mentions his city directly in his project description.

> **Answer:** `London`

---

## Task 3: Connected Network

**Objective:** What is the SSID of the WAP he connected to?

### Methodology
When I came back to his Twitter account, I saw that he shared in a post his BSSID.

<img width="927" height="211" alt="image" src="https://github.com/user-attachments/assets/7f8fc8e6-eb19-4616-8e76-88102f0ae9b2" />


The BSSID provided was `B4:5D:50:AA:86:41`. I searched for that exact BSSID on WiGLE to find its physical location and network name.

<img width="980" height="529" alt="image" src="https://github.com/user-attachments/assets/d98bb480-9927-48de-a92e-85d50a853d1f" />


It shows the exact SSID of the WAP he is connected to on the map.

**Result:** The BSSID belongs to a network named UnileverWiFi.

> **Answer:** `UnileverWiFi`

---

## Task 4: Contact Information

**Objective:** What is his personal email address and what site did you find it on?

### Methodology
To see his personal e-mail, all I had to do was to come back to his GitHub account in the same `README.md` where it wrote that he is from London. 

<img width="980" height="415" alt="image" src="https://github.com/user-attachments/assets/a73bd495-b237-496a-8251-0f5b277deaac" />


**Result:** His email is provided clearly as a contact method for his project.

> **Answer 1 (Email):** `OWoodflint@gmail.com`
> **Answer 2 (Site):** `Github`

---

## Task 5: Current Whereabouts

**Objective:** Where has he gone on holiday?

### Methodology
If I follow the link from his GitHub account about a new project that he is starting soon, it will redirect me to a new WordPress page:

<img width="980" height="502" alt="image" src="https://github.com/user-attachments/assets/7e7ab470-b16e-47e2-97b6-930cfabe46ef" />


On this page, he clearly states that he is in New York right now.

**Result:** The user updated his personal blog with his holiday location.

> **Answer:** `New York`

---

## Task 6: The Hidden Password

**Objective:** What is the person's password?

### Methodology
On the same WordPress page, when inspecting the page elements via Developer Tools, it can be seen that the password is written in white, camouflaging perfectly with the background.

<img width="980" height="503" alt="image" src="https://github.com/user-attachments/assets/a28f0388-e37f-4537-b285-fc77cc7b07a1" />


By simply selecting the text in that area, the camouflage is bypassed, and the password is revealed:

<img width="980" height="319" alt="image" src="https://github.com/user-attachments/assets/15c86307-5bba-4210-a84d-192a989131d1" />


**Result:** The password was hidden using white text on a white background.

> **Answer:** `pennYDr0pper.!`
