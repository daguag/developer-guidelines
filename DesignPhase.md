# Design Phase

During the design phase, the system is designed to satisfy the requirements identified in the previous phases.
The identified requirements need to be transformed into a System Design Document that describes the design of the system which will be used for the implementation of the system.

## Objectives/Goals

The successful completion of the design phase should include:

* Transformation of **all** requirements into detailed specifications covering **all** aspects of the system
* Assessment and mitigation of data security risks
* Assessment and mitigation of privacy risks (infringements of informational self-determination)
[[REM]]("more risks to add?")

## Deliverables

List of deliverables, more detailed information you will find in the sections below:

* Architecture document 
* Planning of test cases and testing schedules [[REM]]("Is test driven development  a hard requirement?")
* Data security risk assessment and mitigations: Document your solutions and your evaluations in order to be able to give an account in case of a review or audit.
    * Where no mitigations are given, justification for the acceptance of security risks is necessary
* Privacy risk assessment and mitigations justification for the acceptance of privacy risks is necessary
* Users of the system need to be informed about known risks and shortcomings of risk mitigations

# Design activities

## System Architecture Document
The system's architecture should give an overview of all physical and logical components of the system and how they interact with each other.

[[REM]]("including the data flows(?)")

A proper documentation about the logical interdependencies and the data flows of the application 
helps you to identify the problematic spots. Spots you have to take into account 
for measuring pitfalls and risks regarding data protection issues.
It also shows where you need special tools to protect users and their privacy -- also to comply with legal obligations (see section Data Protection Impact Assessment below).

[[REM]]("What is needed here essentially? Should we list some issues?")

## Plan test cases and testing schedules
We conceive it as essential to use test-driven development (see also section testing phase).
Experience shows that no one can develop without bugs, and you cannot fully test the functionality of your app manually. However, often changes in one part of the software affect other parts, which usually is overlooked during development. 
For that the best thing is to write test cases which use the functionality of the app.
Think about a schedule for regular testing, in order to find problems early and avoid big trouble.
Write down your plan in order to fully elaborate your cases and schedule.
[[REM]]("find link for reference, in the wiki?")

## Perform Risk Management
[[REM]]("for risk assessment more detailed how to? Assets, attacks, impact, probability...")
Threats and vulnerabilities that exist in the project’s environment or that result from interaction with other systems need to be identified during this phase.
**You cannot consider the design phase complete unless you have a threat model or models that include such considerations.** 

Threat models are critical components of the design phase and reference a project’s functional and design specifications to describe vulnerabilities and mitigations.

In order to assess the risk you need to take into account possible **attacks and threads**.

* Assess the probability of its occurrence 
* Assess the level of harm each thread induces
* Develop tools and measures that address the risks assessed.
* Evaluate if and how the risks are reduced through the measures implemented.


###Code that was created by external development groups in either source or object form.
It is very important to evaluate carefully any code from sources external to your team. Failure to do so might cause security vulnerabilities about which the project team is unaware.

###Threat models that include all legacy code if the project is a new release of an existing program.
Such code could have been written before much was known about software security, and therefore could contain vulnerabilities.
[[REM]]("wording/explain")

### Security Risk Management
The threat models for all functionality identified during the analysis phase need to be completed. Threat models typically must consider the following areas:

* All code exposed on the attack surface and all code written by or licensed from a third party.
* All features and functionality.
* All data flows between components and servers/client
* New features or functionality added in the updated version.

### Privacy Risk Management

Questions that should be addressed during the Privacy Risk Assessment:

* Which personal data is collected?
* What is the compelling customer value proposition and business justification?
* Which notice and consent possibilities are offered?
* What controls are provided to users and enterprises in order to supervise the flow, processing and access of data?
* How is unauthorized access to personal information prevented?

* Which risks are triggered through the storage of data?
  * Which data is stored local on the device?
  * Which data is stored on remote devices?
  * What risks through potential privacy leaks are linked to the place of storage?

