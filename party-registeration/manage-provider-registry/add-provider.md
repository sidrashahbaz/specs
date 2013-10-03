#####Use Case ID: UC-PRS01
#####Use Case Name: Add Provider

**Level:**                     User Level Goal

**Primary Actors:**            Registration Clerk (RC)

**Stakeholders:**              Registration Clerk, Healthcare Provider

**Purpose:**                   The main intent of this use case is to add provider details.

**Pre Condition:**             RC must be identified and authenticated.

**Post Condition:**            Provider identifiers and demographics will be recorded in local provider
registry successfully.

**Frequency of Occurrence:**   Medium

**Priority**                   High
__________________________________________________________
**Main Success Scenario: (Add Provider)**

1. RC requests the system to add provider’s registry.
2. System asks user to enter provider’s full information including name, Id, role identifier,
certification document, work locations and disciplinary actions etc.
3. RC enters the required information.
4. System then performs following steps:
  * Validates the entered information.
  * Associates key identifiers information (i.e Id, state medical license, DEA) with patient record.
  * Stores patient record in separate discrete data fields successfully.
  
_______________________________________________________________________________
**Alternate Flows** 

**Alt-1**

1. Invalid information cannot be added.
2. Invalid identifier.

________________________________________________________________________
**Reference Hl7 V3 Interaction Identifiers (Domain: Scheduling):**

PRPM_ST301000UV01
_______________________________________________________________
**Reference CCHIT Criteria:**

AM 27.01, AM 27.02, AM 27.04

