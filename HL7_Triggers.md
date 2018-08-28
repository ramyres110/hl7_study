# HL7 v2.7
## Triggers

### 1. ACK - Acknowledge
```typescript
interface Acknowledge{
    MSH:MSH,//Message Header
    SFT?:SFT,//Software Segment
    UAC?:UAC,//User Authentication Credential Segment
    MSA:MSA,//Message Acknowledgment
    ERR?:ERR//Error
}
```

### 2. ADT - Admit, Transfer and Dischard
#### ADT A01 - Admit/visit notification
```typescript
interface ADT_A01{
    MSH:MSH,
    SFT?:SFT,
    UAC?:UAC,
    EVN:EVN,
    PID:PID,
    PD1?:PD1,
    ARV?:ARV,
    ROL?:ROL,
    NK1?:NK1,
    PV1:PV1,
    PV2?:PV2,
    ARV?:ARV,
    ROL?:ROL,
    DB1?:DB1,
    OBX?:OBX,
    AL1?:AL1,
    DG1?:DG1,
    DRG?:DRG,
    //GROUP PROCEDURE
    PR1:PR1,
    ROL?:ROL,
    GT1?:GT1,
    //GROUP INSURANCE
    IN1:IN1,
    IN2?:IN2,
    IN3?:IN3,
    ROL?:ROL,
    ACC?:ACC,
    UB1?:UB1,
    UB2?:UB2,
    PDA?:PDA
}
```
#### ADT A02 - Transfer a patient
```typescript
interface ADT_A02{
    MSH:MSH,
    SFT?:SFT,
    UAC?:UAC,
    EVN:EVN,
    PID:PID,
    PD1?:PD1,
    ARV?:ARV,
    ROL?:ROL,
    PV1:PV1,
    PV2?:PV2,
    ARV?:ARV,
    ROL?:ROL,
    DB1?:DB1,
    OBX?:OBX,
    PDA?:PDA
}
```
#### ADT A03 - Discharge/end visit
```typescript
interface ADT_A03{
    MSH:MSH,
    SFT?:SFT,
    UAC?:UAC,
    EVN:EVN,
    PID:PID,
    PD1?:PD1,
    ARV?:ARV,
    ROL?:ROL,
    NK1?:NK1,
    PV1:PV1,
    PV2?:PV2,
    ARV?:ARV,
    ROL?:ROL,
    DB1?:DB1,
    AL1?:AL1,
    DG1?:DG1,
    DRG?:DRG,
    PR1:PR1,
    ROL?:ROL,
    OBX?:OBX,
    GT1?:GT1,
    IN1:IN1,
    IN2?:IN2,
    IN3?:IN3,
    ROL?:ROL,
    ACC?:ACC,
    PDA?:PDA
}
```
#### ADT A04 - Register a patient
```typescript
interface ADT_A04{}
```
#### ADT A05 - Pre-admit a patient
```typescript
interface ADT_A05{}
```
#### ADT A06 - Change an outpatient to an inpatient
```typescript
interface ADT_A06{}
```
#### ADT A07 - Change an inpatient to an outpatient
```typescript
interface ADT_A07{}
```
#### ADT A08 - Update patient information
```typescript
interface ADT_A08{}
```
#### ADT A09 - Patient departing - tracking
```typescript
interface ADT_A09{}
```
#### ADT A10 - Patient arriving - tracking
```typescript
interface ADT_A10{}
```
#### ADT A11 - Cancel admit/visit notification
```typescript
interface ADT_A11{}
```
#### ADT A12 - Cancel transfer
```typescript
interface ADT_A12{}
```
#### ADT A13 - Cancel discharge/end visit
```typescript
interface ADT_A13{}
```
#### ADT A14 - Pending admit
```typescript
interface ADT_A14{}
```
#### ADT A15 - Pending transfer
```typescript
interface ADT_A15{}
```
#### ADT A16 - Pending discharge
```typescript
interface ADT_A16{}
```
#### ADT A17 - Swap patients
```typescript
interface ADT_A17{}
```
#### ADT A20 - Bed status update
```typescript
interface ADT_A20{}
```
#### ADT A21 - Patient goes on a "leave of absence"
```typescript
interface ADT_A21{}
```
#### ADT A22 - Patient returns from a "leave of absence"
```typescript
interface ADT_A22{}
```
#### ADT A23 - Delete a patient record
```typescript
interface ADT_A23{}
```
#### ADT A24 - Link patient information
```typescript
interface ADT_A24{}
```
#### ADT A25 - Cancel pending discharge
```typescript
interface ADT_A25{}
```
#### ADT A26 - Cancel pending transfer
```typescript
interface ADT_A26{}
```
#### ADT A27 - Cancel pending admit
```typescript
interface ADT_A27{}
```
#### ADT A28 - Add person information
```typescript
interface ADT_A28{}
```
#### ADT A29 - Delete person information
```typescript
interface ADT_A29{}
```
#### ADT A31 - Update person information
```typescript
interface ADT_A31{}
```
#### ADT A32 - Cancel patient arriving - tracking
```typescript
interface ADT_A32{}
```
#### ADT A33 - Cancel patient departing - tracking
```typescript
interface ADT_A33{}
```
#### ADT A37 - Unlink patient information
```typescript
interface ADT_A37{}
```
#### ADT A38 - Cancel pre-admit
```typescript
interface ADT_A38{}
```
#### ADT A40 - Merge patient - patient identifier list
```typescript
interface ADT_A40{}
```
#### ADT A41 - Merge account - patient account number
```typescript
interface ADT_A41{}
```
#### ADT A42 - Merge visit - visit number
```typescript
interface ADT_A42{}
```
#### ADT A43 - Move patient information - patient identifier list
```typescript
interface ADT_A43{}
```
#### ADT A44 - Move account information - patient account number
```typescript
interface ADT_A44{}
```
#### ADT A45 - Move visit information - visit number
```typescript
interface ADT_A45{}
```
#### ADT A47 - Change patient identifier list
```typescript
interface ADT_A47{}
```
#### ADT A49 - Change patient account number
```typescript
interface ADT_A49{}
```
#### ADT A50 - Change visit number
```typescript
interface ADT_A50{}
```
#### ADT A51 - Change alternate visit ID
```typescript
interface ADT_A51{}
```
#### ADT A52 - Cancel leave of absence for a patient
```typescript
interface ADT_A52{}
```
#### ADT A53 - Cancel patient returns from a leave of absence
```typescript
interface ADT_A53{}
```
#### ADT A54 - Change attending doctor
```typescript
interface ADT_A54{}
```
#### ADT A55 - Cancel change attending doctor
```typescript
interface ADT_A55{}
```
#### ADT A60 - Update allergy information
```typescript
interface ADT_A60{}
```
#### ADT A61 - Change consulting doctor
```typescript
interface ADT_A61{}
```
#### ADT A62 - Cancel change consulting doctor
```typescript
interface ADT_A62{}
```

