# Background details
TODO: complete online; no specific prose needed here

# Plain English Summary (450 words)
TODO: 2020-05-15: prose below is as per EoI; update in light of modifications whilst writing project plan

More than 1000 patients have elective surgery cancelled every week in the NHS, causing anxiety for patients and families.(D Wong, 2017) Cancellations are upsetting, inefficient, may cause harm, delay treatment, and let slip therapeutic opportunities. Bed capacity is the primary reason for these cancellations. Yet bed capacity fluctuates. Operational efficiency depends on an accurate view of near-future demand, but this is challenging because a hospital is a complex system with many interdepartmental flows, and individual emergencies seem unpredictable.

This challenge can be met by operational modelling combined with Artificial Intelligence. In 2012, we built a demand forecasting solution that supports operational teams to reschedule elective surgery and reallocate resources to avoid last minute cancellations and bed shortages. We deployed and customised this for a single ward: a  cardio-thoracic critical care unit at Great Ormond Street Hospital.(C Pagel, 2017).

However, that technology could not be scaled, nor readily adapted to work in different institutions. In 2018-19, in partnership, with ‘INFORM’ (a translational data science team at University College Hospital), we generalised the underpinning mathematics of the solution and built a prototype that could scale.

Our approach is distinct from most bed modelling approaches in that we deliver forecasts that are local (ward level), and near future (over the next week). Unlike most other bed forecasting models, we predict future *demand* not future bed *utilisation*. Bed utilisation is best thought of as *demand* already mitigated by *actual supply*. More simply, we are interested in bed demand *before* not *after* cancellations have occurred. 
This creates a window for local teams to better use their existing bed capacity by flexing staffing levels, or rescheduling surgical operating lists. More importantly, local teams are enabled to innovate: to find local solutions to predicted bottlenecks and to better use their existing bed capacity. 

We now seek support to

1. Upgrade the AI component of the model so that it can learn from a wider range of patient clinical characteristics (lab results, clinical history, vital signs etc.) 
2. To extend the mathematics to include staffing constraints that must also influence bed availability. 
3. To encapsulate the mathematical model in a software application that is resilient and 'connectable' to hospitals across the NHS (‘interoperability’). Our application would enable both hospitals using predominantly paper notes (most nonetheless have an electronic patient booking system) and hospitals that are already fully paperless.
4. To test the application with clinical and operational teams so that it is reliable, easy and safe to use.

High quality local bed forecasts have the potential to allow the NHS to run at higher capacity, safely and efficiently. This can reduce costs and waste, reduce short-notice cancellations, and ultimately reduce anxiety and suffering for our patients.

# Scientific Abstract (300 word)

For the proposed project, we request funding for 26 months years covering one software engineer, and one post-doctoral research associate supported by MU/SC/SH/KL.

WP-1: 
WP-2:
WP-3:
WP-4:
WP-5:

# Detailed project plan 
OBJECTIVE AS PER PHASE 2: To develop prototypes and generate early clinical  safety/efficacy data towards CE marking

## The opportunity

### NHS unmet clinical need and market plan

We submitted the Expression of Interest for this call on 4 March 2020. On 11 March 2020 the WHO declared COVID-19 a global pandemic. The need for an effective tool to forecast hospital bed demand, and provide reliable, ward level forecasts was pressing when we made the original application. It is even more pressing now. There is no future where NHS capacity is plentiful. Even if we can build temporary hospitals, we cannot instantly train new staff and expand the workforce overnight. Instead it is imperative that we better manage our existing resource, and make the system as efficient as possible. 
Above all we must remember that the problems of bed supply and demand were increasing even before COVID-19. Between 2010 and 2019, NHS bed capacity fell by 10.1%, and bed occupancy levels rose from 85% to 90%, with corresponding knock-on effects in waiting times for A&E, for cancer and for surgery.[@NHS Key Statistics briefing paper 2020]

#### Bed demand prior COVID-19

In 2018, we found in 245 NHS hospitals that on average 10% of surgical admissions had been previously cancelled (more in hospitals with fewer ICU beds, and more emergency work).[@Wong 2018] This amounted to 25,475 operations being cancelled on the day of surgery in just one 3 month period in 2018 (NHS-England): the highest number in two decades. The following winter, NHS-E recommended that all elective surgery be cancelled in January to avoid a repeat.[@Gillies 2018] 
Despite these pressures, NHS operating theatres are often labelled inefficient. In our own hospitals, patients, surgeons, scrub nurses and  anaesthetists are all ready to go from 730am. However, major surgery does not start until after the daily 9am ‘bed meeting’ that reports whether ICU beds are available for high risk surgery. These ICU beds depend on discharges from ICU to the ward. In turn, this depends on clinical status and downstream ward capacity. Both of these are predictable, but teams do not have access to realtime bed information let alone bed forecasts.

