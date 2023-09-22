# SetUp Object Storage
* Buat Object Storage terlebih dahulu untuk menyimpan project dari Prompt Lab yang akan di buat nanti.
1. Cari _Object Storage_ pada kolom pencarian, lalu klik seperti gambar dibawah ini:
   ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/c936c2de-51ac-4ce6-b873-a644af31a51b)

2. Lalu pilih:
  * IBM Cloud
  * Plan "Lite"
  * Klik _Create_
    ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/aa3c8e15-cb67-4f40-95fd-f67140393339)

3. Jika sudah, lanjut ke langkah berikutnya.

# Cara Mengintegrasikan WatsonX (Generative AI) ke Watson Assistant

## WatsonX - Prompt Lab
* Buka [link](https://dataplatform.cloud.ibm.com/wx/home?context=wx) ini untuk login ke dalam IBM watsonx.
* Jika sudah login, maka tampilan antarmuka awal akan terlihat seperti ini:
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/863fc79d-ccc8-401d-86fa-879d12795c98)

* Selanjutnya scroll kebawah sedikit, lalu klik _New Project_ seperti yang terlihat pada gambar:
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/70debf61-ade0-41ea-9a87-4d6b7b238c5a)

* Masukkan nama untuk project yang akan dibuat, lalu klik _Create_.
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/af28571c-7c95-4eba-af44-d98329e5b1c1)

* Selanjutnya, lakukan langkah pada tahap ini
  "[SetUp WatsonX](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/blob/main/Pembuatan%20ViTU%20Chatbot%20dengan%20Generative%20AI%20WatsonX%20dan%20Watson%20Assistant/2.%20Set%20Up%20WatsonX.md#setup-watsonx)" untuk memilih sample prompt dan memasukkan data yang akan dilatih serta setting parameternya.

* Setelah itu, klik pada bagian _View Code_ seperti gambar dibawah ini:
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/4e2e347b-3cf9-4fe7-89fd-9b78688109b0)

* Supaya mudah dilihat, klik _expand_ seperti gambar dibawah ini:

  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/b569fec8-4518-4c2c-ad42-77bc6f878095)

* Perhatikan pada bagian yang digaris bawahi:
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/c8bd771d-7154-4bf5-be5e-7a6e98950696)
  Rekam komponen tersebut yang akan kita gunakan sebagai parameter pada Watson Assistant nanti.

## API Key dari Prompt Lab

* Klik logo **i**, lalu klik **Create a personal API key**

  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/572d3542-9aaf-4fd2-8765-6f1c0f53944b)

* Jika sudah, kemudian klik pada bagian _Create +_ lalu ketik nama untuk API key dan Create:
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/da09203e-0cef-4ab5-8291-2f07ef7917ee)

* Klik _Copy_ untuk menyalin API key yang sudah dibuat ke Extension yang akan digunakan nanti
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/5036be2d-6496-40f1-a211-b2473436e8d3)



## Watson Assistant - Extension/Parameter

* Buka [link](https://us-south.assistant.watson.cloud.ibm.com/crn%3Av1%3Abluemix%3Apublic%3Aconversation%3Aus-south%3Aa%2F871161eea5444d4db95bf9b8f2253fb5%3A8ae1e20e-307a-420d-88d1-185f1ad7a790%3A%3A/assistants/85c79987-0e8d-4709-b45f-e7b80d2bbe69/home) untuk membuka Watson Assistant. Lalu klik _Integrations_ seperti gambar dibawah ini:
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/4bbd9db3-d092-4be0-9ede-eabb714aa601)

* Kemudian scroll kebawah, pada bagian_ **Extensions** klik "_Build custom extension_".
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/1420ff87-afdc-43df-b18a-257f69b18064)

* Selanjutnya:
  - Klik _Next_
  - Berikan nama extension sesuai keinginan, lalu _Next_
  - Import API yang sudah di download berupa file .json
    ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/035f84c6-84fc-4d09-bb98-3cd50e6f757b)
  - Lalu klik _Next_ lagi, dan _Finish_

 * Klik _Add +_, pada Environtment pilih _Draft_

   ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/c0db42d9-ad95-4339-b197-e8744496f542)

* Klik Next, lalu pada _Authentication > Authentication type_ pilih **OAuth 2.0**
* Pada kolom Apikey, masukkan API yang sudah dibuat sebelumnya lalu klik _Next_ dan Finish
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/e67096e6-82ba-47a2-bd5e-9e1347954c05)

## Buka Action di Watson Assistant pada Step yang menggunakan Call Extension
* Pada bagian _And then_ pilih "Use an extension". Kemudian pilih extension yang akan digunakan serta set parameter yang dari prompt lab sebelumnya kecuali pada bagian set **input** yang akan digunakan yaitu pada action step yang menggunakan Extension ini.
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/08cd6149-fc05-4c4a-99db-1515f1d4721b)
  ![image](https://github.com/mslthn/Pembuatan-ViTu-Chatbot-dengan-Generative-AI-WatsonX-dan-Watson-Assistant/assets/145754405/408f6615-7fe7-48f1-ab8d-06a34dfb0a19)

_Note: Setelah kami coba, untuk optional parameter diatas tidak harus sama dengan yang di prompt lab. Parameter yang di inputkan pada Watson Assistant ini memungkinkan untuk menggenerate output sesuai kebutuhan._

* SELESAI
