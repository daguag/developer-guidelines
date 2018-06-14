# Planning Phase

Before you start to code, carefully plan your app: what purpose is it for? 
Which functions will be needed, what are the use cases?
What kind of data do you need to fulfill the purpose of the app.

In order to testify you carefully weighed the use and necessity of data, you need to document your decisions in a separate document. This will also help you to reconsider your design decisions in a later development phase.

## Defining the Purpose and Functionality of the App

### The App's Purpose

What will the app do for the end-user? 
It might seem obvious, but **it is a good start to take a moment and reconsider what the actual aim of the app is**.

- Which functions should the app provide and
- which user data is necessary for the planned functionality.

Especially it is important to carefully think which user data is needed and how it will be processed.


**Determining the purpose is important for deciding upon the functionality that may be included in the app, and if and how user data needs to be processed.**
<br>


| "Legal Hint" - Purpose Binding  |
|---|
|   Personenbezogene Daten dürfen aufgrund Art. 5 Abs. 1 b der Datenschutz-Grundverordnung (DSGVO) nur für festgelegte, eindeutige und rechtmäßige Zwecke verarbeitet werden. Wenn dies erfüllt ist, ist weiter zu beachten: die Daten dürfen nach Art. 5 Abs. 1 c DSGVO nur so weit verarbeitet werden, wie es angemessen und erheblich ist für den Zweck. Es dürfen also nicht mehr Daten verwendet werden als nötig, nicht länger als nötig und die Verarbeitung darf nicht weiter gehen als nötig. |



<br>

| "Example" - Purpose Binding |
|---|
| For example a weather app might let you choose and display weather information; a firewall app might let you inhibit or monitor a smartphone's connections to the internet. <br> 
For this functions certain user data might be necessary or useful like geo-data to give the weather data for the corresponding location or access to the data connections in order to detect malicious data flows. <br>
However the access to this data has strong implications to the users privacy which need to be taken into account at an early stage of development for proper integration of security measures. There are cases where users do not want their whereabouts to be known to certain indiviuals or groups, such as in the case of policital dissidents in authocratic regimes, or if individuals want to be left alone or * |

<br> 

| "Reference" - Purpose Binding |
|---|
| For further information have a look in the  ENISA Report on Privacy and data protection in mobile applications p. 55 |

<br>

### Intended and Unintended Ways to Use the App

- [ ] is the unintended use a main issue here?

When planning the application design, not only the obvious purpose you intended for the app should be taken into account, but also alternative ways to use the app which can have an impact on the user other users of the device.

*For example a firewall app can give you information about other apps' illegitimate connections to the internet. Yet it might also give end users a tool to secretly record and monitor other users' internet activities.*

[comment: better example: babyphone / tracking to spy on users instead of monitor child care]

**Be creative about potentially harmful ways to use of your app. Think about safeguards against illegitimate uses.**

*For example in the case of a firewall app a notification about the monitoring activity in the background would give the user transparency.*

Not only people with physical access to the device can make use of the app, and the data generated. Other apps might have access to shared memory, service providers might use the data in unintended ways, and finally governments might get access to data stored by the service providers or on the device.

*For example third party apps might get access to pictures taken on political manifestations, or governments might be interested in the social-graph included in the contact list or regular whereabouts to trace political opponents.*

**The safest data is data which is not collected or stored.**

## Defining the App's Functionality and Permissions

A privacy-friendly app will only include functionality and permissions that is needed to serve the purpose determined in the beginning.

**Think carefully about which permissions are essential for providing the functionality.**

*An app providing location based services does not need to access the device's microphone to do so.*

Ideally any permissions that are not strictly necessary to serve the intended purpose should be avoided. Any need for permissions must be explained and justified in a comprehensible way. Take into account that users have no deeper understanding of the dependencies and technical necessities. Only if they really understand why and how the permission is used they can actually give a real consent.

| BOX: "Legal hint" - Legitimate grounds for the processing of personal data |
|---|
| ADD TEXT HERE|


## Defining the sort of data to be used

There are different categories of data which are relevant for the use of the app.

 - **Primary Data: Pre-existing data**: Data related to the end-user or to other data subjects concerned. Be aware that on the device might be data which the user has no right to give third parties access to, for instance contact data or pictures of other persons.

 - **Secondary Data: User generated data**: Data will be produced while the app is running. This might be user content (e.g. messages), log data, data related to payment, statistics to authorizing access or other. These will also contain personal data that require protection and thus need to be specified and assessed.

| BOX: is there a legal reference here? |
|---|
| THEN ADD IT HERE |

## Privacy Policy and Terms of Use

Be aware, that in order to provide transparency about which data of the user is collected and how it is processed and who has access to it, you will need to provide an understandable description and give the user access to its data and options about the ways of processing it.

|BOX: "Legal hint" - Policies and User rights |
|---|
|ADD TEXT HERE| 

---
END OF DOCUMENT

---

###Things to add:
 - [ ] Check Laws and Regulations applicable to your specific sector of industry

 - [ ] Rights and obligations to erase the data collected -> in the analysis and design phase

###Pastebin

####former sections:

 - [ ] Data Subjects - reference to glossary

 - [ ] <del>Processes</del>

 - [ ] Responsibilities - legal hint here?

 - [ ] Communication of Purpose / Data Processing Requirement and Protection Measurements