#### Bed demand with COVID-19

Following the initial COVID-19 surge in Spring 2020, constrained ICU bed capacity is now widely recognised. The UK has fewer critical care beds than most: 6.6 per 100,000 compared to a median of 11.5 in Europe.[@rhodes] On March 17 2020, the NHS Senior leadership wrote to all NHS trusts on March 17, and asked them to "free-up the maximum possible inpatient and critical care capacity" (for COVID-19).[@Stevens 2020] This has had, as yet, unmeasured consequences for non-COVID healthcare. Early indicators suggest the pandemic has caused indirect harm through this re-allocation of resource.[@wise2020] A 'medical debt' has accrued whilst normal health care services have been diverted. The cost of this debt remains a modifiable part of the pandemic response. Efficient and effective allocation of beds following the initial surge, and during the ongoing pressures is key to making that modification and minimising harm. 

Future bed management will need to maintain separate 'blue' and 'green' (COVID positive and COVID negative) streams, and to be ready to flex up and down in response to future surges. This is going to be particularly true where pathways involve critical care. Realtime bed information and short-term demand forecasts are going to be even more important to maintain patient flow.  These enable the workforce by putting the information they need in their hands at the right time. Staffing can be flexed, patients forewarned, or schedules re-adjusted to improve efficiency.

#### Market plan
TODO: @Tim: need help here
NOTE: Phase 2 application aim: To develop prototypes and generate early clinical  safety/efficacy data towards CE marking
NOTE: I'd don't think we want to build and run a company. So the end game for this would be a decent enough application that it could be picked up and commercialised by someone else. I'd like to be explicit about this but not sure if that is the right approach.
TODO: INSERT THE FOLLOWING? D/W Sonya/Martin: We originally wrote this proposal to run over 26 months as this fitted with our local staffing and supervision model. However, given the urgency imposed by COVID-19, and the pressing need to find ways to improve patient flow, then we would be prepared to double the staffing allocated to the project and (nearly) halve the duration to 15 months. Please see the original and a proposed accelerated Gantt chart.

We have already built and deployed a prototype bed demand forecasting model. This has been deployed to predict bed demand for Great Ormond Street Hospital’s cardio-thoracic ICU since 2012. It produces a real time, hyper-local, 7-day forecast of bed demand. In 2018-9, we collaborated with University College Hospital’s digital platform team to (1)  generalise our model to work for any ward in a complex network of flows, and (2) start to adapt the technology for different levels of digital ‘readiness’. As per NHS-X strategies, the platform is interoperable, robust and scalable. We now seek support to update our prototype with state of the art ‘machine learned’ clinical features, and to generate the safety and efficacy data for deployment across the NHS.

The next stage prototype deliver the following:

1. A set of learned model coefficients that accelerate deployment with a smaller training data set at a new location.
2. An interface that permits adaption based on key local features
3. A robust software package for reliable deployment
4. A user interface that permits rapid adoption with minimal training needs for front line clinical staff

The target market is NHS acute hospital trusts. The application would be installed by the organisation, and then made available to all wards, including critical care, as well as the bed management and surgical pathway teams. Where digital maturity is such that HL7 or FHIR interfaces are not exposed, the application could be deployed to key wards such as critical care with direct (manual) data entry. 

We will work with UCL/UCLH technology transfer teams to develop the correct business model going forwards.

#### Existing product / experience

### Benefit to patients, the NHS and the wider population

Modelling bed occupancy and flow to improve operational efficiency has been a long term endeavour in the NHS. The health service is under intense pressure and 'coping but not coping' strategies (e.g. premature discharge, outlying medical patients on surgical wards, and negative feedback loops that reduce referrals) cause harm, reduce income, and increase strain elsewhere in the system.(E Wolstenholme, 2007)

Commercial bed forecasting models are typically derived in US markets (e.g. TeleTracking/HospitalIQ), poorly adapted to the NHS, and are simulation based. [TODO: before critiquing simulations, explain what they are]Simulations are unable to distinguish true demand from the mitigated demand derived from the 'coping but not coping' strategies.

Our approach brings three advantages. (1) We model actual demand not mitigated demand. (2) Our results are local (ward level) and real time rather than system level and strategic. This gives local teams the ability to make tactical responses, flex staffing and adjust schedules themselves. (3) We integrate with existing digital systems and use modern machine learning techniques to tune the forecasts to the available data and the local context.

Surgical cancellations are miserable for the patient, wasteful for the system, and can cause harm. But there is a greater opportunity. Current NHS strategy recommends running a hospital at 85% occupancy for maximum efficiency, and above 92% is regarded as a tipping point where flows from upstream services (A&E etc.) are impaired. High quality length of stay (LoS) and bed demand forecasts will allow us to move away from this 'rigid occupancy target' toward the equivalent of 'just-in-time' manufacturing processes. Patients with greater LoS can be identified to downstream health and social care partners earlier. And periods when such patients cause congestion in the system can be managed by pre-emptively adjusting the incoming elective case mix to favour a higher turnover/shorter stay cases.

## The Proposed Innovation

### Competitive advantage: 

We have built a hyper-local realtime bed demand forecast that generates ward level predictions of bed demand over the subsequent week.  We focus on predicting bed *demand* rather than bed *utilisation*; the latter is the more common AI or simulation task but less informative.  Discrete Event Simulation (DSE) is the approach adopted by the majority of existing commercial bed forecasting approaches (e.g. Teletracking & Hospital IQ, GE HealthCare's Digital Twin etc.) However, simulations can only describe observed behaviour.
We eschew predictions under the known strained network and evaluate the 'what might have been' (counterfactual) scenario to gain novel insights.  Specifically, *demand* predictions are upstream of the response, and create a window for intervention (changing discharge priorities, flexing staffing, re-organising schedules etc.). We also build a bottom-up (local) forecast that starts at with the ward rather than hospital. A simulation might be helpful to a the executive team planning bed flows through a new building. However, local forecasts that are placed in the hands of the ward team, surgical pathway coordinators, and theatre planners offer a chance to actually improve operational efficiency.

### Barriers to adoption: 
TODO: see existing list under market plan and discuss here
1. A set of learned model coefficients that accelerate deployment with a smaller training data set at a new location.
2. An interface that permits adaption based on key local features
3. A robust software package for reliable deployment
4. A user interface that permits rapid adoption with minimal training needs for front line clinical staff


## Patient & public involvement (end users involvement)
TODO: end users are hospitals and staff; can cite user centric design; 
TODO: letter of support from BRC? Alison Clements @ UCLH? or other UCLH staff?
TODO: ask @Sonya or @Martin for contacts/suggestions

## Detailed project plan

The research is organised in NN work packages (WP). Each is shown with the number of man-months (MM), the deliverables (D), risks (R) and mitigations (MiT) and milestones (MS). These are then mapped to the attached Gantt chart. Against each of these we have proposed success criteria for three different operational scenarios.

- **medical ward**: booking staff for the following shift
- **surgical ward**: calling patients up for surgery
- **critical care**: giving the go-ahead for surgery that requires ICU

Theses are intended to ensure the application development is focused on delivering achievable improvement in organisational performance, and therefore define the product characteristics.

### Aims and objectives

#### Need
TODO: cite justifications for our approach here (1) demand (beds/staff/side rooms) (2) local use and local data capture (3) digitally adapted

Admissions in NHS hospitals are managed by individual 'pathway' teams (e.g. colorectal surgery, orthopaedics etc.). These decisions are made without sight of their impact on patient flow both locally (on that pathway) and more widely on the hospital. This results in congestion, on-the-day cancellations, premature discharges, stretched staffing patterns and potential patient harm. Where bed forecasts are performed, they are rarely done at the ward level. The appropriate information is then not in the hands of the local decision maker generating a 'learned helplessness' wherein staff assume that patient congestion is not something over which they can exert control. 

#### Aim 
TODO: rewrite para specifcally starting from existing opportunity
TODO: ? levels: hand entry as per existing app / HL7 /FHIR
ASK: Sonya/Martin: can we rebuild the model so that it estimates demand for resources other than beds. For example, if we conceptually subdivided the beds within a ward into groups based on nursing intensity, and then saw the patients moving between those 'subwards' then is it possible we could then recover the nursing demand. Ditto if we divide the wards into open bays and siderooms to account for infection control.

We will generate real-time, hyper-local (ward level), short term forecasts of bed demand. These will be provided within a modular application that adapts to the digital maturity level of the host organisation, presents an EHRS agnostic interface, and allows extensions to manage COVID-19 related issues. Specifically, we will extend the model to forecast staffing demand, and demand for isolation beds.
The same forecasts will be visible by the hospital bed management team allowing informed negotiation, and better use the constrained bed resource. 

#### Objectives
TODO: revisit when you have done the details on the work packages

- extension of the model to use generic inpatient level administrative and clinical features (e.g. demographics, clinical speciality, laboratory measures)
- an evaluation of the performance of the model across of a range of common scenarios (e.g. different wards, different prediction horizons, different demand scenarios)
- a piece of software the incorporates the existing model but hardened to meet state of the art standards for reliability and interoperability (e.g. code coverage, continuous integration, FHIR/HL7 interface etc.)

We will refactor the application to separate the forecasting model from the interface from the data presentation
- the *data presentation* layer will allow hand entry, HL7, and FHIR interfaces
- the *modelling* layer will be run with a minimum feature set that can be expanded based on the data presented
- the *user interface* layer designed to support decision making built built as a separate module that can support the model but could be swapped out for interfaces provided by existing clinical information systems

TODO: green and blue pathways
We will upgrade the AI component of the model
- We will develop model features that are appropriate for the COVID-19 pandemic response
- forecasts that incorporates infection control constraints
- forecasts that respond to levels of pandemic readiness (TODO: change
  incoming stream to reduce LoS for rapid step-up/down)

We will perform user testing
- We will prepare a quality management file ...

### Individual work packages

The project plan below serves two purposes
- itemising the work therefore justifying the cost and the timeline
- explaining the product features and design decisions
The grant funds two 'workers' (2FTE), a 4 person project team (0.7FTE in total), plus consultancy support. The first 'worker' (W-AI) is a post-doc who will update and extend the AI model, and will be supervised by SC/MU/KI (UCL CORU and IHI). The second worker (W-SE) is a *s*oftware *e*ngineer from UCL's Research Software Engineering (RSE) team supervised by SH/JC with consultancy time supporting Quality Management and Health Care design.

#### WP-1: Governance / PPI / Set-up
With respect to research governance, we will divide the project into two components. The first will develop the forecasting application itself. We have already sought confirmation from UCLH Joint Research Office that this component does not require Research Ethics Approval as per HRA guidance. The second will build a pseudonymised training data set, and develop and update the AI component of the forecasting models. Methodological innovation here would constitute research, and we will therefore seek HRA/REC approval for this component. 

- **Staff**: The majority of the team already have UCLH Honorary Contracts and access to the EMAP data science platform (TB/SH/SC/KL). New team members will require the same.
- **Compute**: We order and install a project specific GAE (Generic Application Environment) for the team. This is a component of the EMAP platform: a Linux based Virtual Machine designed to host Dockerised Applications within the NHS environment. Dockerisation of the application infrastructure permits rapid deployment to new environments, and is the recommended solution for application development at UCLH.
- **Data**: We will gain approvals through the UCLH Clinical Research Informatics (CRIU) Data Access Committee to work with identifiable patient data for the purposes of building this application.

###### Success criteria
- Staff: All with Honorary contracts and IT access
- Compute: Virtual Machine (GAE) deployed; Web server accessible on the UCLH network via HTTPS
- Data: Access to EMAP ‘User Data Store’ including full HL7 ADT stream from April 2019 
###### Application Milestone
- N/A
###### Model Milestone
- N/A 
###### Man months
- 1 month but up to 3 months elapsed time
###### Risks and mitigation
We are very much aware that hiring, equipment installations and governance approvals can take much longer than anticipated. 
Once funding is confirmed we will immediately appoint W-AI/W-SE and seek approvals as per the existing team. Ideally, we will draw on existing internal resource from the group since approvals would already be in place, and the team has existing experience with the application. This would accelerate our timelines. We are also confident data access will be approved. We enclose letters of support from Professor Bryan Williams, Director of UCLH/UCL Biomedical Research Centre, and have previously had successful access for earlier work (Wellcome ISSF ED network flow modelling, Health Foundation Critical Care patient monitoring). 

#### WP-2: Application foundation

##### Overall approach
TODO: Comment on - local data capture (tuning) via interactive UI; Early prototype to floor; Simplest possible model to start with; Display ‘now’ and ‘next’

Our current application has been written in several parts over several years.

1. A length of stay prediction model implemented in VisualBasic and calibrated for the Cardiothoracic ICU at Great Ormond Street in 2012. The model uses Classificaion and Regression Trees (CART) which were an appropriate choice given the technology in 2012, but have now been superseded. Moreover, the model used a very limited set of features since data entry was done by hand into an Excel spreadsheet.
2. An Excel spreadsheet that is linked to the VisualBasic application and is used for data entry, and reporting.
3. A non-Markovian network model implemented in Python in 2018. This is an academic proof of principle but the code is not mature (poor code coverage, no testing framework etc.) However, the model is broadly generalisable since it learns from the patients 'journey' through the hosptial, and requires no clinical features. The model currently interfaces directly with the EMAP platform at UCLH that exposes the continuously updating HL7 ADT (Admission-Discharge Transfer) stream as an input. Outputs from this model are available to the development team (R or Python interface) but not to the end user.

Going forwards we see flexibility in the deployment environment for the application as a priority. We imagine the following scenarios/user stories:

- *Low digital maturity (HIMMS 2-3)*: Data is hand entered into a web application by a ward administrator. Existing patients and planned admissions are captured with a lightweight feature list (e.g. age, surgical procedure complexity, emergency status). The forecast is run and used locally only. This mimics the current implementation at GOS.
- *Middle digital maturity (HIMMS 4-5)*: Data is supplied through an automated interface (e.g. a SQL query, an HL7 feed, or a FHIR API) but the hospital lacks an integrated electronic health record system (EHRS) so a full clinical profile is not available. The application therefore automatically updates, and is availble for any ward across the hospital.
- *High digital maturity (HIMMS 6-7)*: The application is embedded in an institution with an integrated EHRS. A full range of administrative and clinical information is automatically available for any ward across the hospital. The output may be returned and displayed within the EHRS.

We will therefore refactor the application into modular components.

- a *data interface layer*: permits hand entry, HL7, FHIR and SQL interfaces etc.
- a *modelling layer*: that will run with a minimum or enhanced clinical feature set depending on the level of digital maturity
- a *presentation layer*: that will be display the forecasts as a web app but does so by querying the modelling layer using a RESTful API, and therefore can be replaced with other presentation tools

In the process, we will rewrite refactoring of code base (currently in Python without unit tests, functional testing etc.). We  propose switching to Java Hibernate framework and achieve alignment with MDR regulations for decision aids in healthcare)

