AI Health and Care Award
Engagement form

s# Brief description of the health or social care problem you are looking to address and how you think your product will solve this: *

Operational efficiency in the NHS depends on an accurate view of future demand. Elective surgical procedures represent a modifiable portion of that demand that can be used to even out service utilisation by emergency case load. Most bed demand (forecasting) solutions are simulations and unable to predict outside of observed experience. We have instead built a *demand* forecasting solution that allows operational teams to reschedule and reallocate resources. We have experience of deploying this in a single centre for a single ward (Paediatric cardio-thoracic critical care) but have now established a partnership that would scale this hospital wide, and potentially across the NHS by respecting modern interoperability standards.

## 1) Brief description of the product: please describe your product application *

An inpatient bed demand forecasting solution that exploits both measured patient level characteristics, and the historical patient flow patterns to predict future demand at ward level up to 1 week in advance.

## 2) Brief description of the product: please describe the possible indications it could be used for *

This is currently in use by the bed management and booking team on a paediatric cardiothoracic critical care unit. They are able to see future ‘crunch points’ for bed demand, contact families and reschedule a case when demand cannot be met, or alternatively flex staffing capacity up. The same scenario exists for all inpatient surgical pathways, and for other ‘scheduled’ medical procedures requiring or likely to require inpatient admission(e.g. chemotherapy administration). 

## 3) Brief description of the product: please include details of any proof of concept testing or relevant previous research *

An earlier version of the software product has been in use at Great Ormond Street Hospital since 2012 (Pagel C, Banks V, Pope C, Whitmore P, Brown K, Goldman A, et al. Development, implementation and evaluation of a tool for forecasting short term demand for beds in an intensive care unit. Operations Research for Health Care. 2017;15:19–31.) Since 2018, a new collaboration with University College Hospital London has been in progress that extends the original model (non-markovian multi-stage journeys), and scales its application from a single ward product to a hospital wide system using generic admission/discharge/transfer message types (HL7 v2.3). This proof of concept has been successfully deployed, and we are now ready to evaluate model accuracy, and extend the features used for prediction.

## Brief description of the research proposed: *
- Please include any research questions that you intend to answer 
- What are the project deliverables? 
- Do you require expertise and academic input into your study design? 
- If relevant, please provide sufficient methodological detail

### The research question could be best phrased

Does a model of inpatient bed demand produce reliable, valid and actionable predictions across a range of contexts in a large tertiary referral inner city hospital?

### Project timeline (summary)

- rewrite refactoring of code base (currently in Python without unit tests, functional testing; proposed switch to Java Hibernate framework and achieve alignment with MDR regulations for decision aids in healthcare)
- extend feature non-Markovian model to include features embedded in (1) existing source data (e.g. demographics, clinical specialty, labelled structural descriptions of hospital infrastructure) (2) routine vital signs and clinical laboratory data. All additional features to be encoded in a modular fashion such that the model can be deployed across institutions with low and high (HIMSS 2-7) digital maturity indices
- design-led user interface development
- deployment and evaluation of core model
- deployment and evaluation of enhanced model
- IP and commercial evaluation  

Project deliverables

- extension of the model to use generic inpatient level administrative and clinical features (e.g. demographics, clinical speciality, laboratory measures)
- an evaluation of the performance of the model across of a range of common scenarios (e.g. different wards, different prediction horizons, different demand scenarios)
- a piece of software the incorporates the existing model but hardened to meet state of the art standards for reliability and interoperability (e.g. code coverage, continuous integration, FHIR/HL7 interface etc.)
- a user interface designed to support decision making built built as a separate module that can support the model but could be swapped out for interfaces provided by existing clinical information systems

We would welcome further external input to our study design but we also believe that we have already assembled a strong and experienced team. Specifically

- Dr Steve Harris (UCLH): a clinician with deep experience of embedded NHS informatics platform design, risk prediction and issues around bed management
- Dr Sonya Crowe and Professor Martin Utley (UCL CORU): methodologists and operational researchers with > 20 years combined experience of demand modelling
- Dr Kehzi Li (UCL Institute of Health Informatics): a senior research fellow with extensive experience of machine learning and AI in health care
- UCL Research Software Engineering was the first team of its kind in the UK. They have been our collaborator for the last 5 years, have particular experience in live message streaming in the NHS, and  will host the post-doctoral software engineer post.


## Please briefly summarise the Artificial Intelligence (AI) component of your technology and justify why this should be considered as AI: *

We have reviewed the AHSN Network AI Initiative. This application clearly covers 'low complexity AI reasoning methods' (classification algorithms, regression etc.) and combined with the realtime health care data platform developed at UCLH can then make recommendations to better manage care (middle complexity AI module). We also propose a modular approach to digital maturity so that where richer feature sets are available we draw on state of the art techniques to improve on the prediction task necessary to define the transition probabilities in the non-Markovian chain. As such the algorithm is ready to deploy across a wide range of NHS institutions but can be locally tuned as fits the available data resources. 


## If you are currently or have previously worked with any NIHR investigators or centres that you know of, please provide details:

## If there are any online sources you would like to highlight to support this form, please list them here:


