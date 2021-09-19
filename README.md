<h1 align="center">
  <br>
<!--   <a href="http://www.amitmerchant.com/electron-markdownify"><img src="https://raw.githubusercontent.com/amitmerchant1990/electron-markdownify/master/app/img/markdownify.png" alt="Markdownify" width="200"></a> -->
  <br>
  ANTIDOTE
  <br>
</h1>

<h3 align="center">Visit Website: <a href="https://akriti.pythonanywhere.com/" target="_blank"> antidote.com </a></h3>

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
![Python](https://img.shields.io/badge/python-3.8.1-blue)
![Version](https://img.shields.io/badge/version-1.0.0-orange)
![Dependencies](https://img.shields.io/badge/dependencies-up%20to%20date-brightgreen.svg)
![Contributions welcome](https://img.shields.io/badge/contributions-welcome-orange.svg)
[![License](https://img.shields.io/badge/license-%20GPL--3.0%20-blue)](https://github.com/Akriti0100/Antidote/blob/main/LICENSE)

<div align="justify">
<!-- # 🧐 Project overview -->

> A major challenge faced by many healthcare organisations is the provision of quality medical services at affordable costs which implies proper diagnosis of the patient. Apart from this the surge in covid-19 cases witnessed has reduced the routine visits made by the patients which includes the routine care for pregnant women, elderly patients and timely immunisation of the infants. `Antidote` is a service built to solve this problem. Patients as well as doctors can register themselves on the portal. Users can send request to the predicted disease specialists and schedule appointment. 
</div>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-to-use">How To Use</a> •
  <a href="#ml-models-used">ML Models</a> •
  <a href="#project-scope">Project Scope</a> •
  <a href="#license">License</a>
</p>

<div align="justify">
  
## Key Features

* Registration/Login 
  - The users need to create an account on the portal before they can start accessing the functionalities. 
  - After user logins, he/she will be assigned a token for the entire session to make sure that he/she is authenticated.
* Edit profile 
  - The patients and the doctors can edit the information given at the time of registration by navigating to the ‘Edit profile’ tab and saving the changes which updates the information stored in the database. 
* Disease prediction and Doctor suggestion
  - This feature will help the patient predict the disease he/she is likely to suffer from. A list of symptoms is provided on the screen where the person is supposed to select the symptoms, he/she has witnessed recently. 
  - These symptoms act as an input to the models followed by the predicted disease being displayed. 
  - The patient can search for the concerned doctor within our database or any other doctor based on their location.
* Uploading medical reports
  - Patients can keep a track of their medical history by uploading their reports along with the details of previous appointments which can be accessed anytime. This also provides an added benefit of forwarding the reports to the doctor if requested. 
* View active patient’s details 
  - The doctor after logging in would be able to see a list of patients who have requested an appointment and the ones he/she is currently attending. 
* Appointment Confirmation 
  - The doctor to whom the patient sends the request can set up an appointment with him/her for further consultation and diagnosis if he/she feels the need for the same. 
  - This will also replace the manual procedures of recording the appointment dates thereby increasing the reliability, efficiency and performance of the product.
* Prescription 
  - Doctors can send a prescription which can then be viewed by the patient. 
  - Depending upon the prediction and reports shared, the doctor can decide whether to keep the further follow ups in an offline mode through the portal and asking the patient to follow the prescription till the next check-up or suggest a course of the medicine for a certain period which would be enough to recover from the disease.

</div>

<div align="justify">

## ML Models Used

* Random Forest Classifier [Refer: `disease_ran.pkl` for implementation]
  - It is similar to the decision tree algorithm. It is a flowchart-like structure where each internal node represents a test on the various symptoms entered by the user and each leaf node represents the class label i.e. the diseases.
  - The difference lies in the process of finding the root node (start point) and splitting the feature nodes here the symptoms randomly. The accuracy of the results lies in the number of trees formed. 
  - This model resulted in an accuracy of `0.998` on the test dataset.

* Logistic Regression [Refer: `disease_log.pkl` for implementation]
  - It is most suited for binary classification though it can be used for multinomial classification. 
  - It makes use of a logistic function i.e., softmax function to categorise the input data. 
  - The probabilities determined by SoftMax function are then used by crossentropy function to calculate the distance from the target classes available. The one which results in the minimum distance is our predicted target class.
  - This model resulted in an accuracy of `1.0` on the test dataset.

```
  - The disease class which is predicted by a majority of the models is the final result. 
  - In case of equal majority, 
    * The result of random forest model is displayed since it is comparatively more accurate than logistic regression.
    * This is because latter resulted in overfitting of the training dataset.
  
```

</div>

<div align="justify">
 
<!-- # 🧐 Project overview -->
 ## Project Scope

> Everything today is moving towards digitalization. This platform designed will increase the efficiency of the hospitals and bring the specialists from the nooks and corners of the country available at a single platform. 
>
> It will help overcome the challenge of increased drop rate in the regular patient visits and also help patients to consult the doctors in case of emergency situations by fixing an appointment without the need to visit the hospital. 
>
> This would also help to overcome the problem of deficiency of human resources in the health sector which is prevalent at several levels such as between regions, between rural and urban areas and between private and public sectors. It's a platform to consult the health care specialists in the respective fields thus, bridging the gap between different sections of the society. 
>
> Apart from these, it aims to reduce the challenges faced by people who are looking online for health information regarding diseases, diagnosis and different treatments.
 
</div>

<div align="justify">
 
## How To Use

To clone and run this application, you’ll need `Git` and `Django` installed on your computer. <br>
From your command line:

```
# Clone this repository
$ git clone https://github.com/Akriti0100/Antidote.git

# Go into the repository
$ cd Antidote

# Install dependencies
$ pip3 install -r requirements.txt
  
# Run the app
$ python manage.py runserver
```

### Login Credentials

* For patient
  - Email id: akritisinghal1663@gmail.com
  - Password: akriti1234
* For doctor
  - Email id: bomepis203@tst999.com
  - Password: testuser0102

</div>

<div align="justify">
 
## License
 
`Antidote` is free and open-source software licensed under the GPL-3.0 License.

</div>