##### Minimal Viable Product
Each development cycle deploys the application and the model, and then works with operational and clinical end users to build outputs that provide insights to better manage flow. The objectives of WP1 are foundational and put the application in the hands of users within 3 months. This user-centred design approach optimises the chance of the product delivering on its promise.

1. Generate the basic structure of the application to allow iterative user testing and development (build-test-learn)

The existing application runs in an Excel spreadsheet. This precludes use of modern ML techniques, realtime updates, or managing data at scale. But it does allow direct user interaction, and is a tool that all staff understand. Developing in practice rather than theory by iterating from the Excel sheet to a basic web application will generate an application that is actually ‘used in practice’ rather than one that is more perfect in theory. This will be the foundation for all future user development, will allow local data capture (see below), and be the default for less digitally mature environments.
	
2. Build in a process for ward level data capture and updates

AI solutions need to learn from their environment, but they can only learn if they have the right data. The most valuable data is local knowledge or ‘end of the bed information’. For example, your model might use EHR data to predict that a 65 year old recovering from hip surgery will have an expected LoS of 10 days. A nurse might look at a patient and realise that this patient is ‘flying’ and will be discharged in 5 days. We will build ‘data-updating’ into the application from the outset. This might capture local estimates (e.g. LoS) or specific attributes that affect flow (infection control status, discharge blockers such as need for social care packages).

 
##### Success criteria

