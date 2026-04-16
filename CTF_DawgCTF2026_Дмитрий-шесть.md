# DawgCTF: Дмитрий-шесть

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

**Information:**

My friend from Ukraine sent me this weird picture; he says that it's the key to a secret treasure room underground. Do you know where this picture was taken? The flag will be the official name of it, and should be 6 letters total, all capital letters.

<img width="786" height="938" alt="image" src="https://github.com/user-attachments/assets/33461ec9-962d-4210-8cd4-b253ccfa179c" />

---

## Solution

To identify the exact location in the photos, the first step was to perform a reverse image search. Using Yandex Images yielded several exact matches of the original photo.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/cec843a9-edae-4207-b2a5-d0d080cc58ca" />


Because there were multiple sites with the exact same photo, I selected the first one.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/77317321-15be-4d4a-9bf2-38ba68cee12a" />

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/8aa7def8-85d0-4326-805e-fc4bab6f47d7" />

The website was written in a language I didn't recognize, though it looked like it could be Russian or Ukrainian. To confirm, I ran a random paragraph through Google Translate, testing for Russian first.

<img width="975" height="518" alt="image" src="https://github.com/user-attachments/assets/88d3da36-f847-4403-bc70-f23da259b28e" />

From the translated paragraph, I managed to find that the article containing the original photo is about a metro line called 'Metro-2' located in Moscow.

**The flag was:** `METRO2`
