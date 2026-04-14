# DawgCTF: Computer Repair 1

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

### Information:
I recently opened a computer repair shop, and a customer left this laptop with my warehouse staff.
Could you assist me in figuring out the RAM size and speed this laptop originally had, as well as the model and capacity of the hard drive?
The flag format is as follows (e.g., if it had 32GB 3200Mhz RAM and a 1TB 980PRO hard drive): DawgCTF{32GB_3200MHZ_1TB_980PRO}

<img width="980" height="655" alt="image" src="https://github.com/user-attachments/assets/a1f6e00a-91a0-4ec0-b530-9bce5ea0a2df" />

---

### Solution:
Initially, I looked at the information printed on the bottom of the laptop.
Along with the model name, I found a Service Tag and an Express Service Code.

<img width="980" height="450" alt="image" src="https://github.com/user-attachments/assets/a7d3d8ce-3d37-4126-bd28-5428c19773c8" />

I decided that searching the internet for the laptop's name would be a solid starting point.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/aac255b6-4430-4183-a664-d23b6599f49d" />

The second search result led directly to Dell's official support page for this exact model.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/721baf68-9125-4fa5-8fac-ac7a777d4007" />

Since the Service Tag allows for precise product identification, I ran a search for the code FZGXPV2.

<img width="980" height="115" alt="image" src="https://github.com/user-attachments/assets/f6b96a3d-58cc-486c-839b-e850c28226f8" />

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/8f17ab3f-1796-4c15-8d9e-1b74f601a4cd" />

On the resulting page, there was a section detailing the device's original specifications.
In that section, I located the two hardware components I needed:

* R4GT0 – This was the RAM, listed as 16GB at a speed of 2666MHz or 2667MHz (depending on whether you look at the title or the detailed description).

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/15157659-bd6e-4eab-8027-6c8d9131d435" />

* 182F1 – This was the SSD, listed as 256GB with the model name 35PK2.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/d09234c6-5ac9-4636-a29f-da44b6ca1a0d" />

Given the two possible RAM speeds, I formulated and tested two different flags:
* DawgCTF{16GB_2667MHZ_256GB_35PK2}
* DawgCTF{16GB_2666MHZ_256GB_35PK2}

The successful flag was:
**DawgCTF{16GB_2666MHZ_256GB_35PK2}**