- **medical ward**: booking staff for the following shift
    - nurse-in-charge uses the application to estimate demands for staff over the next few days
- **surgical ward**: calling patients up for surgery
    - pathway coordinator uses the application to share information with the ward team about future admissions
- **critical care**: giving the go-ahead for surgery that requires ICU
    - nurse-in-charge uses the application to estimate demands for bank staff over the next few days
    - theatre coordinating team use the application to access data on available beds for the following days theatre cases requiring critical care


##### Application milestone
NOTE: what you’d see if you stopped the project at this time

A web application accessed by a ward desktop computer hosted on a hospital server with user access management, and appropriate security.

The web application shows
- a list of current patients
- a list of expected admissions by day over the next week
	- for a surgical ward these would be named patients (and procedures) and unnamed ‘emergencies’
	- for a medical ward these would be unnamed ‘emergencies’
The list is populated by hand and contains nothing more than patient identifiers (hospital number etc.), date of admission (or expected date of admission for expected admissions), and expected length of stay (LoS). This generates a deterministic view of future bed status.
NOTE: LoS predictions simple ward level mean (not modelled); Users interact to correct data and adjust predictions (LoS)

##### Model milestone: 
TODO: Note that there is no AI modelling work in this package but need to develop the patient data model AND the ward data model; need to standardise these and lay foundations for thinking about wards having components (side rooms) so not all beds are the same
TODO: Data model needs to be an interpreted view of electronic model so updates persist but don’t need to be fed back into the EHR 
NOTE: what the AI component looks like at this stage

