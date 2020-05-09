## The opportunity

### NHS unmet clinical need and market plan

We submitted the Expression of Interest for this call on 4 March 2020. On 11 March 2020 the WHO declared COVID-19 a global pandemic. The need for an effective tool to forecast hospital bed demand, and provide reliable, ward level forecasts was pressing when we made the original application. It is even more pressing now. There is no future where NHS capacity is plentiful. Even if we can build temporary hospitals, we cannot instantly train new staff and expand the workforce overnight. Instead it is imperative that we better manage our existing resource, and make the system as efficient as possible. 
Above all we must remember that the problems of bed supply and demand were increasing even before COVID-19. Between 2010 and 2019, NHS bed capacity fell by 10.1%, and bed occupancy levels rose from 85% to 90%, with corresponding knock-on effects in waiting times for A&E, for cancer and for surgery.[@NHS Key Statistics briefing paper 2020]

#### Bed demand prior COVID-19

In 2018, we found in 245 NHS hospitals that on average 10% of surgical admissions had been previously cancelled (more in hospitals with fewer ICU beds, and more emergency work).[@Wong 2018] This amounted to 25,475 operations being cancelled on the day of surgery in just one quarter in 2018 for NHS-England: the highest number in two decades. The following winter, NHS-E recommended that all elective surgery be cancelled in January to aid with winter bed pressures.[@Gillies 2018] 
Yet even then NHS operating theatres are often labelled inefficient. Major surgery in our own hospitals is routinely delayed until after the daily 9am ‘bed meeting’ that reports whether ICU beds are available for high risk surgery while the patients, surgeons, scrub nurses and  anaesthetists are all ready to go from 730am.  
Hospitals often have neither an accurate view of the forthcoming bed demand, nor a realtime view of existing pressures.

#### Bed demand with COVID-19

Key constraints, such as ICU bed capacity, are now widely reported. The UK has few critical care beds: 6.6 per 100,000 compared to a median of 11.5 in Europe. On March 17 2020, the NHS Senior leadership wrote to all NHS trusts on March 17, and asked them to "free-up the maximum possible inpatient and critical care capacity" (for COVID-19).[@Stevens 2020] This has had, as yet, unmeasured consequences for non-COVID healthcare. Early indicators suggest the pandemic has caused indirect harm through this re-allocation of resource.[@wise2020] A 'medical debt' has accrued whilst normal health care services have been diverted. The cost of this debt remains a modifiable part of the pandemic response. Efficient and effective allocation of beds following the initial surge, and during the ongoing pressures is key to making that modification and minimising harm. 

#### ...
TODO: paragraph explaining why now and future views important

Such allocation depends on

- visibility of the ‘now’ (EMAP HL7 parser, background IP); make argument about integration engines and therefore generalisabilty
- accurate forecasts of the ‘future’: CORU work

Efficient and accurate bed forecasts for general wards and for critical care that 

... need to allow for changes in emergency demand as well as scheduled deman

Success criteria

- On-the-day cancellations for bed capacity should become a ‘never event’ in the NHS
- Hospital and critical care occupancy
- Theatre cases start before the 9am bed-meeting
- Ward forecasts and views can be seen across the organisation (not just siloed view from your own nursing work station); no ‘phone calls’ to find out who is ready to discharge

This ambition requires high quality bed demand forecasts. These enable the workforce by putting the information they need in their hands at the right time. Staffing can be flexed, patients forewarned, or schedules re-adjusted to improve efficiency.

#### Existing product / experience
We have already built and deployed a prototype bed demand forecasting model. This has been deployed to predict bed demand for Great Ormond Street Hospital’s cardio-thoracic ICU since 2012. It produces a real time, hyper-local, 7-day forecast of bed demand. In 2018-9, we collaborated with University College Hospital’s digital platform team to (1)  generalise our model to work for any ward in a complex network of flows, and (2) start to adapt the technology for different levels of digital ‘readiness’. As per NHS-X strategies, the platform is interoperable, robust and scalable. We now seek support to update our prototype with state of the art ‘machine learned’ clinical features, and to generate the safety and efficacy data for deployment across the NHS.

### Benefit to patients, the NHS and the wider population

Modelling bed occupancy and flow to improve operational efficiency has been a long term endeavour in the NHS. The health service is under intense pressure and 'coping but not coping' strategies (e.g. premature discharge, outlying medical patients on surgical wards, and negative feedback loops that reduce referrals) cause harm, reduce income, and increase strain elsewhere in the system.(E Wolstenholme, 2007)
Commercial bed forecasting models are typically derived in US markets (e.g. TeleTracking/HospitalIQ), poorly adapted to the NHS, and are simulation based. [TODO: before critiquing simulations, explain what they are]Simulations are unable to distinguish true demand from the mitigated demand derived from the 'coping but not coping' strategies.
Our approach brings three advantages. (1) We model actual demand not mitigated demand. (2) Our results are local (ward level) and real time rather than system level and strategic. This gives local teams the ability to make tactical responses, flex staffing and adjust schedules themselves. (3) We integrate with existing digital systems and use modern machine learning techniques to tune the forecasts to the available data and the local context.
Surgical cancellations are miserable for the patient, wasteful for the system, and can cause harm. But there is a greater opportunity. Current NHS strategy recommends running a hospital at 85% occupancy for maximum efficiency, and above 92% is regarded as a tipping point where flows from upstream services (A&E etc.) are impaired. High quality length of stay (LoS) and bed demand forecasts will allow us to move away from this 'rigid occupancy target' toward the equivalent of 'just-in-time' manufacturing processes. Patients with greater LoS can be identified to downstream health and social care partners earlier. And periods when such patients cause congestion in the system can be managed by pre-emptively adjusting the incoming elective case mix to favour a higher turnover/shorter stay cases.
