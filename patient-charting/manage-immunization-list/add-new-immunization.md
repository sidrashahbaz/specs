#####Use Case ID: UC-PCS08
#####Use Case Name: Add New Immunization

**Level:**                     User Level Goal

**Primary Actors:**            Doctor/ Physician/ Clinician 

**Stakeholders:**              Patient Charting User

**Purpose:**                   The main intent of this use case is to add new immunization in the list.

**Pre Condition:**             Doctor/ Physician/ Clinician must be identified and authenticated.  

**Post Condition:**            Immunization added successfully without any conflicts.  

**Frequency of Occurrence:**   High

**Priority:**                  High
__________________________________________________________
**Main Success Scenario: (Add Comment to Problem)**

1.	Physician selects the add immunization option for a particular patient.
2.	System shows the patient immunization history.
3.	Physician will select the coded immunization from the list and will specify the following information:
    * Route and frequency.
    * immunization type and dose
    * date and time of administration
    * lot number and expiration date
    * manufacturer
    * user ID
4.	System will perform following actions:
    * It will validate the information.
    * It will perform interaction checking.
5.	Physician will save immunization order.
6.	System will perform following actions:
    * It store immunization details as discrete data.
    * It will record the identity of prescriber.
    * It will record the date and time.
    * It will set immunization status to active.

_______________________________________________________________
**Open Issues**

-NA-
_______________________________________________________________
**Reference Hl7 V3 Interaction Identifiers (Domain: Problem List):**

-NA-
_______________________________________________________________
**Reference CCHIT Criteria:**

FN 16.02, FN 16.03, IP 15.01, IP 15.06, IP 15.04  

_______________________________________________________________
**EHR Functional Criteria:**

DC 1.4.4
