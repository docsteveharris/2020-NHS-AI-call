# Background details

TODO: complete online; no specific prose needed here

# Plain English Summary (450 words)

More than 1000 patients have elective surgery cancelled every week in the NHS, causing anxiety for patients and families.(D Wong, 2017) Cancellations are upsetting, inefficient, may cause harm, delay treatment, and let slip therapeutic opportunities. Bed capacity is the primary reason for these cancellations. Yet bed capacity fluctuates. Operational efficiency depends on an accurate view of near-future demand, but this is challenging because a hospital is a complex system with many interdepartmental flows, and individual emergencies seem unpredictable.

This challenge can be met by operational modelling combined with Artificial Intelligence. In 2012, we built a demand forecasting solution that supports operational teams to reschedule elective surgery and reallocate resources to avoid last minute cancellations and bed shortages. We deployed and customised this for a single ward: a  cardio-thoracic critical care unit at Great Ormond Street Hospital.(C Pagel, 2017).

However, that technology could not be scaled, nor readily adapted to work in different institutions. In 2018-19, in partnership, with ‘INFORM’ (a translational data science team at University College Hospital), we generalised the underpinning mathematics of the solution and built a prototype that could scale.

Our approach is distinct from most bed modelling approaches in that we deliver forecasts that are local (ward level), and near future (over the next week). Unlike most other bed forecasting models, we predict future *demand* not future bed *utilisation*. Bed utilisation is best thought of as *demand* already mitigated by *actual supply*. More simply, we are interested in bed demand *before* not *after* cancellations have occurred. 
This creates a window for local teams to better use their existing bed capacity by flexing staffing levels, or rescheduling surgical operating lists. More importantly, local teams are enabled to innovate: to find local solutions to predicted bottlenecks and to better use their existing bed capacity. 

We now seek support to

1. Upgrade the AI component of the model so that it can learn from a wider range of patient clinical characteristics (lab results, clinical history, vital signs etc.) 
2. To extend the mathematics to include staffing and infection control constraints that must also influence bed availability. 
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

NOTE: OBJECTIVE AS PER PHASE 2: To develop prototypes and generate early clinical  safety/efficacy data towards CE marking
TODO: drop the part that talks about EMAP and FHIR since it's overambitious to build this within the project

## The opportunity

### NHS unmet clinical need and market plan

NOTE: Please also provide a description of how your AI solution will support the NHS Long Term Plan, NHSX strategic priorities and/or wider government priorities including the Industrial Strategy grand challenges or resource efficiency. Please report market size, any related trend or forecast, patient population affected, NHS cost burden, and state of the art.
NOTE: relevance to priorities and needs of the NHS, cite the NHSX documents

We submitted the Expression of Interest for this call on 4 March 2020. On 11 March 2020 the WHO declared COVID-19 a global pandemic. The need for an effective tool to forecast hospital bed demand, and provide reliable, ward level forecasts was pressing when we made the original application. It is even more pressing now. There is no future where NHS capacity is plentiful. Even if we can build temporary hospitals, we cannot instantly train new staff and expand the workforce overnight. Instead it is imperative that we better manage our existing resource, and make the system as efficient as possible. 
Above all we must remember that the problems of bed supply and demand were increasing even before COVID-19. Between 2010 and 2019, NHS bed capacity fell by 10.1%, and bed occupancy levels rose from 85% to 90%, with corresponding knock-on effects in waiting times for A&E, for cancer and for surgery.[@NHS Key Statistics briefing paper 2020]

#### Bed demand prior COVID-19

In 2018, we found in 245 NHS hospitals that on average 10% of surgical admissions had been previously cancelled (more in hospitals with fewer ICU beds, and more emergency work).[@Wong 2018] This amounted to 25,475 operations being cancelled on the day of surgery in just one 3 month period in 2018 (NHS-England): the highest number in two decades. The following winter, NHS-E recommended that all elective surgery be cancelled in January to avoid a repeat.[@Gillies 2018] 
Despite these pressures, NHS operating theatres are often labelled inefficient. In our own hospitals, patients, surgeons, scrub nurses and  anaesthetists are all ready to go from 730am. However, major surgery does not start until after the daily 9am ‘bed meeting’ that reports whether ICU beds are available for high risk surgery. These ICU beds depend on discharges from ICU to the ward. In turn, this depends on clinical status and downstream ward capacity. Both of these are predictable, but teams do not have access to realtime bed information let alone bed forecasts.

#### Bed demand with COVID-19

Following the initial COVID-19 surge in Spring 2020, constrained ICU bed capacity is now widely recognised. The UK has fewer critical care beds than most: 6.6 per 100,000 compared to a median of 11.5 in Europe.[@rhodes] On March 17 2020, the NHS Senior leadership wrote to all NHS trusts on March 17, and asked them to "free-up the maximum possible inpatient and critical care capacity" (for COVID-19).[@Stevens 2020] This has had, as yet, unmeasured consequences for non-COVID healthcare. Early indicators suggest the pandemic has caused indirect harm through this re-allocation of resource.[@wise2020] A 'medical debt' has accrued whilst normal health care services have been diverted. The cost of this debt remains a modifiable part of the pandemic response. Efficient and effective allocation of beds following the initial surge, and during the ongoing pressures is key to making that modification and minimising harm. 

