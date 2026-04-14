# DawgCTF: The Temple Of Doom Write-up

**Authors:** Pirău Tudor-Ioan and Croitoru Carina

## Challenge Description

**Information:**
> I used to work at this crazy-looking building. I've attached a picture of it, can you guess where it is?
> 
> If you can, the flag is the nickname the building has. 
> For instance, if the nickname was "The Dragon Building", the flag would be `DawgCTF{The_Dragon_Building}`.

<img width="980" height="543" alt="image" src="https://github.com/user-attachments/assets/36ac0b8f-f7cb-4b32-908f-fad53df2ea42" />

---

## Solution

**Step 1: Reverse Image Search** The first step to identifying the building was to perform a reverse image search. Using Yandex Images returned several exact matches of the structure.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/fc36d9d6-0832-45d9-ad60-c9e2eebf2355" />

**Step 2: Identifying the Location** Since there were multiple search results featuring the same architecture, I selected the Wikipedia entry to get more context. The article revealed that the structure is located in **Laguna Niguel**.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/8bfacdb2-3931-4601-8a78-f7a459eb5e6f" />

**Step 3: Finding the Nickname** The challenge specifically asked for the building's *nickname*, not its official name. Using the location discovered in the previous step, I performed a regular web search for "Laguna Niguel temple" to find sites or news articles that might mention what locals call it.

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/a1a06762-7994-467b-83ef-149760e60da9" />

**Step 4: Discovering the Flag** The search results brought up a news article from the Orange County Register titled: *"Feds get no interest in auction of iconic Ziggurat building in Laguna Niguel"*. 

<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/912a3f36-41ac-4c51-8d7e-805c722eed72" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/66246786-79c8-44f0-8fd5-aa7f2f6745ca" />


Upon inspecting the article and its image captions, the nickname was explicitly highlighted:
> *"The Chet Holifield Federal Building, also known as the **Ziggurat building**..."*

**Step 5: Final Flag Construction** Using the discovered nickname and following the challenge's required format, the flag was:

### **Flag:**
`DawgCTF{The_Ziggurat_Building}`
