# TryHackMe: Searchlight - Write-up

---

**Information:**
<img width="980" height="653" alt="image" src="https://github.com/user-attachments/assets/afa9e85e-5e48-4284-b721-b303b3c90b5c" />

* **Question:**
What is the name of the street where this image was taken?
* **Solution:**
The answer is pretty straight forward: the name of the street is Carnaby Street.
* **Flag:** `
sl{carnaby street}`

---

**Information:** 
<img width="980" height="784" alt="image" src="https://github.com/user-attachments/assets/e708ec50-8960-4b6e-b2e1-22179033010b" />

* **Question:**
Which city is the tube station located in?
* **Solution:**
<img width="980" height="178" alt="image" src="https://github.com/user-attachments/assets/7b855166-0de8-4d04-9820-185a3fff7685" />

  By watching this portion of the image, it can be seen that the first word of the name of the metro station ends with "ly" and the second word is "circus". So, after a search of this syntax on Google, there is a metro station that matches: Piccadilly Circus station.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/4940acc7-81ac-481f-84ad-d55f4550ee89" />

  This station is situated in London.
* **Flag:**
`sl{London}`

* **Question:**
Which tube station do these stairs lead to?
* **Solution:**
I just found that the name of the station is Piccadilly Circus.
* **Flag:**
`sl{Piccadilly Circus}`

* **Question:**
Which year did this station open?
* **Solution:**
After entering the Wikipedia page of this tube station, the date in which the station opened is written in the first paragraph of the “History” section: 10 March 1906.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/9f2ad44a-a7be-48fc-803f-06efbd0a3b0c" />

* **Flag:**
`sl{1906}`

* **Question:**
How many platforms are there in this station?
* **Solution:**
On the same Wikipedia page, when searching with ctrl+F for “Platforms”, it states that the current number of platforms is 4.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/96e9d22e-2555-4222-98d3-5dca55008628" />

* **Flag:**
`sl{4}`

---

**Information:**
<img width="1039" height="580" alt="image" src="https://github.com/user-attachments/assets/eb66c949-cabd-4311-adc0-4ab43d1c3d09" />


* **Question:**
Which building is this photo taken in?
* **Solution:**
<img width="980" height="356" alt="image" src="https://github.com/user-attachments/assets/63078f3c-a9af-4ec4-bd0e-5f154f82016f" />

  After searching for the YVR.CA link shown on this billboard, it redirected me to the Vancouver International Airport site.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/cb85ce92-c3de-461f-b718-26aa2dcdc3bd" />

* **Flag:**
`sl{Vancouver International Airport}`

* **Question:**
Which country is this building located in?
* **Solution:**
Vancouver is a city from Canada.
* **Flag:**
`sl{Canada}`

* **Question:**
Which city is this building located in?
* **Solution:**
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/84cc8f52-ba18-479e-b399-b1511ce6562b" />

  By just entering the “Contact Us” page, the full address can be seen there:
  > Street/Courier Address: 3211 Grant McConachie Way Link Building, L5 Richmond, BC Canada V7B 0A4
  
  This means that the city is Richmond. The same result could be obtained by just searching for it on Google Maps.
* **Flag:**
`sl{Richmond}`

---

**Information:** 
The picture is from Scotland. 
<img width="980" height="1302" alt="image" src="https://github.com/user-attachments/assets/4ad61d31-346b-43ba-9422-60b8ba0d1f53" />


* **Question:**
Which city is this coffee shop located in?
* **Solution:**
First I tried to see if I could find something with an EXIF Tool, but nothing relevant was shown. The info said that it was in Scotland, so I searched on Google Maps for Scotland and then I searched for nearby Edinburgh Woollen Mill.
<img width="980" height="504" alt="image" src="https://github.com/user-attachments/assets/a4e5a222-16c9-4a1b-b2ae-c7d8fb78fe98" />

  Then I entered all of them from north to south in street view mode until I found this one in Blairgowrie.
<img width="980" height="505" alt="image" src="https://github.com/user-attachments/assets/50801399-5ef7-4a96-ab8b-b2a3a16c9b9d" />

* **Flag:**
`sl{Blairgowrie}`

* **Question:**
Which street is this coffee shop located in?
* **Solution:**
Judging by the position of the coffee shop relatively to the store, the street should be Allan Street.
<img width="980" height="907" alt="image" src="https://github.com/user-attachments/assets/5be6d3cb-a1bd-4ea1-bfd6-14d402b225ef" />