## 3. BAR - Add/change billing account
### BAR P01 - Add patient accounts
### BAR P02 - Purge patient accounts
### BAR P05 - Update account
### BAR P06 - End account
### BAR P10 - Transmit Ambulatory Payment Classification(APC)
### BAR P12 - Update Diagnosis/Procedure

### BPS O29 - Blood product dispense status

### BRP O30 - Blood product dispense status acknowledgment

### BRT O32 - Blood product transfusion/disposition acknowledgment

### BTS O31 - Blood product transfusion/disposition

### CCF I22 - Collaborative Care Fetch / Collaborative Care Information

### CCM I21 - Collaborative Care Message

### CCQ I19 - Collaborative Care Query/Collaborative Care Query Update

### CCR I16 - Collaborative Care Referral
### CCR I17 - Modify Collaborative Care Referral
### CCR I18 - Cancel Collaborative Care Referral

### CCU I20 - Asynchronous Collaborative Care Update

### CRM C01 - Register a patient on a clinical trial
### CRM C02 - Cancel a patient registration on clinical trial (for clerical mistakes onl
### CRM C03 - Correct/update registration information
### CRM C04 - Patient has gone off a clinical trial
### CRM C05 - Patient enters phase of clinical trial
### CRM C06 - Cancel patient entering a phase (clerical mistake)
### CRM C07 - Correct/update phase information
### CRM C08 - Patient has gone off phase of clinical trial

