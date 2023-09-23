# Tahap Pembuatan Prompt untuk Chatbot

Klik pada tombol "Get Started", namun karena saya sudah membuat servis dari IBM ini, jadi jika tampilan anda seperti ini langsung saja klik "Launch" dan tampilan web anda akan seperti gambar dibawah ini
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/bb33f944-59f0-4d8a-ae69-a15d34f42b53)

![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/86b418c8-072b-4180-9175-bc2c5b83101c)

Klik menu di pojok kiri atas, lalu pilih "**Project, View All Project**" dan ikuti langkah seperti berikut:
* Buat projek baru dengan klik "**New Project**"
* Pilih "**Create an empty project**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/a54a5b28-3117-4e8f-9530-1d8136901809)

* Isi "project name" sesuai keinginan dan juga "project description" (opsional)
* Lalu klik "**Create**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/7ca9f151-b55a-49e6-a3f8-8a59c46fd8fa)

* Klik "**Assets**" dan klik "**New task**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/5616fa6b-89a2-4678-9e00-b643da88e77c)

* Pilih "**Experimenting with foundation models and build prompts**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/85b1ee94-5bfb-4f76-b8fc-fccd17412e50)

* Lalu akan tampil notifikasi seperti pada gambar, lalu klik "**Associate Service**" dan pilih "**Watson Machine Learnig**", lalu klik "**Associate**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/3de091cb-aa91-4e32-a4b3-2ec238ab5444)

  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/0d554fcb-ed68-4a69-a399-dd1a67c56cc3)

* Kembali ke menu"**Assets**" dan "**Create new task**"
* Lalu halaman web akan tampil seperti ini:
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/61f19b35-f18e-4747-8c38-5e8280c40b5f)

* Klik pada menu, lalu pilih "Question About an Article"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/0acdf35a-1ee9-45c4-b0f3-0071b45f68a8)


* Masukkan teks berikut ke menu "**Setup**"
```
Answer the questions asked from the articles that have been created below. If there is no good answer in the article, say "I don't know".

Article: 

Title : About Tuban, East Java, Indonesia.

###

Kota Tuban is a city located in the East Java province of Indonesia. Tuban City is situated in the northeastern part of East Java province, bordered by the Java Sea to the north. The city has a long history and has been a part of various civilizations and kingdoms throughout Indonesia's history.

The meaning of the word comes from Javanese which means "out of the water". Tuban is a combination of the word "meTU BANyune". Javanese people often make two or more sentences shorter. In the previous two words, the Javanese combined the two words into a word. The two words "meTU BANyune" are shortened to one word namely "Tuban".
Tuban Regency is one of the 38 regencies and cities in the administrative region of East Java Province. Tuban Regency area is on the northern coastal strip (Pantura) of Java Island.

Tuban Regency is an area located on the north coast of East Java Province, precisely Lamongan Regency in the east and Bojonegoro Regency in the south. There are many Tuban specialties encountered, some of which are made from the main ingredients of sea fish. The reason is, this area is classified as a coast that has a fairly wide coastline. In addition to crabs, there is another food that is fun and interesting to enjoy, namely rica-rica eel. This savory and high-protein slippery animal, ready to pamper your tongue and relax your stomach. The technique of processing this food is quite easy, namely the eel is fried until cooked, then mixed with the rica-rica seasoning that has been prepared.

Tuban is indeed famous for its religious tourism spread in various regions, such as the Great Mosque of Tuban, the Tomb of Sunan Bonang, to the tombs of other religious leaders. But Tuban also keeps the charm of natural beauty that is so exotic and stunning.

Tourist destinations that you can visit while in Tuban: 
1.	Beach : Pantai Boom Tuban, Pantai Sowan Tuban, Pantai Pasir Putih Remen, Wisata Pantai Kelapa, etc.
2.	Waterfall : Air Terjun Nglirip, Air terjun Banyu Langse, Air Terjun Lembah Bongok, etc.
3.	Cave : Goa Ngerong, Goa Akbar, Goa Putri Asih, Goa Kancing, etc.
4.	Baths / Water Sources : Pemandian Bektiharjo, Sumber air Krawak, Wisata Nganget, Wisata Prataan, Wisata Pelangi.
5.	Religious Tourism : Great Mosque of Tuban, the Tomb of Sunan Bonang, the Tomb of Syekh Ibrahim Asmoroqondi.

###
```
* Pada bagian "example", isikan seperti pada bawah ini:
  
