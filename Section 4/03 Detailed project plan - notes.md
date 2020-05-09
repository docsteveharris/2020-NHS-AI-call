## Detailed project plan

TODO: add in success criteria with dates and evidence

### Aims and objectives
Need/aim/objectives
- training data
	- staff
	- patient
- two part infrastructure
	- model
	- interface
- user design
- regulation

### Individual work packages

The individual work packages within your project, including deliverables and milestones (a Gantt chart indicating the schedule for the completion of work must be attached). Work packages may focus on, for example, technical, clinical or commercial aspects of the project.

#### WP1: Upgrade AI component of the model

TODO: justification for this WP

We will merge the existing patient level Lenght of Stay (LOS) prediction model and the (non-Markovian) network model; then upgrade the AI from low complexity (CART, regression based) to approaches capable of handling wider ranges of time-fixed and time-varying inputs (deep neural nets, and Long Short Term Memory networks for time-varying features etc.)

- Milestone: Deployment of combined model
- Risks<>Mitigation:
	- Data access <> £2.9m programme 2018-20 @ UCLH built live data science platform; PoC already deployed and running


#### WP2: Staffing/resource constraints
Extension of the model to include staffing/resource constraints wherein current models understand limitations with respect to physical capacity but often staffing/resource is the more important functional limitation.

- Milestone: Deployment of model with staffing module
- Risks<>Mitigation: 
	- Data access <> Electronic Staff Record access already in use by partner at UCLH
	- Mathematics <> CORU world leading Operational research unit with decades of experience in this field 

TODO: explain in detail about how the ESR can be used to calibrate from user interactions

#### WP3: Digital implementation
Update existing network model software to align with ISO 25010:2011 principles (Reliability/Efficiency/Security/Maintainability); ensure interoperability at varying levels of digital maturity (HIMSS 0-7) using HL7 v2.3+ and FHIR. Initiate Quality Management System (QMS) and Medical Device Regulation compliance

- Milestone: Deployment of model with FHIR API
- Risks<>Mitigation: 
	- QMS experience <> New partnership with WEISS centre at UCL
	- Software experience <> Existing partnership with UCL Research Software Engineering team 

TODO: see WP 4 of liver app 'technical file prep'

#### WP4: User evaluation / model evaluation / compliance
Model evaluation, safety and reliability data
Comparison against existing models in general use
Each testing cycle deploys the model, and then works with operational and clinical end users to build outputs that provide insights to better manage flow

- Milestone: Completed user facing validated software application
- Risks<>Mitigation: 
	- User interface design experience: In-house team Royal College of Art Health Care design team


?clinical evaluation
?feasibility study

### hurdles
> A description of the main hurdles to be overcome technically, clinically and commercially.

### risks and mitigations

The key risks to your project (including technical, clinical, financial and IP risks) and the steps you will take to manage and mitigate these risks. Ensure that these risks are considered when defining milestones (the go/no go points for your project).


TODO: section on project management and governance; who is on the team; work with UCLH partners; meeting cadence
