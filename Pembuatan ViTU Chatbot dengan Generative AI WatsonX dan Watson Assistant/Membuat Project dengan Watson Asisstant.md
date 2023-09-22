# Mulai membuat Chatbot dengan Watson Assistant
Pada tahap pembuatan project chatbot ini, kami membuat 3 action pada Watson Assistan yaitu:

Main Action:
* [ViTu (Visit Tuban)](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/blob/main/Pembuatan%20ViTU%20Chatbot%20dengan%20Generative%20AI%20WatsonX%20dan%20Watson%20Assistant/Membuat%20Project%20dengan%20Watson%20Asisstant.md#1-vitu-visit-tuban---main-action)

Subaction:
* [Tourist Spots](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/blob/main/Pembuatan%20ViTU%20Chatbot%20dengan%20Generative%20AI%20WatsonX%20dan%20Watson%20Assistant/Membuat%20Project%20dengan%20Watson%20Asisstant.md#2-tourist-spots---subaction)
* [Local Wisdom](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/blob/main/Pembuatan%20ViTU%20Chatbot%20dengan%20Generative%20AI%20WatsonX%20dan%20Watson%20Assistant/Membuat%20Project%20dengan%20Watson%20Asisstant.md#3-local-wisdom---subaction)

## 1. ViTu (Visit Tuban) - _Main Action_
Action pertama ini, merupakan action utama yang digunakan dalam pembuatan chatbot kami. Langkah-langkah pengerjaannya sebagai berikut:
- Pada bagian _Customer starts with_, isikan kalimat pembuka untuk dapat berinteraksi dengan chatbot.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/9ce56a63-7c70-4f77-b7b9-3f235ffd454c)

### Step 1:
* Pada bagian _Is taken_, pilih **without condition**
* Pada bagian _Asisstant says_, berisi kalimat respon dari kalimat pembuka.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/ce8892a4-c0c8-467d-bc06-cf43c1c6957b)

### Step 2:
* Pada bagian _Is taken_, pilih **without condition**
* Pada bagian _Asisstant says_, berisi kalimat pertanyaan mengenai apa konten yang akan kita cari seputar Kota Tuban.
* Pada bagian _Define customer response_, pilih bagian **Options** untuk menginputkan beberapa pilihan kepada Customer.
* Pada bagian _And then_, pilih **Continue to next step**. 
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/99656f68-1591-4115-975d-17466002a87e)

### Step 3:
* Pada bagian _Is taken_, pilih **with condition**. Pada step ini dimana Customer memilih opsi "**Others**" pada Step 2 sebelumnya.
* Pada bagian _Asisstant says_, berisi kalimat respon.
* Pada bagian _Define customer response_, pilih **Free text**.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/8628bb88-1a66-4215-80c9-8c96d8e4ab12)

### Step 4:
* Pada bagian _Is taken_, pilih **without condition**.
* Pada bagian _And then_, pilih **Use an extension**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/341c56dd-5906-4a97-bde4-22c7dd0b8bab)

Cara menghubungkan WatsonX Extension ke Watson Assistant bisa dilihat di link berikut: 

[klik disini!](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/blob/main/Pembuatan%20ViTU%20Chatbot%20dengan%20Generative%20AI%20WatsonX%20dan%20Watson%20Assistant/Integrasi%20WatsonX%20ke%20Watson%20Assistant.md#watsonx---prompt-lab)

### Step 5:
* Pada bagian _Is taken_, pilih **with condition**. Ketika penggunaan extension pada step 4 berhasil "**Ran successfully**".
* Tambahkan variabel pada _Set variable values_, lalu beri nama "**result**" sebagai _free text_. Variabel ini diisi dengan "_**body.result(extension)[0]["generated_text"]**_".
* Pada bagian _Asisstant says_, isikan dengan variabel yang baru dibuat yaitu "**result**".
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/4aaca0ea-8d11-44bc-ae33-6b0c9ff11b0f)

### Step 6: 
* Pada bagian _Is taken_, pilih **with condition**. Pada step ini dimana Customer memilih opsi "**Tourist Spots**" pada Step 2 sebelumnya.
* Pada bagian _And then_, pilih **Go to a subaction**. Pilih subaction _Tourist Spots_.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/abf10a1a-4d53-4461-9886-2dd9acacba56)

Subaction _Tourist Spots_ bisa dilihat disini: (link)

### Step 7:
* Pada bagian _Is taken_, pilih **with condition**. Pada step ini dimana Customer memilih opsi "**Local Wisdom**" pada Step 2 sebelumnya.
* Pada bagian _And then_, pilih **Go to a subaction**. Pilih subaction _Local Wisdom_.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/6c20b95f-b599-4918-8de5-0a312aed450c)

Subaction _Local Wisdom_ bisa dilihat disini: (link)

### Step 8:
* Pada bagian _Is taken_, pilih **without condition**.
* Pada bagian _Asisstant says_, berisi respon chatbot.
* Pada bagian _Define customer response_, pilih **Confirmation** berupa _Yes_ dan _No_.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/ddfed604-6eee-4827-b972-49cb37124cd5)