The forecasting model is deterministic at this stage. The data model is refactored to a generic FHIR aligned schema (person, encounter observation etc.)[@ref: FHIR]. At this stage the model captures patients in ‘time and place’ but each each patient is indistinguishable with the same expected LoS (the average for a patient in that ward). However, the users would be expected to tune this using the interaction piece described in (2) above.

##### Man months:
- RSE: 3-6
- AI: None? Some work re-factoring the model

##### Figures
- CORU Excel app
##### Refs 
- https://en.wikipedia.org/wiki/Test_and_learn
- https://www.hl7.org/fhir/resourcelist.html

TODO: importantly remember that there is information (learning) in the interaction with the model: this is not a one way flow of info: i.e. the users see the LoS predictions and validate them; the validation becomes part of the model input
	- LoS validation capture
	- Key criteria that affect individual patient movement (sticky patients b/c infection or difficulty in placement); not all patients are equal
	- staffing constraints

#### WP-3: Application integration
TODO: discuss data that are available; duration; generalisability; how to update; need to update
TODO: see if you can find another site for collaboration (Ari, GOSH?): Letter of support
TODO: @ask Ken: would this be a suitable application for transfer learning; imagine seeing a new ward with new LoS predictions to be generated; then we use the existing learning to accelerate LoS predictions in the new ward
TODO: importantly remember that there is information (learning) in the interaction with the model: this is not a one way flow of info: i.e. the users see the LoS predictions and validate them; the validation becomes part of the model input
	- LoS validation capture
	- Key criteria that affect individual patient movement (sticky patients b/c infection or difficulty in placement); not all patients are equal
	- staffing constraints
TODO: add note about correcting errors from (e.g. if truth is always automated and electronic then errors propagate)
TODO: make a big  deal about the importance of ongoing hand data entry to capture those features that the local team thinks are important (e.g. tracheostomy, social issues, infection control, 1:1 nursing requirement); you may like to revisit this in the UI part of the work packages
NOTE: Just-in-time (JIT) current state
NOTE: hand entered data and model above collates ‘known’ information into one place. But relies on hand entry. Most clinical teams use ward white boards for current state and excel for future state (bookings) and have only intuition to describe unplanned future state. This stage now brings in feeds of data and implements the existing models in real time.

Normalised trainng data is already available at UCLH from April 2019 giving a full year of seasonal variation, and capturing the first COVID-19 surge. Data from previous years is also available, and will

Deliverables
- HL7/FHIR interface for admissions/discharges/transfers to a particular ward (medicine/surgery/critical care)
- HL7/FHIR interface for future bookings (surgery/critical care only)

##### Success criteria

- **medical ward**: booking staff for the following shift
    - accurate current bed status; corrections trivial to make; users choose to use this system to see current and view future bed state over other visual displays of bed status
    - nurse-in-charge uses bed *demand* predictions to *negotiate* additional staff for the following day
    - dashboard reports staff-to-patient ratios
    - inverse correlation between demand and staff-to-patient ratios
- **surgical ward**: calling patients up for surgery
    - pathway coordinator uses the application to share information with the ward team about future admissions
    - pathway coordinator uses the application to identify opportunities to flex-up/down bookings, or adjust short/long stay case mix to maximise theatre time/surgical capacity
    - nurse-in-charge uses bed *demand* predictions to *negotiate* additional staff for the following day
- **critical care**: giving the go-ahead for surgery that requires ICU
    - nurse-in-charge uses the application to estimate demands for bank staff over the next few days
    - theatre coordinating team use the application to access data on available beds for the following days theatre cases requiring critical care
    - theatre coordinating team move their planning bed planning discussions forward by 12-24 hours

##### Application milestone
A web application accessed by a ward desktop computer hosted on a hospital server with user access management, and appropriate security. The application now interfaces directly with the hospital Patient Administration System (PAS) using FHIR/HL7, and is populated in near real time. A patient-centric data model is then available for update by the end user, to feed the AI component of the system.

The web application shows a 'just-in-time' view of the current and future bed status
- a list of current patients
- a list of expected admissions by day over the next week
	- for a surgical ward these would be named patients (and procedures) and unnamed ‘emergencies’
	- for a medical ward these would be unnamed ‘emergencies’
The list is automatically populated, but can be edited by hand (corrections, capture of additional salient features). The future view of bed status is now probabilistic rather than determinisitic (see Model milestone below). Manual data entry is still possible as per WP-2.

##### Model milestone
NOTE: what the AI component looks like at this stage

