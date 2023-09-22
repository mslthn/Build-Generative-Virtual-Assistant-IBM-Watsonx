# Mulai membuat Chatbot dengan Watson Assistant
Pada tahap pembuatan project chatbot ini, kamu membuat 3 action diantaranya:
* ViTu (Visit Tuban)
* Tourist Spots
* Local Wisdom

## 1. ViTu (Visit Tuban)
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

### Step 5:
* Pada bagian _Is taken_, pilih **with condition**. Ketika penggunaan extension pada step 4 berhasil "**Ran successfully**".
* Tambahkan variabel pada _Set variable values_, lalu beri nama "**result**" sebagai _free text_.
* Pada bagian _Asisstant says_, isikan dengan variabel yang baru dibuat yaitu "**result**".
* Pada bagian _And then_, pilih **Continue to next step**.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/4aaca0ea-8d11-44bc-ae33-6b0c9ff11b0f)

### Step 6: 
* Pada bagian _Is taken_, pilih **with condition**. Pada step ini dimana Customer memilih opsi "**Tourist Spots**" pada Step 2 sebelumnya.
* Pada bagian _And then_, pilih **Go to a subaction**. Pilih subaction _Tourist Spots_.
  Subaction Tourist Spots bisa dilihat disini: (link)
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/145754405/abf10a1a-4d53-4461-9886-2dd9acacba56)