### CSU C09 - Automated time intervals for reporting, like monthly
### CSU C10 - Patient completes the clinical trial
### CSU C11 - Patient completes a phase of the clinical trial
### CSU C12 - Update/correction of patient order/result information

### DFT P03 - Post detail financial transaction
### DFT P11 - Post Detail Financial Transactions - New

### EAC U07 - Automated equipment command

### EAN U09 - Automated equipment notification

### EAR U08 - Automated equipment response

### EHC E01 - Submit HealthCare Services Invoice
### EHC E02 - Cancel HealthCare Services Invoice
### EHC E04 - Assess HealthCare Services Invoice Request
### EHC E10 - Edit/Adjudication Results
### EHC E12 - Request Additional Information
### EHC E13 - Additional Information Response
### EHC E15 - Payment/Remittance Advice
### EHC E20 - Submit Authorization Request
### EHC E21 - Cancel Authorization Request
### EHC E24 - Authorization Response

### ESR U02 - Automated equipment status request

### ESU U01 - Automated equipment status update

### INR U06 - Automated equipment inventory request

### INU U05 - Automated equipment inventory update

### LSR U13 - Automated equipment log/service request

### LSU U12 - Automated equipment log/service update

### MDM T01 - Original document notification
### MDM T02 - Original document notification and content
### MDM T03 - Document status change notification
### MDM T04 - Document status change notification and content
### MDM T05 - Document addendum notification
### MDM T06 - Document addendum notification and content
### MDM T07 - Document edit notification
### MDM T08 - Document edit notification and content
### MDM T09 - Document replacement notification
### MDM T10 - Document replacement notification and content
### MDM T11 - Document cancel notification

### MFN M02 - Master file - staff practitioner
### MFN M04 - Master files charge description
### MFN M05 - Patient location master file
### MFN M06 - Clinical study with phases and schedules master file
### MFN M07 - Clinical study without phases but with schedules master file
### MFN M08 - Test/observation (numeric) master file
### MFN M09 - Test/observation (categorical) master file
### MFN M10 - Test /observation batteries master file
### MFN M11 - Test/calculated observations master file
### MFN M12 - Master file notification message
### MFN M13 - Master file notification - general
### MFN M14 - Master file notification - site defined
### MFN M15 - Inventory item master file notification
### MFN M16 - Master File Notification Inventory Item Enhanced
### MFN M17 - DRG Master File Message

### NMD N02 - Application management data message (unsolicited)

### OMB O27 - Blood product order

### OMD O03 - Diet order

### OMG O19 - General clinical order

### OMI O23 - Imaging order

### OML O21 - Laboratory order
### OML O33 - Laboratory order for multiple orders related to a single specimen
### OML O35 - Laboratory order for multiple orders related to a single container of a sp
### OML O39 - Specimen shipment centric laboratory order

### OMN O07 - Non-stock requisition order

### OMP O09 - Pharmacy/treatment order

### OMS O05 - Stock requisition order

### OPL O37 - Population/Location-Based Laboratory Order Message

### OPR O38 - Population/Location-Based Laboratory Order Acknowledgment Message

### OPU R25 - Unsolicited Population/Location-Based Laboratory Observation Message

### ORA R33 - Observation Report Acknowledgement

### ORB O28 - Blood product order acknowledgment

### ORD O04 - Diet order acknowledgment

### ORG O20 - General clinical order response

### ORI O24 - Imaging order response message to any OMI

### ORL O22 - General laboratory order response message to any OML
### ORL O34 - Laboratory order response message to a multiple order related to single sp
### ORL O36 - Laboratory order response message to a single container of a specimen OML
### ORL O40 - Specimen Shipment Centric Laboratory Order Acknowledgment Message

### ORN O08 - Non-stock requisition acknowledgment

### ORP O10 - Pharmacy/treatment order acknowledgment

### ORS O06 - Stock requisition acknowledgment