| Question                   | Answer                                                                                                                                |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| What is Tuban Specialities?       | There are many Tuban specialties encountered, some of which are made from the main ingredients of sea fish. The reason is, this area is classified as a coast that has a fairly wide coastline. In addition to crabs, there is another food that is fun and interesting to enjoy, namely rica-rica eel. |
| What is Tuban? | Kota Tuban is a city located in the East Java province of Indonesia. Tuban City is situated in the northeastern part of East Java province, bordered by the Java Sea to the north. The city has a long history and has been a part of various civilizations and kingdoms throughout Indonesia's history. |
| Can you tell me, where is Tuban location? | Tuban Regency is an area located on the north coast of East Java Province, precisely Lamongan Regency in the east and Bojonegoro Regency in the south. There are many Tuban specialties encountered, some of which are made from the main ingredients of sea fish. |
| What destinations are often visited in Tuban? | Some of the destinations often visited in Tuban include the Great Mosque of Tuban, the Tomb of Sunan Bonang, the Tomb of Syekh Ibrahim Asmoroqondi, Pantai Boom Tuban, Pantai Sowan Tuban, Pantai Pasir Putih Remen, Wisata Pantai Kelapa, Air Terjun Nglirip, Air terjun Banyu Langse, Air Terjun Lembah Bongok, Goa Ngerong, Goa Akbar, Goa Putri Asih, Goa Kancing, Pemandian Bektiharjo, Sumber air Krawak, Wisata Nganget, Wisata Prataan, Wisata Pelangi. |
| What is the meaning of the word 'Tuban'? | The word "Tuban" comes from Javanese which means "out of the water". Question: What is the history of Tuban? Answer: Tuban has a long history and has been a part of various civilizations and kingdoms throughout Indonesia's history. |
| What combination does the word 'Tuban' come from? | Tuban is a combination of the word "meTU BANyune". Javanese people often make two or more sentences shorter. In the previous two words, the Javanese combined the two words into a word. The two words "meTU BANyune" are shortened to one word namely "Tuban". |
| Is there anythings in Tuban City? | Tuban City is a city located in the East Java province of Indonesia. Tuban City is situated in the northeastern part of East Java province, bordered by the Java Sea to the north. The city has a long history and has been a part of various civilizations and kingdoms throughout Indonesia's history. |

![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/8831d545-13db-4c64-9ec5-7524fed3945c)

* Pastikan parameter pada Prompt Lab diset terlebih dahulu. Parameter ini digunakan untuk menggenerate pertanyaan yang ditanyakan pada Prompt Lab dengan Generative AI, set parameter sebagai berikut:

  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/42b4ae7d-4caa-49ba-8a28-3202129a5fbb)
  - Model : llama-2-70b-chat
  - Decoding : Greedy
  - Repetition Penalty : 1
  - Stopping Criteria : "." dan "enter"
  - Min Token : 50
  - Max Token : 200

_Note: Dengan setting parameter diatas, memungkinkan AI akan memberikan jawaban sesuai kebutuhan yaitu seberapa panjang jawaban yang akan diberikan dari min dan max token._

* Lakukan percobaan pada kolom Try dengan memasukkan pertanyaan dan output yang kita inginkan, seperti contoh berikut:
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/ef59af2f-c3d1-44c8-9ca0-a4891f4d0694)

* SELESAI

  
