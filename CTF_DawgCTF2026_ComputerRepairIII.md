# DawgCTF: Computer Repair III

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

**Information:**
My technician is working on this Dell device of some sort, and he's trying to figure out what it is so he can order a replacement component.
Can you identify what Dell product this is? The flag will be six characters, capital letters and numbers, such as DawgCTF{T4CH95}

<img width="803" height="602" alt="image" src="https://github.com/user-attachments/assets/2777b848-2bd4-4d20-b881-d40553d81aec" />

<img width="499" height="666" alt="image" src="https://github.com/user-attachments/assets/5a0d2c42-885f-46e5-b5f9-9723396bc266" />


## Solution

To begin, I searched for one of the provided images on Google Images to see if I could immediately find the original part and identify it. 

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/c7e8a294-fc4b-43c9-bb4d-0f95ef9b36fc" />


The search yielded several websites featuring pictures of a part similar to the one in the given image. I visited an Amazon link from the results, which led to a product page for a "Fan Dell Docking Station WD19TB". However, the part code on the site (DC28000NZF0) did not match the one in the picture; the original fan's code was DC28000NZD0.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/c9edf592-702a-45c6-bf96-e754d0162b25" />


For the next step, I used DuckDuckGo to search specifically for the fan's code: DC28000NZD0.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/40f66a15-7c8e-4e08-8b81-38b50f16274d" />

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/4333791d-b463-4a77-b25e-cd957892b0ec" />


Accessing an eBay listing from the results, I noticed that these fans with the DC28000NZD0 code were also meant for the Dell WD19. Following this, I performed a specific search for the "Dell Dock WD19" model.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/27e3cc0a-f5e2-4b1e-a45c-7655d50445d7" />

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/b71c1aa4-1944-4d18-bbb7-f7f3d577bdea" />

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/e1dc1eee-1159-4d06-856c-4a2db590bfc0" />


Analyzing the official Dell support page, I observed that the drivers and firmware utilities are shared between the WD19 and WD22TB4 models. However, the challenge required a 6-character identifier. Among the possible variants, WD19TB (the Thunderbolt variant of the series) is the only one that matches both the identified hardware specifications and the required flag format.

**The flag is:** `DawgCTF{WD19TB}`
