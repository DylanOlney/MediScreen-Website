# MediScreen-Website
This is the website for the project and it is intended for participating medical and insurance professionals. 
Professionals, once registered and logged in, can view a list of patients/clients registered to them, select any one and view their details. If a patient/client has entered sufficient medical data via their mobile app, professionals can also get an estimate of that patient's risk of developing certain medical conditions through the Medi-AI service. Professionals may also create reports which are stored to the database and may be read by a patient through their mobile app. Insurance professionals can view a medical professioanal's report for a particular patient, but an insurance professional's report is not visible to the patient's medical professional.

# Medi-AI
This is the back-end machine learning service, written in Python, that can be called upon to estimate a patient's risk of developing certain medical conditions. The service can be called by a professional from the website or by a patient through their mobile app. There are four medical conditions catered for by Medi-AI in this project. Machine learning models have been compiled for each condition and predictions are made by feeding a model with a row of numerical medical data relating to the particular condition. This data, or feature set, is read from the database and has been supplied by the patient via their mobile app. The service uses Python's 'Flask' library which sets up a server in which URL endpoints can be mapped to execute Python functions. The data is posted to these endpoints and the functions process the data, carry out the predictions and return the results.

# Mobile-API
This is a collection of PHP scripts which enable the mobile app to communicate with the database and the Medi-AI service. These files are not directly related to the website but need to be on the server none the less. The mobile app makes HTTP POST requests to these scripts via Android's Volley library and the scripts pass the relevant data back (either from the database or the Medi-AI service).
