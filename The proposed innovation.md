The proposed innovation

### Competitive advantage: 
We have built a hyper-local realtime bed demand forecast that generates ward level predictions of bed demand over the subsequent week. 

We focus on predicting bed *demand* rather than bed *utilisation*; the latter is the more common AI or simulation task but less informative. We eschew predictions under the known strained network and evaluate the 'what might have been' (counterfactual) scenario to gain novel insights.  Specifically, *demand* predictions are upstream of the response, and create a window for intervention (changing discharge priorities, flexing staffing, re-organising schedules etc.).  

### Barriers to adoption: 
The bed demand forecast exists in two forms: (1) a model that uses patient level characteristics but cannot learn or be readily adapted to new settings; (2) a non-clinical model that extends to networks of wards and generalises to new settings. We now are now ready to combine and surpass the best of these two approaches in a new partnership of:

- a machine learning team led by Dr Ken Li at the UCL Institute of Health Informatics who will re-work the CART (regression based) predictions in the first model to use deep neural nets for continuously updating length-of-stay predictions
- a clinical informatics team at University College London Hospital led by Dr Steve Harris that have built infrastructure to permit deployment of the application at varying levels of digital maturity (HIMSS Levels 0-7 using HL7v2.3+ and PAS systems and FHIR and EHRS systems)
- the UCL operational researchers that developed the mathematics used in the forecasts and that have expertise in working with clinicians and managers to specify and deliver predictive tools that fit with clinical and operational realities, led by Dr Sonya Crowe

### Intellectual property
Model development was done by UCL staff (Utley/Crowe) and local implementation by UCLH software engineering (Harris).