In certain cases, like the processing of sensitive data or bulk processing of personal data you are obliged by the GDPR to conduct a Data Protection Impact Assessment. The UK's [Information Commissioner Office](https://ico.org.uk/for-organisations/guide-to-the-general-data-protection-regulation-gdpr/accountability-and-governance/data-protection-impact-assessments/ "ICO UK: Data Protection Impact Assessment") outlined the basic aspects to take into account and offers a checklist for Data Protection Impact Assessments. The French [Commission Nationale de l'Informatique et des Libertés (CNIL)](https://www.cnil.fr) developed an [Open Source tool for conducting Privacy Impact Assessments](https://www.cnil.fr/en/open-source-pia-software-helps-carry-out-data-protection-impact-assesment).


## Common problems in the context of application development
Especially if data is exchanged with 3rd parties you should evaluate the transmission channels and the kind of information which is exchanged.

* Data receiving 
  * How is data collected or received?
  * Are the connections secure?
  * Is metadata generated which might reveal personal information?
  * [[REM]]("add?: is executable code reveived?")

* Data sending
  *  How is data transmitted to other apps and servers?
  *  Are connections secure?
  *  Is it necessary to send the data?
  *  Can the transmission be manipulated?

* Data processing 
  * How is the data used and processed?
  * Are decisions made which might affect the fundamental rights of users and others?
  * Do you build behavioural models which might affect the freedom of action of individuals? [[REM]]("elaborate or examples needed here")

* Interaction with 3rd parties? 
  * In case of interaction, e.g. during paying functions, take into account the 
  * Yes? (z.B. beim Bezahlvorgang (paypal / Kreditinstitut etc.))
    * back to point -> "how can the following steps possibly help?"

    *(Arbeitsnotizen:)*
*(TODO Verbinden von Problemen und technischen Umsetzungsmöglichkeiten. Welche Optionen existieren, wo sind sie angebracht und welche Implikationen haben sie.)*
*(zB Vermeidung eines jeden Datenabflusses, hier gute Beispiele einbringen: Wetterapp, genau oder ungenau, nächste Wetterstation, Rasterung, etc)*
*(-> Designentscheidungen sollen hier wohl überlegt sein.)*
*(Bewertung von Daten? Oder: alle Daten sind immer sensibel?)*
*(-> nur wenn nötig nur für den bestimmten Zweck und nur möglichst sicher verarbeitet....)*
*(als App-Entwickler weiss man gar nicht wo am Ende aggregierte Daten verwendet werden)*

## Technical Measures
Which technical measures can be applied to address the identified risks.
Possible counter measures include:

* Cryptography
* Anonymisation
* Pseudonymisation

*(-> PLib (!) Beispiele sind hier ein guter Anknüpfungspunkt)*

|Legal Hint: "Data Deletion"|
|---|
|An app SHOULD implement a procedure for deleting data, which was been generated by the app or during utilization thereof. This includes accounts, local data, and data stored on the servers of the app provider or on cloud servers.
If no deletion procedure is provided within the app, contact details MUST be provided to ensure the user is able to send a data deletion request to the service provider.|
[comment]:"added from MTD"

**(an jedem Schritt des Design möglichst überlegen wie man hier datenschutzfreundlich umsetzen kann...)**

TODO: Add links and examples
* comment: design decisions... (TODO)

## Organisational Measures

Organisational measures include:
[comment]:"reflexivity, communication, testification"

* Transparency
  * Communication of risks and purpose of data collection to the end user
* Intervenability
  * Means for the end user to delete and modify data
  * which extend functionality is necessary
  * contact person
* Availability
  * SDM (Standard Datenschutz Modell)
* Data minimisation

TODO: Add links and examples

# TODO:
* licence of SDL documents

# Sources
* MS SDL Design Phase: https://msdn.microsoft.com/en-us/library/windows/desktop/cc307414.aspx
* Appendix C - SDL Privacy Questionaire: https://msdn.microsoft.com/en-us/library/windows/desktop/cc307393.aspx
* http://doit.maryland.gov/SDLC/Documents/SDLC%20Phase%2005%20Design%20Phase%20Single%20Custom.pdf
* http://infolab.stanford.edu/~burback/watersluice/node11.html