### ORU R01 - Unsolicited transmission of an observation message
### ORU R30 - Unsolicited Point-Of-Care Observation Message Without Existing Order - Pla
### ORU R31 - Unsolicited New Point-Of-Care Observation Message - Search For An Order
### ORU R32 - Unsolicited Pre-Ordered Point-Of-Care Observation

### OSM R26 - Unsolicited Specimen Shipment Manifest Message

### OUL R22 - Unsolicited Specimen Oriented Observation Message
### OUL R23 - Unsolicited Specimen Container Oriented Observation Message
### OUL R24 - Unsolicited Order Oriented Observation Message

### PEX P07 - Unsolicited initial individual product experience report
### PEX P08 - Unsolicited update individual product experience report

### PGL PC6 - PC/ goal add
### PGL PC7 - PC/ goal update
### PGL PC8 - PC/ goal delete

### PIN I07 - Unsolicited insurance information

### PMU B01 - Add personnel record
### PMU B02 - Update personnel record
### PMU B03 - Delete personnel re cord
### PMU B04 - Active practicing person
### PMU B05 - Deactivate practicing person
### PMU B06 - Terminate practicing person
### PMU B07 - Grant Certificate/Permission
### PMU B08 - Revoke Certificate/Permission

### PPG PCG - PC/ pathway (goal-oriented) add
### PPG PCH - PC/ pathway (goal-oriented) update
### PPG PCJ - PC/ pathway (goal-oriented) delete

### PPP PCB - PC/ pathway (problem-oriented) add
### PPP PCC - PC/ pathway (problem-oriented) update
### PPP PCD - PC/ pathway (problem-oriented) delete

### PPR PC1 - PC/ problem add
### PPR PC2 - PC/ problem update
### PPR PC3 - PC/ problem delete

### PPT PCL - PC/ pathway (goal-oriented) query response

### PPV PCA - PC/ goal response

### PRR PC5 - PC/ problem response

### PTR PCF - PC/ pathway (problem-oriented) query response

### QBP E03 - HealthCare Services Invoice Status
### QBP E22 - Authorization Request Status
### QBP Q11 - Query by parameter requesting an RSP segment pattern response
### QBP Q13 - Query by parameter requesting an RTB - tabular response
### QBP Q15 - Query by parameter requesting an RDY display response
### QBP Q21 - Get person demographics
### QBP Q22 - Find candidates
### QBP Q23 - Get corresponding identifiers
### QBP Q24 - Allocate identifiers
### QBP Q25 - Personnel Information by Segment Query
### QBP Q31 - QBP Query Dispense history
### QBP Q32 - Find Candidates including Visit Information
### QBP Z73 - Information about Phone Calls
### QBP Z75 - Tabular Patient List
### QBP Z77 - Tabular Patient List
### QBP Z79 - Dispense Information
### QBP Z81 - Dispense History
### QBP Z85 - Pharmacy Information Comprehensive
### QBP Z87 - Dispense Information
### QBP Z89 - Lab Results History
### QBP Z91 - Who Am I
### QBP Z93 - Tabular Dispense History
### QBP Z95 - Tabular Dispense History
### QBP Z97 - Dispense History
### QBP Z99 - Who Am I

### QCN J01 - Cancel query/acknowledge message

### QRY PC4 - PC/ problem query
### QRY PC9 - PC/ goal query
### QRY PCE - PC/ pathway (problem-oriented) query
### QRY PCK - PC/ pathway (goal-oriented) query

### QSB Q16 - Create subscription
### QSB Z83 - ORU Subscription

### QSX J02 - Cancel subscription/acknowledge message

### QVR Q17 - Query for previous events

### RAS O17 - Pharmacy/treatment administration

### RDE O11 - Pharmacy/treatment encoded order
### RDE O25 - Pharmacy/treatment refill authorization request

### RDR RDR - Pharmacy/treatment Dispense Information
### RDS O13 - Pharmacy/treatment dispense

### RDY K15 - Display response in response to QBP^Q15
### RDY Z80 - Dispense Information (Response)
### RDY Z98 - Dispense History (Response)

### REF I12 - Patient referral
### REF I13 - Modify patient referral
### REF I14 - Cancel patient referral
### REF I15 - Request patient referral status

### RGV O15 - Pharmacy/treatment give