### Step 9:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 8 memilih option _No_.
* Pada bagian _Asisstant says_, berisi respon chatbot.
* Pada bagian _And then_, pilih **Re-ask previous step(s)**. Bagian ini akan mengulangi langkah dari step sebelumnya.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/904a1fb6-d7cf-40a3-a6a7-fff3f84c0c04)

### Step 10: 
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 8 memilih option _Yes_.
* Pada bagian _Asisstant says_, berisi respon chatbot.
* Pada bagian _Define customer response_, pilih **Option** berupa _Ask Again_ dan _No, that's enough_.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/bc7f759a-1a63-4a02-b799-127cf392ed3b)

### Step 11:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 10 memilih option _Ask Again_.
* Pada bagian _And then_, pilih **Re-ask previous step(s)**. Bagian ini akan mengulangi langkah dari step sebelumnya.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/5a370975-717f-4ae5-91bf-78b410546d33)

### Step 12:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 10 memilih option _No, that's enough_.
* Pada bagian _And then_, pilih **End the action**. Bagian ini akan mengulangi langkah dari step sebelumnya.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/e50d7a17-8a58-45a4-a337-c4f4603edd7d)

## 2. Tourist Spots - _Subaction_
- Action ini merupakan subaction yang akan di panggil dan digunakan pada action utama. Sesuai namanya, subaction ini berisi daftar tempat-tempat wisata yang ada di Kota Tuban.
- Pada sub action ini tidak diperlukan lagi untuk menginputkan kalimat pembuka seperti pada action utama. Cukup dikosongkan saja agar chatbot tidak kebingungan karena memiliki lebih dari satu kalimat pembuka pada setiap action yang berbeda.

### Step 1:
* Pada bagian _Is taken_, pilih **without condition**.
* Pada bagian _Asisstant says_, berisi respon chatbot.
* Pada bagian _Define customer response_, pilih **Option** dimana terdapat pilihan seperti _Beach_, _Historic Sites_, _Waterfall Tourism_, dan _Religious Tourism_.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/7ee06fc8-915a-496d-b4ed-454e46524a7a)

### Step 2:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 1 memilih opsi _Beach_.
* Pada bagian _Asisstant says_, berisi respon chatbot yang memberikan jawaban terkait wisata pantai yang ada di Kota Tuban serta memberikan preview foto salah satu pantai disana.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/b9847872-b817-44b1-abab-2073ab37d65c)

### Step 3:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 1 memilih opsi _Historic Sites_.
* Pada bagian _Asisstant says_, berisi respon chatbot yang memberikan jawaban terkait wisata tempat bersejarah yang ada di Kota Tuban serta memberikan preview foto salah satu tempat bersejarah yang ada disana.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/e31e04d2-8d05-43e2-be95-fd2adf56fb27)

### Step 4:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 1 memilih opsi _Waterfall Tourism_.
* Pada bagian _Asisstant says_, berisi respon chatbot yang memberikan jawaban terkait wisata air terjun yang ada di Kota Tuban serta memberikan preview foto salah satu wisata air terjun disana.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/4a562b67-7fcb-49cc-9dff-1d29d7a25c22)

### Step 5:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 1 memilih opsi _Religious Tourism_.
* Pada bagian _Asisstant says_, berisi respon chatbot yang memberikan jawaban terkait wisata tempat religi yang ada di Kota Tuban serta memberikan preview foto salah satu wisata tempat religi disana.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/bbf0451c-79ed-4bd5-a176-f9118c4ec7c2)

## 3. Local Wisdom - _Subaction_
- Action ini merupakan subaction yang akan di panggil dan digunakan pada action utama. Sesuai namanya, subaction ini berisi tentang kebudayaan lokal yang ada di Kota Tuban.
- Pada sub action ini tidak diperlukan lagi untuk menginputkan kalimat pembuka seperti pada action utama. Cukup dikosongkan saja agar chatbot tidak kebingungan karena memiliki lebih dari satu kalimat pembuka pada setiap action yang berbeda.

### Step 1:
* Pada bagian _Is taken_, pilih **without condition**.
* Pada bagian _Asisstant says_, berisi respon chatbot.
* Pada bagian _Define customer response_, pilih **Option** dimana terdapat pilihan seperti _Traditional Music_, _Arts and Crafts_, dan _Traditional Performance Arts_.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/34d3e4c8-eba0-412a-b84b-34cbf53bf0aa)

### Step 2:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 1 memilih opsi _Traditional Music_.
* Pada bagian _Asisstant says_, berisi respon chatbot yang memberikan jawaban terkait alat musik tradisional khas Kota Tuban.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/69bf1d86-70b3-4b64-8aa0-e98b795c8f4d)

### Step 3:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 1 memilih opsi _Arts and Crafts_.
* Pada bagian _Asisstant says_, berisi respon chatbot yang memberikan jawaban terkait seni kerajinan khas Kota Tuban.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/5c197264-db6f-47d1-af9c-113ec0928839)

### Step 4:
* Pada bagian _Is taken_, pilih **with condition**. Pada saat step 1 memilih opsi _Traditional Performance Arts_.
* Pada bagian _Asisstant says_, berisi respon chatbot yang memberikan jawaban terkait pertunjukan tradisional khas Kota Tuban.
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/d2858bdb-efe7-4129-b066-b86ed5371061)
