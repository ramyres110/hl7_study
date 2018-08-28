# HL7 v2.7

## Message Type

### 1. ACK - Acknowledge
There are two types of Acknowledgement messages (ACKs) used in healthcare data exchange communications:
ACKs (including original mode acknowledgements and enhanced mode acknowledgements) and non-HL7 ACKs (also known as static string acknowledgements).

- **Original Mode Acknowledgement** – a “Receive” ACK, and 95% of the ACKs used in HL7 communications; indicates that a message has been received but not necessarily processed yet.
- **Enhanced Mode Acknowledgement** – an “Application” ACK that is a resultant status return rather than a communication response (i.e. query results, order response, etc.).
- **Non-HL7/Static String ACK** - is a custom acknowledgement, and is simply a text string (rather than an HL7-formatted ACK). These types of ACKs are used when a system is not receiving HL7 messages, and therefore cannot use the HL7 message information to automatically populate an HL7-formatted ACK.

##### Structure
```typescript
interface Acknowledge{
    MSH:MSH,//Message Header
    SFT?:SFT,//Software Segment
    UAC?:UAC,//User Authentication Credential Segment
    MSA:MSA,//Message Acknowledgment
    ERR?:ERR//Error
}
```

##### Ex:
Receive
```batch
MSH|^~\&|MegaReg|XYZHospC|SuperOE|XYZImgCtr|20060529090131-0500||ADT^A01^ADT_A01|01052901|P|2.5
EVN||200605290901||||200605290900
PID|||56782445^^^UAReg^PI||KLEINSAMPLE^BARRY^Q^JR||19620910|M||2028-9^^HL70005^RA99113^^XYZ|260 GOODWIN CREST DRIVE^^BIRMINGHAM^AL^35 209^^M~NICKELLâS PICKLES^10000 W 100TH AVE^BIRMINGHAM^AL^35200^^O |||||||0105I30001^^^99DEF^AN
PV1||I|W^389^1^UABH^^^^3||||12345^MORGAN^REX^J^^^MD^0010^UAMC^L||678 90^GRAINGER^LUCY^X^^^MD^0010^UAMC^L|MED|||||A0||13579^POTTER^SHER MAN^T^^^MD^0010^UAMC^L|||||||||||||||||||||||||||200605290900
OBX|1|NM|^Body Height||1.80|m^Meter^ISO+|||||F
OBX|2|NM|^Body Weight||79|kg^Kilogram^ISO+|||||F
AL1|1||^ASPIRIN
DG1|1||786.50^CHEST PAIN, UNSPECIFIED^I9|||A
```
Response
```batch
MSH|^~\&|SuperOE|XYZImgCtr|MegaReg|XYZHospC|20180828185109||ACK|ACK20180828185109|P|2.3
MSA|AA|01052901
```

***MSA**: Message Acknowledgment Segment
***AA** = Acknowledgment Code from table  0008: Acknowledgment Code.
***01052901** = Message Control Id