Future bed management will need to maintain separate 'blue' and 'green' (COVID positive and COVID negative) streams, and to be ready to flex up and down in response to future surges. This is going to be particularly true where pathways involve critical care. Realtime bed information and short-term demand forecasts are going to be even more important to maintain patient flow.  These enable the workforce by putting the information they need in their hands at the right time. Staffing can be flexed, patients forewarned, or schedules re-adjusted to improve efficiency.


*Alignment with NHS/NHS plan and priorities*: Optimising management of inpatient resource, specifically bed capacity, is key to delivering the NHS Long Term plan. Beds, and by definition, are a hospital's most precious resource. It absurd that in 2020, major teaching hosptitals with budgets in the hundreds of millions providing thousands of surgeries, manage their patient admissions with Excel spreadsheets and 'huddles' the day before surgery. Despite the good will, the enthusiasm, and the considerable talent brought to this process, it cannot be efficient if the teams are not provided with both a view of the 'now' and a meaningful prediction of the near future. Supermarkets, airlines, postal services do not wait to see how many products are sold, tickets booked, or parcels sent. These flows can be forecasted, and then resources saved or augmented as demand requires.
NHS-X has rightly called out that the process for translating prototypes into products, and seeing Digital Health Technlogy (DHT) scale has been a blocker to innovation. The existing application is a case in point. Even in 2012, no one would have developed an modelling tool in Visual Basic to run in an Excel spreadsheet. It is not only limiting, but almost impossible to meet the technology and interoperabilty standards outlined in the NHS Digital Health Technology Standard.[@NHS DHT Feb 2020] However, it was a sensible and pragmatic choice, that led to the application actually being used. This proposal is simply seeking to combine an update of the AI component, with a programme that meets these standards. In doing so, we will be enabling the NHS-X mission to 'reduce the burden on our workforce', and 'improve health ... productivity' with digital technology.[@https://www.nhsx.nhs.uk/about-us/what-we-do/]

#### Existing product / experience

### Benefit to patients, the NHS and the wider population

Modelling bed occupancy and flow to improve operational efficiency has been a long term endeavour in the NHS. The health service is under intense pressure and 'coping but not coping' strategies (e.g. premature discharge, outlying medical patients on surgical wards, and negative feedback loops that reduce referrals) cause harm, reduce income, and increase strain elsewhere in the system.(E Wolstenholme, 2007)

Commercial bed forecasting models are typically derived in US markets (e.g. TeleTracking/HospitalIQ), poorly adapted to the NHS, and are simulation based. [TODO: before critiquing simulations, explain what they are]Simulations are unable to distinguish true demand from the mitigated demand derived from the 'coping but not coping' strategies.

Our approach brings advantages to the end user, and to the organisation. For the end user, (1) we model actual demand not mitigated demand. (2) Our results are local (ward level) and real time rather than system level and strategic. This gives local teams the ability to make tactical responses, flex staffing and adjust schedules themselves. For the organisation, the system can installed on to HL7 integration engines that are found in all NHS hospitals. These integration engines process messages from disparate electronic systems including the Patient Administration System (PAS) and laboratory orders and results. Hence even in organisations where FHIR interfaces are not yet exposed, it is possible to build a fully electronic bed forecasting system for administrative and laboratory data.

This brings benefit to the surgical patient otherwise suffering on-the-day cancellation. But there is a also a greater opportunity. Current NHS strategy recommends running a hospital at 85% occupancy for maximum efficiency, and above 92% is regarded as a tipping point where flows from upstream services (A&E etc.) are impaired. High quality length of stay (LoS) and bed demand forecasts will allow us to move away from this 'rigid occupancy target' toward the equivalent of 'just-in-time' manufacturing processes. Patients with greater LoS can be identified to downstream health and social care partners earlier. And periods when such patients cause congestion in the system can be managed by pre-emptively adjusting the incoming elective case mix to favour a higher turnover/shorter stay cases.

## The Proposed Innovation

We have built a hyper-local realtime bed demand forecast that generates ward level predictions of bed demand over the subsequent week.  We focus on predicting bed *demand* rather than bed *utilisation*; the latter is the more common AI or simulation task but less informative.

The bed demand forecast exists in two forms: (1) a model that uses patient level characteristics but cannot learn or be readily adapted to new settings; (2) a non-clinical model that extends to networks of wards and generalises to new settings. We now are now ready to combine and surpass the best of these two approaches in a new partnership of:

- the UCL operational researchers that developed the mathematics used in the forecasts and that have expertise in working with clinicians and managers to specify and deliver predictive tools that fit with clinical and operational realities, led by Dr Sonya Crowe. More specifically, we propose to extend the mathematics of the existing forecasting approach to
    - forecast demand in terms of staffing units rather than beds
    - forecast demand adapted for infection control requirements (e.g. for side rooms) with particular note to the current COVID-19 response
- a machine learning team led by Dr Ken Li at the UCL Institute of Health Informatics who will re-work the CART (regression based) predictions in the first model to use deep neural nets for continuously updating length-of-stay predictions

TODO: insert summary of Ken's notes here

- a clinical informatics team at University College London Hospital led by Dr Steve Harris that have built infrastructure to permit deployment of the application at varying levels of digital maturity (HIMSS Levels 0-7 using HL7v2.3+ and PAS systems and FHIR and EHRS systems)

### Competitive advantage: 

Our competitive advantage comes at three levels

1. Embedded joint academic-clinical team
2. Modelling strategy
3. Digital infrastructure (EMAP)

#### Joint academic-clinical team
We are a team of clinicians (SH/TB) who have built and deployed a realtime data science platform at UCLH (EMAP). We have a long standing collaboration with UCL's Research Software Engineering team, and the highest commitment to sustainable and robust software development practices. We have worked with UCL's Clinical Operational Research Unit (SC/MU) for several years. CORU have extensive experience in both methodological innovation for operational research, and embedded clinical problem solving (e.g. the 'modeller' in residence programme). This joint working means that we can meet the standards in the NHS DHT draft (e.g. fit for purpose, clinically safe, compliant wiht open standards etc.)

#### Modelling strategy
Discrete Event Simulation (DSE) is the approach adopted by the majority of existing commercial bed forecasting approaches (e.g. Teletracking & Hospital IQ, GE HealthCare's Digital Twin etc.) However, simulations can only describe observed behaviour.
We eschew predictions under the known strained network and evaluate the 'what might have been' (counterfactual) scenario to gain novel insights.  Specifically, *demand* predictions are upstream of the response, and create a window for intervention (changing discharge priorities, flexing staffing, re-organising schedules etc.). We also build a bottom-up (local) forecast that starts at with the ward rather than hospital. A simulation might be helpful to a the executive team planning bed flows through a new building. However, local forecasts that are placed in the hands of the ward team, surgical pathway coordinators, and theatre planners offer a chance to actually improve operational efficiency.

#### Digital Infrastructure (EMAP)
Over the last two years, UCLH has not only acquired a fully integrated Electronic Health Record System (Epic EHRS), but we (SH/TB/JC) have built a real-time data processing platform (EMAP) that exposed the information in the EHRS and other systems for research and innovation. This has been done with modern digital standards at its core. HL7 message streams are parsed, data is normalised to the OMOP Common Data Model, and FHIR aligned applications are on the roadmap for 2020. This means that we can move rapidly from concept to prototype, and indeed we were able to deploy CORU's non-Markovian model for the ICU at UCLH in less than a month.
In contrast with most digital innovation scenarios, we can guarantee that *both* the data and the infrastructure are available from the first day of the project. This removes the usual delays that are assocaited with gathering, cleaning and organising data before AI models can be brought to bear. EMAP exposes admission/discharge/transfer updates within 5 minutes of their being entered into the EHRS. The updates are granular (bed level), and trust wide.
Through the Clincial Research Informatics Unit (CRIU) at UCLH, we have an excellent working relationship with the the EHRS team. This will permit us to bring other clinical data streams to bear on the AI task. 

### Barriers to adoption: 
TODO: !!! 2020-05-18
TODO: see existing list under market plan and discuss here

## Patient & public involvement (end users involvement)

### End users
The application will be used by NHS ward staff (sisters and charge nurses, ward managers, pathway coordinators, theatre coordinators, bed managers and consultant medical and surgical staff). We have a long history of *end user* engagement. The original model was developed under the auspices of the 'modeller in residence' programme by SP/MU at GOSH. This was a collaborative programme that involved both observation, prototyping, and feedback. 
At UCLH, we have similarly good relationships with the same teams. We ran a workshop with more than 50 attendees from clinical, academic, and management teams describing the ambition to deliver a forecasting application here. We (SH) was a member of the programme board for the Coordination Centre, and we maintain a close working relationship with UCLH's Director of Operations (Clements).
We have orientated the project to follow the principles of 'user centred design', and allocated significant resource to gather information on the needs and requirements of end-users from the outset. This will keep our DHT focused on delivering relevant operational benefits (as per recommendation 2 of NHS DHT standard).[@NHS DHT]

### PPI and data
The effects of the application, and the research performed, have important but indirect effects on patients. We recognise that use of NHS data must have an 'explicit aim to improve health ... or the operation of the NHS'.[@NHS data guiding principles, Principle 1] And we recognise that whilst the effect is indirect, PPI in the project will be important with respect to (1) access to data and (2) unintended consequences or harm.

To date, we have led or actively participated in the following 
- PPI events (2018,2019) to discuss the use of data for secondary use including operational improvement and research. Patients have repeatedly been supportive of our work as long as there is benefit to the NHS, and privacy is protected.
- Datathons: (2015,2016) to engage the public and to show the value of the data to answer relevant clinical questions, and to bring benefit back to patients

Going forwards we now propose to
- appoint a patient or public representative to the project strategy board
- implement a small series (3) workshops to specifically explore the issues surrounding cancellation of surgery, and the notice periods different individuals would consider acceptable. For example, there is trade off between use of model outputs that would lead to early but more frequent versus late but less frequent cancellations
- continue to work with the PPI lead at UCLH/UCL Clinical Research Informatics Unit to disseminate information about the programme
- engage with the staff, patients and the public whenever possible (e.g. UCLH/UCL BRC Research Open Days: we will host a stand where we show how the forecasts are being used to improve operational efficiency for the trust, and reduce patient distress from short notice cancellations)

## Detailed project plan

TODO: ===========================
TODO: @RESUME 2020-05-19t00:01:46
TODO: ===========================

The research is organised in NN work packages (WP). Each is shown with the number of man-months (MM), the deliverables (D), risks (R) and mitigations (MiT) and milestones (MS). These are then mapped to the attached Gantt chart. Against each of these we have proposed success criteria for three different operational scenarios.

- **medical ward**: booking staff for the following shift
- **surgical ward**: calling patients up for surgery
- **critical care**: giving the go-ahead for surgery that requires ICU

Theses are intended to ensure the application development is focused on delivering achievable improvement in organisational performance, and therefore define the product characteristics.

The work packages are

1. Set-up and governance
2. Application foundation
3. Application integration
4. AI development
5. Application design
6. Model evaluation
7. Quality Management

These work packages are aligned to the following aims and objectives.

### Aims and objectives

#### Need

Admissions in NHS hospitals are managed by individual 'pathway' teams (e.g. colorectal surgery, orthopaedics etc.). These decisions are made without sight of their impact on patient flow both locally (on that pathway) and more widely on the hospital. This results in congestion, on-the-day cancellations, premature discharges, stretched staffing patterns and potential patient harm. Where bed forecasts are performed, they are rarely done at the ward level. The appropriate information is then not in the hands of the local decision maker generating a 'learned helplessness' wherein staff assume that patient congestion is not something over which they can exert control. 

#### Aim 
TODO: rewrite para specifcally starting from existing opportunity
TODO: ? levels: hand entry as per existing app / HL7 /FHIR
TODO: @Sonya/Martin: can we rebuild the model so that it estimates demand for resources other than beds. For example, if we conceptually subdivided the beds within a ward into groups based on nursing intensity, and then saw the patients moving between those 'subwards' then is it possible we could then recover the nursing demand. Ditto if we divide the wards into open bays and siderooms to account for infection control.

We will generate real-time, hyper-local (ward level), short term forecasts of bed demand. These will be provided within a modular application that adapts to the digital maturity level of the host organisation, presents an EHRS agnostic interface, and allows extensions to manage COVID-19 related issues. Specifically, we will extend the model to forecast staffing demand, and demand for isolation beds.
The forecasts will be built in an application designed for the ward leadership team. They are already manage their own staffing and admissions but now they will have a tool that allows them to plan their work. Moreover, the same forecasts will be visible by the hospital bed management team allowing informed negotiation, and better use the constrained bed resource across an organisation. 

#### Objectives
TODO: revisit when you have done the details on the work packages

- to build a robust software application that accepts both automated data feeds, and direct user data entry and reports both current bed status, and forecasted bed demand
- to build the model with a rigorous quality management approach so that can achieve the relevant regulatory approvals for deployment into the NHS
- to perform continuous user testing so that the model and the application are producing 'actionable insights' relevant to the local ward decision makers
- to rebuild the existing length of stay model to use generic inpatient level administrative and clinical features (e.g. demographics, clinical speciality, laboratory measures) that would be available in a wide range of organisations
- to update the AI component of the existing model to improve demand predictions 
- to extend the domain of the model to offer predictions of staffing demand and infection control requirements
- to adapt the model to support the COVID-19 pandemic response (e.g. separate models for blue/green pathways)


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

##### Success criteria
- Staff: All with Honorary contracts and IT access
- Compute: Virtual Machine (GAE) deployed; Web server accessible on the UCLH network via HTTPS
- Data: Access to EMAP ‘User Data Store’ including full HL7 ADT stream from April 2019 
##### Application Milestone
- N/A
##### Model Milestone
- N/A 
##### Man months
- 1 month but up to 3 months elapsed time
##### Risks and mitigation
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
TODO: see if you can find another site for collaboration (Ari, GOSH?): Letter of support; look for external data to validate
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

##### Man months
- W-SE: 6 months: HL7 (+FHIR) interface building; providing an API for the modelling inputs/outputs
- W-AI: 3 months: Re-training the existing models on generic administrative + local ward level data; refactoring code to produce PMML compliant models[@ref: http://dmg.org/pmml/v4-3/GeneralStructure.html]

##### Risks and mitigations
- HL7 interface does not express the full range of ADT messages

We already have HL7v2.3 ADT (01/02/03/04 plus updates and merges) parsed and expressed within EMAP. This creates a system that captures patients in ‘time and place’ with >99% accuracy. We have also already confirmed that we are receiving SIU 12-15. These should cover the majority of ADT and scheduling information that we need. We have a good, longstanding working relationship with both Epic Systems and Atos who have provided these interfaces at UCLH, and we are confident that were we to identify additional fields we would be able to add them to the existing interfaces.

- FHIR interface not previously developed.

Our current HL7 parser is built in a modular manner that converts the incoming message into an internal ‘interchange’ format. Converting from HL7 to FHIR requires only a re-write of the external interface. The logic that then constructs the patient and visit index can then be re-used, and the underlying data model will not need changing. 

- Model cannot be expressed in PMML

Our existing models fall within the specification for PMML. It is unlikely that we would develop a model sufficiently bespoke that this could not be used. However, in that case, we would nonetheless follow the existing principles of keeping the modelling code separate from the application. Therefore whilst the model could not be externally shared, it could be updated and replaced as needed.

##### Figures
##### Refs

#### WP-4: Upgrade AI component of the model
TODO: model and SoA ML
TODO: model and transfer learning
TODO: model upgrades - staffing: the trick here is think about staff demand instead of bed demand: that is rebuild model to predict nursing demand! this can be captured from clinical characteristics
TODO: model upgrades -  infection control: again the key here is to predict demand for bed types
TODO: explain in detail about how the ESR can be used to calibrate from user interactions
TODO: use staff/resource constraints as an example of capturing different information but make this about building an API for the ‘model’

We will explore four areas for upgrading the AI component of the model.

1. Upgrade the LoS predictions using modern ML tools
TODO: @Ken: please comment
The LoS model uses Classificaion and Regression Trees (CART) which were an appropriate choice given the technology in 2012, but have now been superseded. We will evaluate modern machine learning techniques that handle wider ranges of time-fixed and time-varying inputs (deep neural nets, and Long Short Term Memory networks for time-varying features etc.) We will explore the use of a wider range of clinical features (demographics, clinical specialty, labelled structural descriptions of hospital infrastructure, vital signs and clinical laboratory data), and we will ensure that the models are performant at varying levels of digital maturity. Where modern techniques outperform simpler regression models, it is possible that the computational cost will be prohibitive. For example, it may not be feasible to see the model deployed if it must be hosted on GPU enabled infrastructure. We will evaluate the trade-off between model performance and digital infrastructure requirements to ensure the application is widely deployable. Transfer learning (see below) may provide a partial solution.

2. Develop a transfer learning component 
TODO: @Ken: is this sensible?
The initial model will be trained on the full patient record available at UCLH. This includes > 1yr of data from our integrated EHRS plus decades of data from previous PAS and laboratory systems. Even when we limit the features to those that are likely to be available at a wide range of different sites, it is likely that the original UCLH model will be richer and more complete. 
We can imagine a scenario now when the application is deployed to a new institution with either a much reduced or absent training data set. Transfer learning[@ref] will allow the parameters derived from the UCLH model to ‘kick-start’ predictions at the new institution. As local data then accumulates, the model can update and and adapt its performance.
We will simulate this scenario locally by withholding historical data from different sub-speciality wards from the model, and then using transfer learning to generate predictions. 

3. Alternative predictions (staff, bed subtypes)
TODO: @Sonya/Martin: please comment

Forecasting demand for resources other than physical bed capacity will be explored. Specifically, we will investigate extensions of the model that label the beds according to staffing requirements, or infection control standards. For example, we can imagine that the critical care unit is composed of a mixture of beds nursed at 1:1 (Intensive Care) to 1:2 (High Dependency Care) ratios. If we relabel our training data, then the ward can be conceptually subdivided into HDU and ICU compartments and LoS and transitions between each ‘sub-ward’ can be modelled. This can then be expressed as a staffing demand forecast to the end user. A similar approach can be taken by assigning beds certain infection control standards (e.g. side-room  vs open bay beds). 
Predictions derived from these more expressive models will enhance the quality and the range of responses to the demand forecast. For example, acute pressure on siderooms may require re-scheduling of admissions or different cohorting strategies even if the over-all bed demand is manageable.  
Further improvements may be made by using the electronic staff record do describe the actual nursing staff allocated to each ward each shift, or using staff interactions with the EHRS as a proxy for actual nursing levels.  

4. Modelling extensions for COVID-19

Finally, we will explore different modelling strategies to support end users during the COVID-19 pandemic. This will include but not be limited to

- tracking COVID-19 status: specifically, these patients will have different predicted lengths of stay, and different transition pathways within a model.
- blue versus green pathways: patient flow and movement within the same physical footprint will be very different depending on whether the wards are part of a blue (COVID-19 positive), green (COVID-19 negative) or non-pandemic pathway.  
- COVID-19 pandemic resource

##### Success criteria
As per WP-3 plus

- **All scenarios**
    - model accuracy improves so that there are fewer manual corrections
    - demand predictions are subdivided by bed type (side room versus open bay)
    - dashboard reports staff-to-patient by bed type
- **medical ward**: booking staff for the following shift
    - staffing predictions adapt for nursing workload (e.g. proportion of patients on intravenous medications etc.)
- **surgical ward**: calling patients up for surgery
    - surgical admissions requiring specific bedtypes are labelled and forecast distinctly. Scenarios such as surgical cases with MRSA requiring siderooms are handled 
- **critical care**: giving the go-ahead for surgery that requires ICU
    - ICU admissions requiring specific bedtypes are labelled and forecast distinctly (as above). 
    - theatre coordinating team move their planning bed planning discussions forward by 24-48 hours as the predictions become more reliable
    - on-the-day cancellations because of lack of ICU bed capacity reduce
    - theatre teams are confident to start cases before the 9am bed meeting because bed demand was know in advance

##### Application milestone
The web application will now be able to accept a range of different models, and report a range of different outputs. The original length of stay forecasts, and demand models can replaced without loss of application functionality with upgraded versions, or alternative forecasting 'tasks' (staffing, infection control bed subtypes etc.) can be chosen.
The existing patient status view now captures, and reports the relevant inputs (organ support, nursing intensity, or infection control risks etc.)

##### Model milestone
- Model performance is improved for bed demand
- Forecasts of new wards with limited training data are better calibrated than when using a standard 'drop-in' model approach
- Alternative predictions are available as per (3) above
- Model performance is appropriate and meaningful in different COVID-19 scenarios

##### Risks&Mitigation
TODO: add below
* Data access & Electronic Staff Record access already in use by partner at UCLH
* Mathematics & CORU world leading Operational research unit with decades of experience in this field 
##### Figures

##### References 

Special attention will be paid to two specific sources of information that will affect capacity.

#### WP-5: Application user design
TODO: define relevant KPI: can you report and show occupancy and LoS; can we then convert these into a game that the team trys to optimise - nurse to patient ratios : less variation and better optimised

No AI supported health care application is of any value if it is not used, and for the application to add value the users also need to be decision makers. We specifically focus on the ward as the operational unit. Wards manage their own staff, flex up by booking bank staff, handle sickness, and declare a 'capacity' to the wider organisation based on the balance between staff and patient workload.  This task is managed by the nurse in charge. The ward then works in concert with administrative and management roles such as surgical pathway coordinators who manage the upcoming theatre diary, and (operating) theatre managers who construct the daily theatre schedule.

We will use a 'User-centred design' (UCD) to deliver a product that meaningfully enables the ward team to interact with these other groups to maximise operational efficiency. UCD is ... "an iterative design process in which designers focus on the users and their needs ... (and) ... involve users throughout the design process via a variety of research and design techniques, to create highly usable and accessible products for them."[@ref: https://www.interaction-design.org/literature/topics/user-centered-design] This is not about building a slick user interface or using the latest web framework, but rather a functional application that fits into the daily work flow, and solves problems for the users. 
Indeed, the existing Excel based application built through CORU's 'modeller in residence' program closed followed these principles. The product is functional rather than beautiful but has remained in use over many years. The initial product was built in collaboration with the end users, and modified iteratively after deployment.[@ref: original CORU report]
The work will run in parallel with the other work packages with an early phase where the 'user context' is defined, and the 'user's requirements' specified. Potential design solutions will be mocked up, and shared with the application engineer (W-SE). A process of rapid iterations of prototypes and testing will be implemented from the beginning of the project. A similar approach will also be used to tune the inputs and outputs to and from the AI model.

##### Success criteria
- a list of user requirements generated by observation and interviews with ward, theatre, critical care, and surgical pathway teams
- a process for rapid iteration and prototyping that is then employed through-out each of the phases of development for the remainder of the project
- an application that is 'in use' and reached for out of choice when teams come to consider ward operational questions

##### Man months
We have allocated 0.5 days per week over the duration of the project to this work. We would expect this to be front-loaded whilst we collected the initial interviews, and then taper.

##### Risks and mitigations
- Limited access to staff: Staff may be busy or reluctant to invest time with team. We think this risk is low. We have worked with health care design during the implementation of a dashboarding tool on the EMAP platform, and user engagement has been excellent. We will be using the same team. This team has extensive experience of working in healthcare and NHS environments, and are able to observe effectively and gather requirements with minimal disruption.
- Insufficient time: We believe we under-budgeted the time for this work at the Expression of Interest stage, and have increased the investment modestly but to a level where we are confident that we can deliver.
- Front-end-development expertise: Whilst the principles of design are more fundamental than the user-interface, some aspects of the product will require front end development expertise. We will make this a 'desirable' requirement when employing W-SE. Where the individual needs further support then we are confident that there is depth with UCL's Research Software Engineering group such that this can be provided through training.

##### References
- https://www.interaction-design.org/literature/topics/user-centered-design
- [The Four Fundamental Principles of Human-Centered Design and Application](https://jnd.org/the-four-fundamental-principles-ofhuman-centered-design/)

#### WP-x: Model evaluation
TODO: make it clear that this wil be part of the ongoing work; in the Gantt chart it should run all the way through
TODO: work with other sites
TODO: refer to pp14 of - Evidence Standards Framework for Digital Health Technologies (March 2019) and Table 3; 
TODO: unit testing, functional testing; system for monitoring bugs; and tracking issues; then real world data to show that people don't make crazy decisions/cancel cancer cases

TODO headings
- Credibility with UK health and social care professionals (tier 1)
- Relevance to current care pathways in the UK health and social care system
- Acceptability with users (tier 1)
- Equalities considerations (tier 1)
- Accurate and reliable measurements (if relevant).
- Accurate and reliable transmission of data (if relevant).

Model evaluation, safety and reliability data
Comparison against existing models in general use
Each testing cycle deploys the model, and then works with operational and clinical end users to build outputs that provide insights to better manage flow



##### Success criteria
- pre-forecasting success: just timely information available to all users of the *current* state: i.e. who is in what bed at what time
- can you fix the 9am bed meeting so that firstly it runs the evening before; then iteratively move that forward
##### Application milestone
##### Model milestone: 
##### Man months:
##### Figures
##### Refs 

#### WP-x: Quality Management process

It is crucial that we prepare the documentation for the application during its development. This is essential to meet MHRA regulation for software deployed in health care environments. To this end, we have allocated resource and time to work with Prof Dean Barratt who has successfully developed a Quality Management System for the Centre for Medical Image Computing (CMIC) to ISO 13485 standards, and has previous experience of commercialisation. We do not believe this application constitutes a 'medical device' as it does not meet the criteria provided by the MHRA.[@MHRA]

The project will be undertaken with CE marking in mind. Programming will be undertaken within an appropriate environment and documentation will be completed to the required standards. External consultation will be used to ensure that appropriate standards and documentation are maintained.

The aim will be to meet recommended standards such as IEC-62304 (software lifecycle for medical devices) and produce documents including a 'Software Development Plan', and a preliminary 'Risk Analysis' in accordance with ISO-14791 for medical devices.


Update existing network model software to align with ISO 25010:2011 principles (Reliability/Efficiency/Security/Maintainability); ensure interoperability at varying levels of digital maturity (HIMSS 0-7) using HL7 v2.3+ and FHIR. Initiate Quality Management System (QMS) and Medical Device Regulation compliance


Success criteria
Application milestone
Model milestone

NOTE: MHRA class 1? I don't think this is a medical device because the product is not being used for a medical purpose
NOTE: CE marking
NOTE: NHS Evidence Standards for Digital Health Technology (Tier 1); "improve system efficiency but unlikely to have direct and measurable individual patient outcomes"

TODO: will need instead to refer to https://www.gov.uk/government/publications/code-of-conduct-for-data-driven-health-and-care-technology/initial-code-of-conduct-for-data-driven-health-and-care-technology 
    - could map a response against these needs

##### References
- https://www.gov.uk/government/publications/medical-devices-software-applications-apps
- Evidence Standards Framework for Digital Health Technologies (March 2019)

----

## Hurdles
TODO: ?enumerate the hurdles here but explain in detail above

## Risks and mitigations
TODO: enumerate the risks here but explain in detail above
TODO: talk about team management and why we have SH/TB + SC/MU; talk about how we will keep the project on track
TODO: set-up and describe the members of the project management board PMB (cf. study project team) and strategic advisory board (SAB) cf. study steering group
TODO: add in links to be made with UCLB / TTO?

- Risks::Mitigation: 
Others
- lack of experience developing non-research software
    - QMS experience : New partnership with WEISS centre at UCL
    - Software experience ::Existing partnership with UCL Research Software Engineering team 
- inability to recruit
    - use existing team if timing works out well
- limited commercial uptake?
- limited user engagement when there are already other high quality bed planning tools
- too many applications (epic already there)
    - embed in EHRS?


## The Team
NOTE: Explain why the group is well qualified to run this project, describing the track record of the team in health research, technology development and commercialisation. Explain how the applicants work together (or propose to work together if they have not done so previously), and identify other major collaborations important for the research.
NOTE: Describe the existing research support (e.g. funding from other sources) available to the research team, which is relevant to this proposal. Clearly delineate the proposed project from other related research, funded from another source.



TODO: Describe how the project will be managed; use this to talk about the CRIU and how the infrastructure there and that provided by the BRC will enable this project
TODO: explain how the team has worked together before
TODO: perhaps provide a timeline of the work we have done to date
TODO: add Tim

###Specify the role of the lead applicant

## Finance analysis
----------------

## Ethics and regulatory approvals

NOTE: Outline any ethical issues associated with this research and the
arrangements for handling them. If there are no plans to obtain ethical
review, this must be clearly justified. Note that work outlined in your
application must adhere to the UK Framework for Health and Social Care
Research.

- data flow map
- data protection impact assessment
- data sharing agreement
- privacy notice

## Intellectual Property (IP) and commercialisation strategy

### Background IP

\[AppName\] will be built on top of the EMAP Data Science Platform. The
EMAP platform will be responsible for providing an API to access data
from the Epic EHRS. The EMAP IP will be considered background IP.

In building the application front-end we will use open source components
where required. We will ensure that any open source technologies used do
not have a license that would impair our ability to commercialise
\[AppName\].

### Foreground IP
 
#### Freedom to Operate

We have not conducted a formal Freedom to Operate search at this stage
of the project. However, based on our own internal review we see no
potential restrictions on Freedom to Operate for this project. The data
to train the algorithm will come from UCLH and the algorithm itself will
be designed by the CORU, without utilisation of proprietary
technologies.

We will engage the services of our Technology Transfer Office, UCL
Business (UCLB), to conduct this search in the final stages of this
project.

#### Patents/Commercialisable IP

The patentable or commercially exploitable IP generated by this project
will be:

-   An algorithm to predict bed demand using routinely collected EHRS
    data.

-   A scoring engine for running the algorithm in real-time.

-   A software front end for displaying algorithm outputs and allowing the user to interact with the information provided,

UCLB will act on behalf of both UCL and the UCLH NHS Foundation Trust to
manage the IP. UCLB will explore the feasibility of protecting the HAVEN
concept at an early stage and if necessary, will engage the services of
a patent attorney to scope out the novel and inventive elements as the
basis on which a UK priority application could be filed. Additional
claims can be added to this during the first twelve months after
submission, so all developments and outcomes of this project will be
assessed at regular intervals, for submission either as supplementary
information/claims to strengthen the original patent application, or
where appropriate as additional priority applications.

If patenting is not pursued, the \[AppName\] algorithm and code would
still be protected by copyright law, and UCLB would seek to ensure that
the full extent of copyrighted information was captured, that suitable
copyright notices were in place, and that appropriate licensing models
were used to protect and exploit this copyright, following UCLB's
leading-edge software commercialisation strategy. Regular meetings
between the project management team and UCLB to assess arising IP are an
integral part of the project plan.

Revenue-sharing agreements will be put in place between the project
partners and partner institutions, to appropriately reflect the relative
contributions made, as determined by mutual agreement.

### Commercialisation Strategy 

#### Route to Market

The initial target market would be acute hospital trusts the NHS in England, Scotland and Wales who together have an annual budget in excess of £130 billion. The application would be installed by the organisation, and then made available to all wards, including critical care, as well as the bed management and surgical pathway teams. Where digital maturity is such that HL7 or FHIR interfaces are unavailable, the application could be deployed to key wards such as critical care with direct (manual) data entry. 

We will work with UCL/UCLH technology transfer teams to develop the correct business model going forwards.

#### Competitors
TODO: outline of all other current solutions
TODO: \[Guys, you need to write a section in here about how else does flow
management stuff. Anything that might reasonably be considered a
competitor. You've referred to teletracking above. You don't have to do
anything detailed, just classify them into groups -- eg: dashboards with
no AI, RFID-solution etc etc. Then you need to say why your approach is
better.\]

Dashboarding solutions
- Epic ...
Simulation based forecasts
- Hospital IQ
- GE Command Centre
RFID solutions

#### Commercialisation Strategy

The commercialisation strategy will be managed by UCLB. \[Insert
sentence demonstrating their track record\]

We will engage with other NHS Trusts via the UCL Partners Academic
Health Science Network to confirm market demand and optimise
product-market fit. Industry networking opportunities and events will be
identified by UCLB in order to identify potential commercial partners.

The most likely route to market is through licensing of project IP.
However, if our market analysis suggests that a spin-out company would
be a better approach then we will be able to pursue this via UCLB.


Dissemination and NHS adoption strategy
---------------------------------------

NOTE: Please describe the planned outputs of the research and how they
may lead to short and longer-term NHS and patient impacts. As far as
possible, indicate anticipated timescales for these benefits and a
quantitative estimate of their scale. Impacts may include, but are not
restricted to - patient benefit; healthcare staff benefits; changes in
NHS service (including efficiency savings); commercial return (which
could contribute to economic growth); public wellbeing.

NOTE: Describe how the outputs of the research will be communicated and
to whom. Identify key stakeholders, and your plans for engaging them. To
realise impact, it is unlikely that simply making outputs available will
be sufficient. Please consider and outline the active approach you will
take to engaging key parties to disseminate the work.

NOTE: Present a specific strategy for adoption of the technology into
the NHS. Describe the process by which the technology will enter the
healthcare environment, including how your solution will be
acknowledged, selected and introduced for use in the health and care
service or wider society. Detail what current and future barriers to
adoption are likely to be encountered, and a strategy for overcoming
them. Where possible, consider how your solution will be adopted and
implemented longer term, and what efforts and investment are likely to
be needed beyond the project to achieve widespread NHS adoption.

TODO: classify by 
- publications
- algorithms
- application
- user research
- transfer learning model
- local pseudonymised database of patient movements
- Outcomes
    - patient impact
    - NHS benefits

Other supporting roles - signatories
====================================

Director of finance signature against the declaration
=====================================================