The forecast models from the existing application (LoS, non-Markovian network) are now re-deployed on the foundational infrastructure above. The existing length of stay model is deliberately simplified. It uses a narrow range of administrative features that will be common to any NHS ward (e.g. simple administrative data including but not limited to age, source of admission, operative urgency, ward type).
The ward level length of stay (LoS) model can be deployed as single ward solution for low digital maturity environments. The model predicts individual LoS then aggregates to estimate future bed demand. In more digitally mature environments, where hospital wide data are available, these LoS predictions these now feed into the non-Markovian network model and modify the ward-to-ward transition probabilities.  Both models produce short term probabilisitc forecasts of bed occupancy.
The ward level data captured from WP-1 is now both an input to the model, and a layer that updates the patient level predictions before reporting. Specific examples might include
- The LoS prediction estimates a future LoS for an individual patient at 2 days. The ward team know the patient is being discharged tomorrow (i.e. in 1 day). They correct the expected discharge date. This correction feeds forward to reduce the predicted occupancy by one patient in two days. The correction is stored as a patient specific feature so that the local training data is enriched.
- The application is deployed to a critical care unit. Patients who are confused or agitated are labelled as a 'falls risk'. Such patients are provided with health care assistant who to sits at the patient's bedside. Finding this additional staffing resource often delays discharge. The web application allows the ward team to label patients as a 'falls risk'. This feature is then fed into the model which learns the association between 'falls risk' and delayed discharge, and propagates that learning forward.