* **Flag:**
`sl{Allan Street}`

* **Question:**
What is their phone number?
* **Solution:**
The coffee shop from across the street from the Edinburgh Woollen Mill is The Wee Coffee Shop.
<img width="980" height="504" alt="image" src="https://github.com/user-attachments/assets/52e7ddc0-caab-4fa1-a670-e203575dad7d" />

  Searching for the store online it can be found on multiple review sites, such as Tripadvisor.
<img width="980" height="500" alt="image" src="https://github.com/user-attachments/assets/24f04311-71b7-4aa6-8758-bc4d439ae80d" />

  On Tripadvisor the contact number written is +447878 839128.
* **Flag:**
`sl{+447878 839128}`

* **Question:**
What is their email address?
* **Solution:**
To the right of the phone number, the email is listed: theweecoffeeshop@aol.com.
* **Flag:**
`sl{theweecoffeeshop@aol.com}`

* **Question:**
What is the surname of the owners?
* **Solution:**
Searching the internet for: `"the wee coffee shop" blairgowrie "owned"` it returned a result on Blairgowrie Cafes and Restaurants. Where it was stated that the place is owned by Debbie and David Cochrane.
* **Flag:**
`sl{Cochrane}`

---

**Information:**
<img width="980" height="1308" alt="image" src="https://github.com/user-attachments/assets/a0ca18a4-09df-4e93-9708-61bc611b8e2a" />


* **Question:**
Which restaurant was this picture taken at?
* **Solution:**
After a quick Reverse Image Search on Yandex, there are a lot of pictures taken in the same place:
<img width="980" height="357" alt="image" src="https://github.com/user-attachments/assets/701e2188-cfb9-4276-87f2-cbb2f30839bd" />

  Entering one of them it can be seen that the title is “Katz's deli in New York City. Made famous in the film When Harry Met Sally”.
<img width="980" height="503" alt="image" src="https://github.com/user-attachments/assets/86e42fba-9e02-408f-a6b6-b0b679e33452" />

* **Flag:**
`sl{katz's deli}`

* **Question:**
What is the name of the editor?
* **Solution:**
After a simple search with “katz's deli Bon Appétit” the following result appeared:
<img width="980" height="507" alt="image" src="https://github.com/user-attachments/assets/39b05cbe-7508-46bc-b44c-46a2111f50d0" />

  In the description of the first link that appeared it states that the name of the editor is: Andrew Knowlton.
<img width="809" height="280" alt="image" src="https://github.com/user-attachments/assets/d1ce884e-eb65-46a6-afa8-b3b0a5d90f9c" />

* **Flag:**
`sl{andrew knowlton}`

---

**Information:**
<img width="980" height="735" alt="image" src="https://github.com/user-attachments/assets/e397d43f-eb41-4a58-a7c5-3ad711652bbb" />

*For the following questions I cannot use reverse image search.*

* **Question:**
What is the name of this statue?
* **Solution:**
With just a simple search: “Sculpture with a motorcycle body, and reindeer legs and antlers” I got the following result:
<img width="980" height="506" alt="image" src="https://github.com/user-attachments/assets/b1fa26fc-7335-4d0e-a482-685c4d3c9d20" />

  The first result shown is the exact picture that I got, named “Rudolph the Chrome Nosed Reindeer”.
* **Flag:**
`sl{Rudolph the Chrome Nosed Reindeer}`

* **Question:**
Who took this image?
* **Solution:**
When searching for “Rudolph the Chrome Nosed Reindeer Oslo” on Google I have seen a site named “Visit Oslo” where you are able to search for a sculpture by its name.
<img width="980" height="503" alt="image" src="https://github.com/user-attachments/assets/a31d6998-6b82-4001-bc04-d0fbd1ad782d" />

  When searching for “Rudolph the Chrome Nosed Reindeer” it shows the exact location of it and also who took the photo: Kjersti Stensrud.
<img width="573" height="653" alt="image" src="https://github.com/user-attachments/assets/1c42771c-2950-432e-9300-90e365cc0926" />

* **Flag:**
`sl{kjersti stensrud}`

---

**Information:**
<img width="980" height="655" alt="image" src="https://github.com/user-attachments/assets/3d5f55ea-c189-4c70-b919-dbfe584f54d9" />


