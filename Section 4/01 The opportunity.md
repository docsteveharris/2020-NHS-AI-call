## The opportunity

---
Notes
compare/contrast with current technology
explain advantages of our approach
explain current state of the work
notes on the specific need with COVID to manage beds better
overall justification of the importance of this work
need to show the tech works; but that you need now to develop this into a platform that can be deployed and tested: i.e. again this efficacy not effectiveness work

---


### NHS unmet clinical need and market plan
> Provide a clear explanation of the health or social care problem to be addressed, the impact on patients as well as health and social care services, and how the proposed work would fill a demonstrable evidence gap. Please also provide a description of how your AI solution will support the NHS Long Term Plan, NHSX strategic priorities and/or wider government priorities including the Industrial Strategy grand challenges or resource efficiency. Please report market size, any related trend or forecast, patient population affected, NHS cost burden, and state of the art.


25,475 operations were cancelled on the day of surgery in NHS England (NHS-E) in just one quarter in 2018: the highest number in two decades. Last winter, NHS-E recommended that all elective surgery to be cancelled in January to aid with winter bed pressures.(M Gillies, 2018) Yet even in winter NHS operating theatres are often labelled inefficient. Major surgery in our own hospitals is routinely delayed until after the daily 9am ‘bed meeting’ that reports whether ICU beds are available for high risk surgery while the patients, surgeons, scrub nurses and  anaesthetists are all ready to go from 730am. 
We found in 245 NHS hospitals that on average 10% of surgical admissions had been previously cancelled (more in hospitals with fewer ICU beds, and more emergency work).(D Wong 2018) On-the-day cancellations for bed capacity should become a ‘never event’ in the NHS. 
This ambition requires high quality bed demand forecasts. These enable the workforce by putting the information they need in their hands at the right time. Staffing can be flexed, patients forewarned, or schedules re-adjusted to improve efficiency.
We have already built and deployed a prototype bed demand forecasting model. This has been deployed to predict bed demand for Great Ormond Street Hospital’s cardio-thoracic ICU since 2012. It produces a real time, hyper-local, 7-day forecast of bed demand. In 2018-9, we collaborated with University College Hospital’s digital platform team to (1)  generalise our model to work for any ward in a complex network of flows, and (2) start to adapt the technology for different levels of digital ‘readiness’. As per NHS-X strategies, the platform is interoperable, robust and scalable. We now seek support to update our prototype with state of the art ‘machine learned’ clinical features, and to generate the safety and efficacy data for deployment across the NHS.

### Benefit to patients, the NHS and the wider population

> Provide a clear case of how the proposed device, technology or intervention will change clinical practice and provide benefit to patients (such as reduced mortality or morbidity, improved quality of life, reduced misdiagnosis, and improved patient outcomes and experiences). Potential cost savings for the NHS should also be provided.
> Clearly articulate the expected benefit to patients, the NHS and/or social care settings and the wider community. Please note that your AI solution must have the potential to be cost effective and meet at least one of the following criteria

> - Improvement in patient outcomes
> - Improvement in patient experience
> - Improvement in operational efficiency

> Descibe the impact the project aims to achieve. Impact may include but is not restricted to:

> - Patient & public wellbeing (improved quality of life, improved safety, improved satisfaction with care, improved independent living, improved health, slowed progression of ill health)
> - Clinical benefits (improved accuracy of diagnosis, improved detection rates, reduced false positive/negatives, improved health data quality/availability; improved effectiveness of the therapy, improved availability of the therapy, improved ability to stabilise/manage the condition)
> - Staff & service provision benefits (improved staff capacity, improved staff capabilities-knowledge and skills-, simplified/improved care pathway, more efficient care pathway, reduced number of procedures, reduced waiting times)
> - Economic benefits & commercial ROI (reduced service delivery costs, improved organisation/service cost control, reduced treatment cost to patient, reduced staffing cost)
> - Social and policy benefits (change in policy, change in professional guidance, improved awareness)

Modelling bed occupancy and flow to improve operational efficiency has been a long term endeavour in the NHS. The health service is under intense pressure and 'coping but not coping' strategies (e.g. premature discharge, outlying medical patients on surgical wards, and negative feedback loops that reduce referrals) cause harm, reduce income, and increase strain elsewhere in the system.(E Wolstenholme, 2007)
Commercial bed forecasting models are typically derived in US markets (e.g. TeleTracking/HospitalIQ), poorly adapted to the NHS, and are simulation based. Simulations are unable to distinguish true demand from the mitigated demand derived from the 'coping but not coping' strategies.
Our approach brings three advantages. (1) We model actual demand not mitigated demand. (2) Our results are local (ward level) and real time rather than system level and strategic. This gives local teams the ability to make tactical responses, flex staffing and adjust schedules themselves. (3) We integrate with existing digital systems and use modern machine learning techniques to tune the forecasts to the available data and the local context.
Surgical cancellations are miserable for the patient, wasteful for the system, and can cause harm. But there is a greater opportunity. Current NHS strategy recommends running a hospital at 85% occupancy for maximum efficiency, and above 92% is regarded as a tipping point where flows from upstream services (A&E etc.) are impaired. High quality length of stay (LoS) and bed demand forecasts will allow us to move away from this 'rigid occupancy target' toward the equivalent of 'just-in-time' manufacturing processes. Patients with greater LoS can be identified to downstream health and social care partners earlier. And periods when such patients cause congestion in the system can be managed by pre-emptively adjusting the incoming elective case mix to favour a higher turnover/shorter stay cases.