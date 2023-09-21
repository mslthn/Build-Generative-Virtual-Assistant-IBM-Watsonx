# Setup Your Watson Machine Learning

First of all, click on this [link](https://cloud.ibm.com/) to create the IBM account and follow the steps. Then your account will look like this:
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/2eca1288-635c-48e2-bab3-7126bcd55453)
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/2bc8116f-2d0d-4e9a-94ad-e85aad1ed9a5)

Type "Watson Machine Learning" into the search field, select Watson Machine Learning and activate the service :
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/db1d4edc-8120-4d2a-af5a-43ee97b07d11)

Checklist the checklist button "I have read and agree to the following license agreement" then select the plan you want to use, then select location Dallas-US and click create.

Please note that Watson Machine Learning runs when IBM Cloud Pack For Data is installed in your IBM account, you can read the following link as a reference for [IBM Cloud Pack For Data setup](https://cloud.ibm.com/docs/cloud-pak-data?topic=cloud-pak-data-getting-started)

# Setup WatsonX
After activating the Watson Machine Learning, WatsonX is ready to run.
Type in the IBM Cloud search field "**WatsonX**" and click on it.
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/31d5a467-7f1b-4d51-9f3e-bed4101dd345)

Later, you will be instructed to log in or register using your ibm cloud account, fill in according to the instructions, and your page should be like this:
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/bb33f944-59f0-4d8a-ae69-a15d34f42b53)

Click on the "Get Started" button, since I've already used the service from IBM WatsonX so it says "launch" then the page should look like this:
![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/86b418c8-072b-4180-9175-bc2c5b83101c)

Click the menu in the upper left corner and select "**Project, View All Project**" then follow the steps below:
* Create a new project by clicking "**New Project**"
* Select "**Create an empty project**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/a54a5b28-3117-4e8f-9530-1d8136901809)

* Enter your project name, then enter your project description (optional)
* Then click "**Create**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/7ca9f151-b55a-49e6-a3f8-8a59c46fd8fa)

* Click "**Assets**" and click "**New task**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/5616fa6b-89a2-4678-9e00-b643da88e77c)

* Select "**Experimenting with foundation models and build prompts**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/85b1ee94-5bfb-4f76-b8fc-fccd17412e50)

* A notification will look like this:
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/3de091cb-aa91-4e32-a4b3-2ec238ab5444)

* Click "**Associate Service**" and select "**Watson Machine Learnig**" and click "**Associate**"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/0d554fcb-ed68-4a69-a399-dd1a67c56cc3)

* Return to the "**Assets**" menu and "**Create new task**" as above
* And your page will look like this:
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/61f19b35-f18e-4747-8c38-5e8280c40b5f)

* Click on the menu I've rounded up and select "Question About an Article"
  ![image](https://github.com/mslthn/Build-Generative-Virtual-Assistant-IBM-Watsonx/assets/75915809/0acdf35a-1ee9-45c4-b0f3-0071b45f68a8)


* Enter the following text into the "**Setup**" menu
```
Answer the following question using only information from the article. If there is no good answer in the article, say "Sorry, i cant get your answer. Because my foundation not updated yet😅".

Article: 
###
FC Barcelona, often referred to simply as Barcelona or Barça, is one of the most renowned and successful football clubs in the world. Here's a brief overview of the club's history and significant years:

Foundation (1899): FC Barcelona was founded on November 29, 1899, by a group of Swiss, English, and Catalan footballers led by Joan Gamper. The club's first president was Walter Wild.

Early Success (1910s - 1920s): Barcelona won its first Copa del Rey (Spanish Cup) in 1910. In the 1920s, they won several regional and national titles, solidifying their status in Spanish football.

Civil War and Franco Era (1930s - 1940s): During the Spanish Civil War and the subsequent dictatorship of Francisco Franco, the club faced numerous challenges. Its Catalan identity made it a symbol of resistance against Franco's regime.

Golden Era (late 1940s - 1950s): The 1940s and 1950s were marked by tremendous success for Barcelona. Players like Ladislao Kubala and Luis Suárez led the team to win numerous domestic and international titles.

Cruyff's Era (1970s - 1980s): Johan Cruyff's arrival as a player in the 1970s and later as a manager in the late 1980s had a profound impact on Barcelona. He implemented a playing style known as "Total Football" and won the club's first-ever European Cup (now UEFA Champions League) in 1992.

The Dream Team (1990s): Under Cruyff, Barcelona's "Dream Team" achieved great success, winning four consecutive La Liga titles from 1991 to 1994.

Modern Era (2000s - Present): In the 21st century, Barcelona reached the pinnacle of football success under managers like Pep Guardiola. The team won numerous domestic and international titles, including multiple UEFA Champions League titles and La Liga championships.

Lionel Messi Era: The club's most iconic player, Lionel Messi, made his debut for Barcelona in 2004. Messi became the club's all-time leading scorer and led the team to numerous victories.

Recent Challenges: In recent years, Barcelona has faced financial challenges, leading to the departure of Lionel Messi to Paris Saint-Germain in 2021. The club has been rebuilding its squad and finances.

FC Barcelona's history is rich with success, iconic players, and a commitment to a distinctive style of football known as "tiki-taka." The club has a passionate global fan base and remains a symbol of Catalan culture and identity.
###
```
* In the example field, enter as follows:
  
| Question                   | Answer                                                                                                                                |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| What is FC Barcelona       | FC Barcelona, often referred to simply as Barcelona or Barça, is one of the most renowned and successful football clubs in the world. |
| When FC Barcelona was born | FC Barcelona was founded on November 29, 1899, by a group of Swiss, English, and Catalan footballers led by Joan Gamper.              |

![image](https://github.com/yogasungkowo/Build_Generative_Virtual_Assistant_With_IBM_WatsonX_Watson_Assistant/assets/93362737/3ffeee19-8787-4968-8e2c-486b7d4e34a2)

* Try prompt and make sure bot answer correctly
* Select the part that I highlighted:

![Screenshot (8)](https://github.com/yogasungkowo/Build_Generative_Virtual_Assistant_With_IBM_WatsonX_Watson_Assistant/assets/93362737/e20d3e67-c906-4a50-a32f-f9c1da92aabf)

* Make sure the options like the following:
  * Decoding Type: Greedy
  * Repetition Penalty : 1
  * Stop Sequences: (enter), and "." (period)
  * Min token: 0
  * Max tokens: 500
    
# After doing all the instructions correctly, the step for the setup of WatsonX has been completed