###### Man months
- W-SE: 6 months: HL7 (+FHIR) interface building; providing an API for the modelling inputs/outputs
- W-AI: 3 months: Re-training the existing models on generic administrative + local ward level data; refactoring code to produce PMML compliant models[@ref: http://dmg.org/pmml/v4-3/GeneralStructure.html]
###### Figures
###### Refs



#### WP-4: Upgrade AI component of the model
TODO: model and SoA ML
TODO: model and transfer learning
TODO: model upgrades - staffing: the trick here is think about staff demand instead of bed demand: that is rebuild model to predict nursing demand! this can be captured from clinical characteristics
TODO: model upgrades -  infection control: again the key here is to predict demand for bed types

We will augment model 2 with the clinical features that were used to construct model 1 but update that model using modern machine learning techniques that handle wider ranges of time-fixed and time-varying inputs (deep neural nets, and Long Short Term Memory networks for time-varying features etc.) We will explore the use of a wider range of clinical features (demographics, clinical specialty, labelled structural descriptions of hospital infrastructure, vital signs and clinical laboratory data), and we will ensure that the models are performant at varying levels of digital maturity.

Special attention will be paid to two specific sources of information that will affect capacity.

##### WP-x: Application user design

> Rapid Iterations of Prototyping and Testing
> "User-centered design (UCD) is an iterative design process in which designers focus on the users and their needs in each phase of the design process. In UCD, design teams involve users throughout the design process via a variety of research and design techniques, to create highly usable and accessible products for them"


TODO: incr budget for designer
TODO: Need to justify why the output of the model is important
What do people need from it and what will be the actionable reports/components
TODO: Use analogy: what do people do with the information from a weather forecast ?take an umbrella: what are the actionable piece of information; likely to vary from scenario to scenario; and who is the decision maker
	- ward team who can manage staff
	- pathway coordinator
	- bed manager (places?)
	- consulting surgeon: defines clinical priority
TODO: define relevant KPI: can you report and show occupancy and LoS; can we then convert these into a game that the team trys to optimise
	- nurse to patient ratios : less variation and better optimised
TODO: 

- design-led user interface development
- deployment and evaluation of core model
- deployment and evaluation of enhanced model
- IP and commercial evaluation  


References
- hhttps://www.interaction-design.org/literature/topics/user-centered-design
- [The Four Fundamental Principles of Human-Centered Design and Application](https://jnd.org/the-four-fundamental-principles-ofhuman-centered-design/)

#### WP-x: Model evaluation
TODO: make it clear that this wil be part of the ongoing work; in the Gantt chart it should run all the way through
TODO: work with other sites

Model evaluation, safety and reliability data
Comparison against existing models in general use
Each testing cycle deploys the model, and then works with operational and clinical end users to build outputs that provide insights to better manage flow

#### Define early success criteria

Criteria
- pre-forecasting success: just timely information available to all users of the *current* state: i.e. who is in what bed at what time
- can you fix the 9am bed meeting so that firstly it runs the evening before; then iteratively move that forward

- Milestone: Completed user facing validated software application
- Risks&Mitigation: 
	- User interface design experience: In-house team Royal College of Art Health Care design team



#### WP-x: Model extensions for COVID-19

Extension of the model to include staffing/resource constraints wherein current models understand limitations with respect to physical capacity but often staffing/resource is the more important functional limitation.

- Milestone: Deployment of model with staffing module
- Risks&Mitigation: 
    - Data access & Electronic Staff Record access already in use by partner at UCLH
    - Mathematics & CORU world leading Operational research unit with decades of experience in this field 

TODO: explain in detail about how the ESR can be used to calibrate from user interactions
TODO: use staff/resource constraints as an example of capturing different information but make this about building an API for the ‘model’

#### WP-x: Quality Management process

Update existing network model software to align with ISO 25010:2011 principles (Reliability/Efficiency/Security/Maintainability); ensure interoperability at varying levels of digital maturity (HIMSS 0-7) using HL7 v2.3+ and FHIR. Initiate Quality Management System (QMS) and Medical Device Regulation compliance

- Milestone: Deployment of model with FHIR API
- Risks::Mitigation: 
	- QMS experience : New partnership with WEISS centre at UCL
	- Software experience ::Existing partnership with UCL Research Software Engineering team 

## Hurdles
TODO: ?enumerate the hurdles here but explain in detail above

## Risks and mitigations
TODO: enumerate the risks here but explain in detail above

## The Team
TODO: explain how the team has worked together before
TODO: perhaps provide a timeline of the work we have done to date

NOTE: Describe the existing research support (e.g. funding from other sources) available to the research team, which is relevant to this proposal. Clearly delineate the proposed project from other related research, funded from another source.

###Specify the role of the lead applicant

## Finance analysis
TODO: details of the company's cash flow etc
TODO: justification of the costs (see Appendix 2)

## Patient data use and monitor of patient safety
NOTE: Describe any known limitations of the data used and algorithms deployed by the AI solution. Include an ethical examination of how the data would be used, and how it would comply with the AI Code of Conduct. Explain how the product’s performance would be validated and how it would be integrated into health and care provision. Demonstrate that security of the data is integral to its design.  Please include details of how you will monitor and report patient safety or data issues, including any recovery plan.

## Ethics and regulatory approvals
NOTE: Outline any ethical issues associated with this research and the arrangements for handling them. If there are no plans to obtain ethical review, this must be clearly justified. Note that work outlined in your application must adhere to the UK Framework for Health and Social Care Research.

## Intellectual Property (IP) and commercialisation strategy
NOTE: All background and any potential foreground IP arising from the project must be described in the application. An initial freedom to operate opinion must be provided, referencing any third parties’ rights which may affect the implementation of your device or technology. A strategy should be proposed for how third party rights will be managed to allow for further development, implementation and commercial exploitation. Provide details of any new types of IP that may arise during the project, including ownership arrangements and management of the IP.
NOTE: IP arrangements between collaboration partners, and with consultancies and sub-contractors must be regulated by appropriate agreements. The Lambert Toolkit provides model agreements for collaborations between universities and companies.
NOTE: Please include details of the intended market, barriers to entry, and competitor analysis as well as details of your sales strategy/channels and marketing plans. Include a pricing strategy. Provide any details of market traction, interested customers and their potential value for the company, and/or any income already being generated. Market opportunities, both domestic and global can be explored.

TODO: IP from existing forecasting model (background) and future (foreground)
TODO: IP from HL7 interface (background) and FHIR (foreground)

## Dissemination and NHS adoption strategy
NOTE: Please describe the planned outputs of the research and how they may lead to short and longer-term NHS and patient impacts. As far as possible, indicate anticipated timescales for these benefits and a quantitative estimate of their scale. Impacts may include, but are not restricted to - patient benefit; healthcare staff benefits; changes in NHS service (including efficiency savings); commercial return (which could contribute to economic growth); public wellbeing.
NOTE: Describe how the outputs of the research will be communicated and to whom. Identify key stakeholders, and your plans for engaging them. To realise impact, it is unlikely that simply making outputs available will be sufficient. Please consider and outline the active approach you will take to engaging key parties to disseminate the work.
NOTE: Present a specific strategy for adoption of the technology into the NHS. Describe the process by which the technology will enter the healthcare environment, including how your solution will be acknowledged, selected and introduced for use in the health and care service or wider society. Detail what current and future barriers to adoption are likely to be encountered, and a strategy for overcoming them. Where possible, consider how your solution will be adopted and implemented longer term, and what efforts and investment are likely to be needed beyond the project to achieve widespread NHS adoption.



# Other supporting roles - signatories

# Director of finance signature against the declaration

# 

