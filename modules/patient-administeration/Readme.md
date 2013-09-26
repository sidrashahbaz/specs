1. Module Scope
---------------

Patient Administration services represent functions necessary to manage, search, and access patient administration registry. Patient Administration services provide a consistent specification for accessing and managing patient administration registry, independent of the underlying technology stack. Patient Administration registry represents various resources including person’s demographics, patient demographics, patient encounters, service locations, entity state changes and encounter appointments. The following thematic areas are considered in scope for.

..* ####Person Demographics and Identification: 
This is a set of functionality that provides the ability to manage person demographics as part of a patient administration service. Its functions include the ability to identify a person and record its demographics as well as verify the identification documents validity provided by the person. These functions are generally protected and accessible by registration clerk and medical record clerk with appropriate authorization.

..* ####Patient Demographics and Identification:
This is a set of functionality that provides the ability to manage patient demographics as part of a patient administration service. The patient information model is not limited to persons; any type of living subject can be registered as a patient. Its functions include the ability to capture full information about the living subject playing the role of patient and patient identification using globally unique identifier. These functions are generally protected and accessible by registration clerk, receptionist and medical record clerk with appropriate authorization.

..* ####Patient Encounters: 
This is a set of functionality that provides the ability to capture a whole lifecycle of patient encounter. From a patient administration perspective, this would include the maintaining different types of patient encounters such as ambulatory, inpatient, short stay and home health encounter. This would also include management service delivery location, attending practitioners and encounter organization as well as encounter location. These functions are generally protected and accessible by clerks, receptionist and provider coordinators with appropriate authorization.

..* ####Search / Query: 
This is a set of functionality that provides the ability to find encounters history based on some search criteria. This includes search encounters by parameters such as encounter type, date of service, patient Id, encounter organization, attending practitioner and a time frame. These functions are generally protected and accessible by clerks, receptionist, provider coordinator and patient with appropriate authorization.

2. Module Perspective
---------------------

SPAS is a subsystem of the SEMR which provides functionality of management of person and patient demographics and visit information about patients.  In addition, the SPAS has interfaces to the external systems such STS (Semantic based terminology Service), SOES (Semantic based order entry service) and SPA enabled applications. Any details of an external system are out of scope of this document. The figure #1 shows decomposition of SPAS on the functionality areas and the supported external systems.
