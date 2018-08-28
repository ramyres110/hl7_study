# HL7 v2.7

## Message Type

### 2. ADT - Admit, Transfer and Dischard
HL7 ADT messages carry patient demographic information for HL7 communications but also provide important information about trigger events (such as patient admit, discharge, transfer, registration, etc.). 
Some of the most important segments in the ADT message:

- **PID** (Patient Identification) segment, the
- **PV1** (Patient Visit) segment, and occasionally the 
- **IN1** (Insurance) segment.

ADT messages are extremely common in HL7 processing and are among the most widely used of all message types.
ADT messages communicate patient demographic and visit information, as well as the reason why the message is being sent.
There are _51_ different types of ADT messages that are used for various trigger events

For instance, an ADT-A01 (patient admit) message might be sent to an Emergency Department system while an ADT-A04 (patient registration) message might be sent to an HIS system. The level of urgency and pace at which the message is transmitted might also be different depending on the trigger event.

### Triggers

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
interface ADT_A04{
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
    PR1:PR1,
    ROL?:ROL,
    GT1?:GT1,
    IN1:IN1,
    IN2?:IN2,
    IN3?:IN3,
    ROL?:ROL,
    ACC?:ACC,
    UB1?:UB1,
    UB2?:UB2,
    PDA?:PDA,
}
```
#### ADT A05 - Pre-admit a patient
```typescript
interface ADT_A05{
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
    PR1:PR1,
    ROL?:ROL,
    GT1?:GT1,
    IN1:IN1,
    IN2?:IN2,
    IN3?:IN3,
    ROL?:ROL,
    ACC?:ACC,
    UB1?:UB1,
    UB2?:UB2,
}
```
#### ADT A06 - Change an outpatient to an inpatient
```typescript
interface ADT_A06{
    MSH:MSH,
    SFT?:SFT,
    UAC?:UAC,
    EVN:EVN,
    PID:PID,
    PD1?:PD1,
    ARV?:ARV,
    ROL?:ROL,
    MRG?:MRG,
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
    PR1:PR1,
    ROL?:ROL,
    GT1?:GT1,
    IN1:IN1,
    IN2?:IN2,
    IN3?:IN3,
    ROL?:ROL,
    ACC?:ACC,
    UB1?:UB1,
    UB2?:UB2,
}
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