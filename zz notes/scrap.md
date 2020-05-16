Scrap notes

- [ ] TODO: transfer learning as part of the novel model

To develop prototypes and generate early clinical  safety/efficacy data towards CE marking

Previously under barriers to adoption
The existing bed demand forecast exists in two forms: (1) a model that uses patient level characteristics but cannot learn or be readily adapted to new settings; (2) a non-clinical model that extends to networks of wards and generalises to new settings. We now are now ready to combine and surpass the best of these two approaches in a new partnership of:
- the UCL operational researchers that developed the mathematics used in the forecasts and that have expertise in working with clinicians and managers to specify and deliver predictive tools that fit with clinical and operational realities, led by Dr Sonya Crowe
- a machine learning team led by Dr Ken Li at the UCL Institute of Health Informatics who will re-work the CART (regression based) predictions in the first model to use deep neural nets for continuously updating length-of-stay predictions
- a clinical informatics team at University College London Hospital led by Dr Steve Harris that have built infrastructure to permit deployment of the application at varying levels of digital maturity (HIMSS Levels 0-7 using HL7v2.3+ and PAS systems and FHIR and EHRS systems)

Plain English Summary.txt

01 The opportunity.md
02 The proposed innovation.md
03 Detailed project plan.md
04 Patient and public involvement.md
05 The team.md

Stage Application- Scientific abstract.md


---


##### Success criteria
##### Application milestone
##### Model milestone: 
##### Man months:
##### Figures
##### Refs 



#### Project progress

- Minimally Viable Product (MVP): an application that takes hand entered data, runs a forecast, and returns the output deployed and running on hospital infrastructure
- Data interfaces for
    - SQL
    - HL7
    - FHIR
- Non-patient centric data
    - e.g. staffing
- RESTful API for predictions
    - patient LoS
    - bed demand
Man months
- Permissions and contracting:
- MVP: 2 months
- Data interfaces: 1-3 months each
Mile stones


Risks & Mitigations
- Permissions and contracting
    - Use existing team
- MVP delays interfere with user testing
- Software maturity


- Milestone: Deployment of combined model
- Risks<>Mitigation:
	- Data access <> £2.9m programme 2018-20 @ UCLH built live data science platform; PoC already deployed and running
