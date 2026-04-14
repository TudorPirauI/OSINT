# DawgCTF: Computer Repair 2

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

### Information:
I received another photo from the warehouse, and although there's not much to go on, could you determine the screen size of this laptop?
The required flag format is DawgCTF{18.9IN}.

<img width="980" height="735" alt="image" src="https://github.com/user-attachments/assets/a1e305f2-ae2c-4e3a-ae82-ef5e9a1447ee" />

---

### Solution:
Initially, I looked for unique features in the photo that could help distinguish this laptop from others.
I noticed the keyboard features a round blue button, as shown in the lower section of the image.

<img width="717" height="283" alt="image" src="https://github.com/user-attachments/assets/2bfcfbdc-4e53-4974-ba12-e0d62abf74e3" />

Additionally, the power button has a distinct line across it.

<img width="481" height="361" alt="image" src="https://github.com/user-attachments/assets/118dcbf8-b7ba-4678-8aed-e8a38006ef88" />

Once I knew which specific details to look for, I performed a reverse image search using Yandex.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/b52e2824-4a12-4e1c-8166-a08ddba3a7a4" />

The very first visually similar result appeared to be the exact same model, as it featured both the blue keyboard button and the distinct power button.

<img width="969" height="677" alt="image" src="https://github.com/user-attachments/assets/ec11d310-97ec-4c72-b47f-f452a39927ff" />

Clicking the link associated with that image redirected me to an eBay listing.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/6eaec407-5ebc-42d6-b91a-da828595a194" />

I grabbed the laptop model name from the eBay page and ran a standard web search to find an official retail listing.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/b6541b1c-d118-40d0-81be-9ba177b9211e" />

I found the exact model listed on eMAG, sold directly by a verified seller rather than an independent third party.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/58f34c9f-95ea-4bc0-8cfc-a5bd2244c43f" />

The screen size was clearly stated right in the product title: 15.6 Inches.

Therefore, the final flag is: 
**DawgCTF{15.6IN}**
