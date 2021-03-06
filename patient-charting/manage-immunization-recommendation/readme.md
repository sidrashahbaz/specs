####Description
--------------

The Immunization Recommendation is intended to cover communication of a specified patient's immunization recommendation and status across all healthcare disciplines in all care settings and all regions. Additionally, the Immunization Recommendation is expected to cover key concepts related to the querying of a patient's immunization recommendation and status.

![image](https://f.cloud.github.com/assets/4283040/1813840/37f08bc2-6ed6-11e3-84f8-3dc58991e755.png)

####Functional Requirements
* REQ-1: Create Immunization Recommendation
* REQ-2: List Immunization Recommendation
* REQ-3: Get Immunization Recommendation
* REQ-4: Check Immunization Recommendation Status
* REQ-5: Update Immunization Recommendation
* REQ-6: Change Immunization Recommendation Status
* REQ-7: Add Comment to Immunization Recommendation

_______________________________________________________________
**Reference Hl7 RMIM:** [More Details](http://www.hl7.org/implement/standards/product_brief.cfm?product_id=306)

N/A
_______________________________________________________________
**Reference FHIR Resource:**
[More Details](http://www.hl7.org/implement/standards/fhir/immunizationrecommendation.html)

![image](https://f.cloud.github.com/assets/4283040/1810160/a161abd2-6e17-11e3-9c99-8dd73c7117a1.png)

_______________________________________________________________
**Reference CDA Template:** [More Details](http://www.hl7.org/Special/committees/structure/index.cfm)

Section Level Template **"Immunizations V2"**
_______________________________________________________________
**Reference OpenEHR Archetypes (Version 1.4):** [More Details](http://www.openehr.org/ckm/)

```
archetype (adl_version=1.4)
	openEHR-EHR-COMPOSITION.vaccination_list.v1
concept
	[at0000]	-- Vaccination List
language
	original_language = <[ISO_639-1::en]>
description
	original_author = <
		["name"] = <"Heather Leslie">
		["organisation"] = <"Ocean Informatics">
		["email"] = <"heather.leslie@oceaninformatics.com">
		["date"] = <"2013-03-12">
	>
	details = <
		["en"] = <
			language = <[ISO_639-1::en]>
			purpose = <"To record a persistent a list of vaccinations that have been administered to the subject over time and to enable sharing of a vaccination list to other healthcare providers.">
			use = <"Use to record a persistent list of all vaccinations administered to the subject.

In local systems it is possible to generate a list of vaccinations by querying the database for all ACTION.medication archetypes that have been used to record vaccinations. However this list is useful to support exchange of a local vaccination list with other healthcare providers.">
			keywords = <"vaccination", "immunisation", "list">
			misuse = <"">
			copyright = <"© openEHR Foundation">
		>
	>
	lifecycle_state = <"CommitteeDraft">
	other_contributors = <"Ian McNicoll, Ocean Informatics, United Kingdom (Editor)", "Sam Heard, Ocean Informatics, Australia", "Sistine Barretto-Daniels, Ocean Informatics, Australia">
	other_details = <
		["current_contact"] = <"Heather Leslie, Ocean Informatics, heather.leslie@oceaninformatics.com">
		["MD5-CAM-1.0.1"] = <"2D1B12194E93B860DBD6E553CB0D0344">
	>
definition
	COMPOSITION[at0000] matches {	-- Vaccination List
		category matches {
			DV_CODED_TEXT matches {
				defining_code matches {[openehr::431]}
			}
		}
		content cardinality matches {1..*; unordered} matches {
			allow_archetype ACTION[at0001] occurrences matches {0..*} matches {	-- Vaccinations Administered
				include
					archetype_id/value matches {/openEHR-EHR-ACTION\.medication(-[a-zA-Z0-9_]+)*\.v1/}
			}
			allow_archetype EVALUATION[at0002] occurrences matches {0..*} matches {	-- Exclusion Statement
				include
					archetype_id/value matches {/.*/}
			}
			allow_archetype EVALUATION[at0003] occurrences matches {0..*} matches {	-- Absent Information
				include
					archetype_id/value matches {/openEHR-EHR-EVALUATION\.absence(-[a-zA-Z0-9_]+)*\.v1/}
			}
		}
	}
ontology
	term_definitions = <
		["en"] = <
			items = <
				["at0000"] = <
					text = <"Vaccination List">
					description = <"A persistent a list of vaccinations that have been administered to the subject over time, that may influence clinical decision-making and care provision.">
				>
				["at0001"] = <
					text = <"Vaccinations Administered">
					description = <"Details about vaccinations that have been administered to the subject.">
				>
				["at0002"] = <
					text = <"Exclusion Statement">
					description = <"Positive statement about the known exclusion of vaccination administration.">
					comment = <"For example: \"No vaccinations have been administered\".">
				>
				["at0003"] = <
					text = <"Absent Information">
					description = <"Positive statement that no information is available about vaccine administration.">
				>
			>
		>
>
```
