# HealthCare-Syntactic Processing

‘BeHealthy’, a hypothetical example of a health tech company has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions. The dataset has text written related tot he medical domain. We determine the disease name and its probable treatment from the dataset and list it out in the form of a table or a dictionary.

## Table of Contents
* [General Info](#general-information)
* [General Approach](#general-approach)
* [Conclusion](#conclusion)
* [Contact](#contact)
  
## General Information
Companies like ‘BeHealthy’ are providing medical services, prescriptions and online consultations and generating huge data day by day.

Take a look at the following snippet of medical data that may be generated when a doctor is writing notes to his/her patient or as a review of a therapy that he or she has done.
“The patient was a 62-year-old man with squamous cell lung cancer, which was first successfully treated by a combination of radiation therapy and chemotherapy.”

A person with a non-medical background cannot understand the various medical terms. The objective is to traverse through such data and identify teh disease and correspondig treatment.

## General Approach 

- Data preprocessing - The data given in token format is modified into sentence format.
- Concept identification - PoS tagging is used to identify words from the corpus that have a tag of NOUN or PROPN using spacy library.
- Defining the features for CRF - Features for he current word and previous word are defined. Use of information of the preceding word makes the CRF model more accurate.
- Build the CRF model and evaluate on test set.
- A dictionary with disease as keys and treatments as values is created.

## Conclusion
Using the generated dictionary, the tratment for the disease named 'hereditary retinoblastoma' is predicted.

## Contact
Created by [@jenifer2409] - feel free to contact me!