* **Question:**
What is the name of the character that the statue depicts?
* **Solution:**
After a quick reverse image search on Yandex with the picture, I found this:
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/7114c654-b16a-443e-8a82-4641f766c351" />

  After entering the link, on the YouTube video it can be seen that the exact statue is in front of “Albert V. Bryan United States Courthouse”.
<img width="980" height="692" alt="image" src="https://github.com/user-attachments/assets/8bea38c4-b4ec-4496-8a0b-18901dd1e2d6" />

  After this I searched for the name of the statue and found out that it is "Blind Justice".
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/0a9315d1-a074-4155-9fa4-cf7b37fe6e45" />

  I searched more information about this statue and all the searches were referring to a character named “Lady Justice”.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/55030997-878f-4d8f-b554-0a0504e74085" />

* **Flag:**
`sl{lady justice}`

* **Question:**
Where is this statue located?
* **Solution:**
* Going back a few steps, searching for “Albert V. Bryan United States Courthouse” retrieves this exact information in the first rows: Alexandria, Virginia.
<img width="980" height="407" alt="image" src="https://github.com/user-attachments/assets/a8db2c8f-110e-4be5-814a-4f5796f2eb1e" />

* **Flag:**
`sl{alexandria, virginia}`

* **Question:**
What is the name of the building opposite from this statue?
* **Solution:**
I searched for “Albert V. Bryan United States Courthouse” on Google Maps.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/5b624b0a-9af4-4028-ae25-ce10c5861319" />

  I entered the Street View mode to be sure that I am looking on the right side of the building.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/5bb8045a-0c16-47c9-ac1f-8da6a4e6d9c8" />

  Then I turned around to see what building is behind me.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/c2822b8b-2ed7-444c-b995-84092c04037c" />

  Now exiting the Street View mode I could see that the name of the building is “The Westin Alexandria Old Town”.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/b33d61fa-f79d-4452-b8c8-85c8f03213ba" />

* **Flag:**
`sl{the westin alexandria old town}`

---

**Information:** 
A video taken from the balcony.

https://github.com/user-attachments/assets/b51ce289-2df0-4fc3-a043-c2367b57db5e



* **Question:**
What is the name of the hotel that my friend stayed in a few years ago?
* **Solution:**
In the video there was clearly a shot taken of the Riverside Point Mall.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/a92047eb-860a-4d5e-b9d1-770a2aeff900" />

  So I searched for it on Google Maps.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/d1e6a6b5-984d-4f40-b78b-b5b91158140f" />

  The area was pretty similar to the one seen in the video (a green area to the left of the place where the video was taken and a river to the right side).
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/47421ab0-b41d-44d3-bb1f-9bb4b042ecf7" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/53356a00-a5e2-4a18-8e20-dd9bd2dd361d" />

  This means that the area I am looking for is around here:
<img width="980" height="1063" alt="image" src="https://github.com/user-attachments/assets/7c4dccc2-0006-48f8-a8a4-d85a07badf27" />

  Considering that the Riverside Point mall was close to the right of the area where the video was taken, it means that the place I am looking for is either on Tan Tye Pl or on Clarke Quay.
  Going into Street View Mode, I cannot see any building that tall such as the one in the video. Despite that, I was able to see some houses that looked similar to the ones in front of the hotel where the video was taken.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/4077431c-5859-447f-9a2f-b9b2823d91f4" />
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/15a81a09-1aeb-4b5f-9d4c-b784644ce6c2" />

  This means that the building I am looking for should be on the left side of my Google Maps, but it was taken down in the last years.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/ec54f991-7f0e-4d84-8dd5-6a9bb2bbc33b" />

  So I switched the year of the map to 2019 and I found the building.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/5e951796-36fc-4b81-b93a-20dffe7a520a" />

  Following the side of the building I found that it was named Liang Court.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/1dedc483-9949-40a8-9c07-537053952a14" />

  After searching about it online it was a Chinese-only mall which included a hotel and a residential area. After a Google Search about it I found a page which contained nostalgic buildings, one of them being Liang Court.
<img width="980" height="527" alt="image" src="https://github.com/user-attachments/assets/f2ec75c4-e488-4ca2-92f0-c74d9651279a" />

  In the description it stated clearly that the complex included Novotel Clarke Quay and Somerset Liang Court Residences.
* **Flag:**
`sl{novotel singapore clarke quay}`