### RQA I08 - Request for treatment authorization information
### RQA I09 - Request for modification to an authorization
### RQA I10 - Request for resubmission of an authorization
### RQA I11 - Request for cancellation of an authorization

### RQC I05 - Request for patient clinical information
### RQC I06 - Request/receipt of clinical data listing

### RQI I01 - Request for insurance information
### RQI I02 - Request/receipt of patient selection display list
### RQI I03 - Request/receipt of patient selection list

### RQP I04 - Request for patient demographic data

### RRA O18 - Pharmacy/treatment administration acknowledgment

### RRD O14 - Pharmacy/treatment dispense acknowledgment

### RRE O12 - Pharmacy/treatment encoded order acknowledgment
### RRE O26 - Pharmacy/Treatment Refill Authorization Acknowledgement

### RRG O16 - Pharmacy/treatment give acknowledgment

### RSP K11 - Segment pattern response in response to QBP^Q11
### RSP K21 - Get person demographics response
### RSP K22 - Find candidates response
### RSP K23 - Get corresponding identifiers response
### RSP K24 - Allocate identifiers response
### RSP K25 - Personnel Information by Segment Response
### RSP K31 - Dispense History Response
### RSP K32 - Find Candidates including Visit Information Response
### RSP Z82 - Dispense History (Response)
### RSP Z84 - Who Am I (Response)
### RSP Z86 - Pharmacy Information Comprehensive (Response)
### RSP Z88 - Dispense Information (Response)
### RSP Z90 - Lab Results History (Response)

### RTB K13 - Tabular response in response to QBP^Q13

### RTB Z74 - Information about Phone Calls (Response)
### RTB Z76 - Tabular Patient List (Response)
### RTB Z78 - Tabular Patient List (Response)
### RTB Z92 - Who Am I (Response)
### RTB Z94 - Tabular Dispense History (Response)
### RTB Z96 - Tabular Dispense History (Response)

### SCN S37 - Notification of anti-microbial device cycle data

### SDN S36 - Notification of anti-microbial device data

### SDR S31 - Request anti-microbial device data

### SIU S12 - Notification of new appointment booking
### SIU S13 - Notification of appointment rescheduling
### SIU S14 - Notification of appointment modification
### SIU S15 - Notification of appointment cancellation
### SIU S16 - Notification of appointment discontinuation
### SIU S17 - Notification of appointment deletion
### SIU S18 - Notification of addition of service/resource on appointment
### SIU S19 - Notification of modification of service/resource on appointment
### SIU S20 - Notification of cancellation of service/resource on appointment
### SIU S21 - Notification of discontinuation of service/resource on appointment
### SIU S22 - Notification of deletion of service/resource on appointment
### SIU S23 - Notification of blocked schedule time slot(s)
### SIU S24 - Notification of opened ("unblocked") schedule time slot(s)
### SIU S26 - SIU/ACK Notification that patient did not show up for schedule appointment
### SIU S27 - Broadcast Notification of Scheduled Appointments

### SLN S34 - Notification of sterilization lot
### SLN S35 - Notification of sterilization lot deletion

### SLR S28 - Request new sterilization lot
### SLR S29 - Request Sterilization lot deletion

### SMD S32 - Request anti-microbial device cycle data

### SRM S01 - Request new appointment booking
### SRM S02 - Request appointment rescheduling
### SRM S03 - Request appointment modification
### SRM S04 - Request appointment cancellation
### SRM S05 - Request appointment discontinuation
### SRM S06 - Request appointment deletion
### SRM S07 - Request addition of service/resource on appointment
### SRM S08 - Request modification of service/resource on appointment
### SRM S09 - Request cancellation of service/resource on appointment
### SRM S10 - Request discontinuation of service/resource on appointment
### SRM S11 - Request deletion of service/resource on appointment

### SSR U04 - specimen status request

### SSU U03 - Specimen status update

### STC S33 - Notification of sterilization configuration

### STI S30 - Request item

### TCR U11 - Automated equipment test code settings request

### TCU U10 - Automated equipment test code settings update

### UDM Q05 - Unsolicited display update message

### VXU V04 - Unsolicited vaccination record update
