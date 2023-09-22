# Setup Watson Assistant IBM Cloud

* Pertama buka [link ini](https://cloud.ibm.com/) untuk login ke IBM Cloud
* Login dengan akun IBM kamu
* Ketik "**Watson Assistant**" pada search bar, lalu pilih "**Watson Assistant**"
* selanjutnya, ganti wilayah menjadi Dallas-US, pilih plan lite, dan centang "**i have read and aggree to the license aggreement**", lalu klik "**Create**"
* Setelah Watson Assistant Service dibuat, Anda dapat melihatnya di search bar dan tampilan akan terlihat seperti gambar dibawah ini :
  
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/0738386c-50ca-4be1-91ed-7d7608766552)

* Klik pada "**Watson Assistant-(random character, for me is Watson Assistant-aa, it would be different per user)**"
* Klik "**Launch**"
* Setelah klik launch, tampilan tab Anda akan terlihat seperti gambar berikut :

![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/3176afbb-cabf-4c0a-8107-bb94c5178d4d)

# Setup WatsonX Extension di Watson Assistant

Sebelum kita mengatur virtual agent, kita harus menghubungkan WatsonX Generated AI dengan Watson Assistant agar virtual asisten kita dapat menghasilkan serangkaian kata atau kalimat layaknya bot yang ada di chat GPT, Bing, dan lainnya.
* Klik metu di pojok kiri atas, lalu pilih "**Integration**"
* Scroll kebawah dan pilih "**Build Custom Extension**"
* Untuk langkah selanjutnya, kita membutuhkan WatsonX API KEY yang didapatkan dari projek yang telah kita buat
* Kembali ke WatsonX dan buka project assets, lalu klik pada ikon seperti pada gambar
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/738124ef-2697-4dba-b5ed-15f3b6837f5f)

* Buat personal API key dengan klik "**Create a personal API key**"
* Setelah klik "Create", akan diarahkan ke tab baru untuk membuat Personal API Key
* Beri nama API key dan tuliskan deskripsi sesuai kebutuhan
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/faf9da30-bc5c-4379-8130-43b320614cd2)

* Klik "**Create**"
* Copy API Key / Download, lalu kembali lagi ke Watson Assistant
* Klik "**Next**"
* Isi Extension Name dan Extension Description lalu klik next
* Download JSON file from [this link](https://github.com/watson-developer-cloud/assistant-toolkit/blob/master/integrations/extensions/starter-kits/language-model-watsonx/watsonx-openapi.json).
* Selanjutnya pilih file JSON yang tadi sudah diunduh pada direktori file kamu, atau dapat juga dengan cara drag and drop file JSON tersebut ke bagian kotak unggah :

![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/7e491303-ba30-4bdc-8f07-fb11eb29ee52)

* Klik "**Next**"
* Klik "**Finish**"
* Scroll kebawah ke bagian extension menu dan klik "**Add**"
* Klik "**Next**"
* Pilih "**Oauth 2.0**" pada Authentication Type
* Paste API Key dari WatsonX, yang sudah kita copy sebelumnya ke "**Api Key Form**"
* Klik "**Next**"
* terakhir "**Finish**"

# Setup Action pada Watson Assistant

Setelah berhasil mengintegrasilam WatsonX dan Watson Assistant, langkah selanjutnya adalah testing
* Buka menu pada bagian pojok kiri atas, lalu pilih "**Action**"
* KLik "**New Action**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/170d83e8-be31-4ccd-8ad5-491aafa1e0e3)

* Tuliskan "Customer Say" untuk memanggil Bot, untuk kali ini saya menggunakan kata "hai" untuk memulai interaksi dengan bot
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/5151b31e-d551-490e-ac96-2cd00e9262a5)

  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/2e44e6a8-a213-4827-99ab-92d113414506)


* Lalu atur kalimat apa yang akan keluar pertama dari bot dan disampaikan ke user nantinya. Disini saya menanyakan hal apa yang ingin user ketahui mengenai Tuban, lalu pilih Customer response dengan "**Free Text**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/43b3509b-fde1-4033-aeee-46e203988cde)

  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/6fde2373-18e5-4dd0-b696-9f216864228b)


## Import WatsonX ke Watson Assistant

* Pilih "**New Step**"
* Pada menu "_And Then_" pilih "**Use an Extension**"
* Klik extension dan pilih extension yang tadi telah dibuat
* Klik "**Generation**" pada "_Operation_" 
* Untuk parameter kita dapat melihatnya dari WatsonS prompt lab pada bagian "view Code", lalu isikan sesuai dengan detil parameter yang ada disana seperti gambar dibawah ini.
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/e70ef1c9-8f1b-4b1c-ae05-47db0f92a9c9)


* Untuk input parameter pilih "**Action Variables**" lalu pilih "**step 1**"
* Setelah mengatur extension, selanjutnya membuat variable untuk memanggil extension
* Klik "**New Step**"
* Ganti "**Is taken to** ke "**With conditions**"

https://github.com/yogasungkowo/Build_Generative_Virtual_Assistant_With_IBM_WatsonX_Watson_Assistant/assets/93362737/2eec23cd-ea8c-4ad1-b695-ac985763db34

* klik "**Set Variable Values**"
* klik "**Set New Value**", "**New Session Variable**", insert the variable name, this time e.g result, and variable type select "**Free Text**"
* pada "variable to" pilih "**Expression**" dan masukkan kode ini
```
${step_472_result_1.body.results}[0].generated_text
```

https://github.com/yogasungkowo/Build_Generative_Virtual_Assistant_With_IBM_WatsonX_Watson_Assistant/assets/93362737/3d2a9ebb-b655-495b-b03f-03926c26269d

* Tahap setup telah selesai, selanjutnya kita dapat menguji botnya apakah sudah berjalan dengan baik, klik "**preview**" pada pojok kanan bawah

https://github.com/yogasungkowo/Build_Generative_Virtual_Assistant_With_IBM_WatsonX_Watson_Assistant/assets/93362737/83ee4409-5d7f-479f-832f-fc2cd4429f6a

# Membuat ViTu (Visit Tuban) Chatbot Virtual Assistant

