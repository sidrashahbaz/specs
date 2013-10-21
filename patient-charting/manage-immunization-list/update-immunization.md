#####Use Case ID: UC-PCS09
#####Use Case Name: Update Immunization

**Level:**                     User Level Goal

**Primary Actors:**            Doctor/ Physician/ Clinician 

**Stakeholders:**              Patient Charting User

**Purpose:**                   The main intent of this use case is to update immunization in the list.

**Pre Condition:**             Doctor/ Physician/ Clinician must be identified and authenticated.  

**Post Condition:**            Immunization updated successfully without any conflicts.  

**Frequency of Occurrence:**   High

**Priority:**                  High
__________________________________________________________
**Main Success Scenario: (Update Immunization)**

1.	Physician selects the update immunization option.
2.	System shows the list of the current immunization of particular patient.
3.	Physician will select the immunization from the list.
4.	System will display immunization administration history including; administering clinician, date and time, immunization name, lot number, manufacturer and expiration date.
5.	Physician will modify the required information.
6.	System will perform following actions:
    * It will validate the information.
    * It will perform interaction checking.
7.	Physician will save the updated immunization.
8.	System will perform following actions:
    * It store immunization details as discrete data.
    * It will record the identity of prescriber.
    * It will record the date and time.
    * It will set immunization status to active.

_______________________________________________________________
**Open Issues**

-NA-
_______________________________________________________________
**Reference Hl7 V3 Interaction Identifiers (Domain: Immunization List):**

-NA-
_______________________________________________________________
**Reference CCHIT Criteria:**

FN 16.02, FN 16.03, IP 15.01, IP 15.06, IP 15.04  

_______________________________________________________________
**EHR Functional Criteria:**

DC 1.4.4
