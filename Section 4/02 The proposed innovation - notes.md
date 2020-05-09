## The proposed innovation (notes)

---
enumerate the specific advantages/opportunities for the reader
I think you should separate out the forecasting technology from the 'pipeline' and argue that the tech can be upgraded but getting the pipeline sorted is the major challenge
sections on data governance
build prototype local case study working with ops centre to figure out what outputs they need to better plan their work (human factors/health care design stuff)
might be appropriate to define aims/objectives

- focus on data set building
- think about optimum placement of patients to minmise transmission; realtime monitoring of ICT
- Keep the system running as a distributed network of forecasts to get local buy in
- Whiteboard data updates as per FixNFiddle: e.g. build your own HL7 stream forecast; run in its own database; then add additional information (imagine each patient has a tuning parameter that adjusts the LoS; derived from observed characteristics; now local team can interact by updating that in a meaningful way: flag likely to die; likely to discharge; likely to bed block)
- Keep the forecasting tool local so it is used (but also by being local then team *adds* knowledge to it as above) whereas if ‘hospital’ level then no knowledge added; local tool becomes untrustworthy
	- go further and emphasise there that no AI solution will be perfect and this compensates; don’t always have to build a better methodological model but often more important to get better data 

?Jon Gillham as the dev?

talk about tessellating cases to make use of capacity; it's not just about the bed being full but about the bed being 'used'

> Provide a clear description of your AI solution covering comprehensive details of its functionality, structure and intended use. Explain the level of innovation of the proposed technology and the intellectual property position, accompanied by a review of the existing evidence surrounding similar products that may already be on the market, and of any relevant ongoing research in the area of focus. A consideration of the proposed barriers to clinical/social adoption must also be clearly articulated.

#### WP2.1 UI
Justify the hyperlocal piece here
local data capture (tuning) via interactive UI 
Early prototype to floor
Simplest possible model to start with
Display ‘now’ and ‘next’


#### WP3: Digital implementation

TODO: refactor the app (include figure to show) 
	inputs piece (HL7 or FHIR or even ‘hand’ entry)
	display now and receive edits
	forecast piece
TODO: hence need data models that can handle this representation
	- patient data model
	- Bed model
	- Staff model	 
TODO: see WP 4 of liver app 'technical file prep'



