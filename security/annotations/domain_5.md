# RISK MANAGEMENT

## 5.3 - (1.2u) CIA triad

### REVIEW

---
## 5.3 - (1.4u) - what is risk?
> Goal of cybersecurity is to protect your stuff from bad things. >> we do this applying 'Risk management'

### ASSETS
> Assets are any part of organisation that we're worried to getting harm (people, computers, ideas, reputation)

### VULNERABILITY
> Weakness to an asset that lives open to bad things happening to it

### THREATS
> Threat is a discovered action that exploits the vulnerability's potential to do an harm to an asset

### THREAT AGENT
> Agent that initiates a threat (hacker, hurricane)

### LIKELIHOOD
> Defines the level of of certainty that something will happen (in one year, what is the likelihood to this bad thing happen?) 

### QUANTITATIVE LIKELIHOOD
> What is a percentage (%) chance that I'm gonna loose my power supply?

### QUALITATIVE LIKELIHOOD
> How do I measure custumer loyalty?

### IMPACT
> Is the harm caused by a threat

## threats x vulnerabilities = risk

## THREATS -> VULNERABILITIES = RISK
> *Threats* applyed to *Vulnerabilities* is equals *Risk*

*National Institute of Standards and Security* Guide for Conducing Risk Assessments

- [NIST SP 800-30](https://nvlpubs.nist.gov/nistpubs/legacy/sp/nistspecialpublication800-30r1.pdf)

### REVIEW 

- Threats exploits vulnerabilities to harm assets
- Assets can have vulnerabilities
- Use SP 800-30 as part of risk assessment

---
## 5.2 (1.5u) - Managing Risk

Catalog all assets and determine what are a threat and vulnerabilities

**Risk management:**

- Vulnerability assessment
- Threat assessment

Documented in [NIST SP 800-37](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-37r1.pdf)

**CVEs (*Common Vulnerabilities and Exposures*)** - details vulnerabilities [cve.miltre.org]

**Finding vulnerabilities:**
1. PENTEST (GOLD STANDARD)
2. Nessus Scanning

### THREAT ASSESSMENT

- **Adversarial:** hacker, malware, somebody intentionally doing a bad thing
- **Accidental:** people who have rights and permissions using incorrectly or accidentally, hitting a wrong command, plug wrong cables, that causes e.g. an DB to corrupt
- **Structural:** equipment, software failures
- **Environmental:** Hurricanes, earthquakes, AC going out and it starts a fire

> OK, I've just defined my threat assessment and risks, so now?

### RISK RESPONSE
> Apply mitigation on those risks

### RISK MITIGATION
> Apply some effort that will reduce the impact of a risk

### RISK TRANSFERENCE
> Offload of the likelihood, risks and impact on a third party
> e.g. instead of monitoring my own web server, i'm gonna use a cloud based service. 

### RISK ACCEPTANCE
> Likelihood and impact of the risk is less than the cost of trying to mitigate that risk
> e.g. accept the risk of a meteor hit your data center, doesn't worths the protection

### RISK AVOIDANCE
> when the organisation must deal with the whole process of risk management, as a result of an legal obligation in case of an incident.
> e.g. if a company that sells bananas require custumer data for the payment, they will have to deal with the risks, so they simply don't require it to avoid the risk

### FRAMEWORK
> A workflow/methodology of process that helps you a security professional deal with **RISK MANAGEMNET**

- [NSIT SP 800-37](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-37r1.pdf)
- [ISACA RISK IT FRAMEWORK](https://www.isaca.org/Knowledge-Center/Research/Documents/Risk-IT-Framework-Excerpt_fmk_Eng_0109.pdf)

### REVIEW
- Threat assessment finds threats applicable to your infrastructure
- Threats come in four groups: adversarial, accidental, structural, environmental.
- Mitigation is used to reduce impact of risk

---

## 5.7 (1.7u) - SECURITY CONTROLS


### REVIEW

---
## 5.7 (1.8u) - INTERESTING SECURITY CONTROLS

> They are not common security controls that could be bought

- **Mandatory vacation:** used to detect fraud, unauthorized activity, gather clues during investigation.
- **Job rotation:** it keeps people happy about their job dismotivating them to do naughtiness.
- **Multi-person control(to accomplish a task):** it prevents one person on initiate an action that could be bad. Also make sure that multiple people ensure is done in a right way.
- **Separation of duties (adm control):** ensures that not a single individual should not perform all critical privileged duties across the board.
- **Principle of Least Privilege:** ensures that individuals have only approved privileges necessary for the to perform their job.

### REVIEW

- Mandatory vacation is a type of security control to detect vulnerability or unauthorized activity
- Multi-person control allows for check and balances of critical funcitons.
- Principle of Least privilege is set to resource access to what is only necessary to perform the job.

---
## 5.7 (1.9u) - Defense in Depth
*Compare and contrast various types of controls*

### Diversity vs Redundancy
> Redundancy is the same security control (or whatever that applies to it) in a layered fashion.
> Diversity is a different type of control in the game. 

**Examples**
Anti-malware system in different places
- Individual systems
- Network based intrusion detection
- block type of malware in ACL on the firewall
*Redundancy*

Different Internet Provider
- Main provider Comcast
- Second provider AT&T
*Diversity*

### DIVERSITY:
Use a variety of of controls:

- physical
- administrative
- technical

> E.G.: Vendor diversity is a type of technical control in depth. (**TECHNICAL CONTROL**)

> E.G.: I dont want people login computer in certain times.
> I could setup my windows server to block the user to login (**TECHNICAL CONTROL**)
> OR
> I can simply assign people to a different shift (**ADMINISTRATIVE CONTROL**)

> E.G.: I dont want people using facebook during their company time.
> I could block facebook.com right on my firewall (**TECHNICAL CONTROL**)
> OR
> I can setup an use policy saying "YOU SHOULD NOT USE SOCIAL MEDIA DURING BUSINESS HOURS!" (**ADMINISTRATIVE CONTROL**)
*very diverse and different types of controls achieving the same goal*

### REVIEW

- Whenever applying security in depth, make sure you have good DIVERSITY
- Redundancy is repeating the same controls at various intervals
- Diversity is using a variety of controls in a random pattern
- Defense in depth uses *administrative*, *physical* and *technical* controls.
- Vendor diversity is a method of defense in depth with technical control

---
## 5.1 (1.10u) - IT Security Governance
*Explain the importance of policies, plans and procedures related to organizational security.*

Where do security policies come from?

### GOVERNANCE
> Set of overarching rules that define how an organization and its personnel conduct themselves.

### IT SECURITY GOVERNANCE
> Set of overarching rules that define how an organization and its personnel conduct their **IT SECRUTIY**.

### SOURCES TO SET THE RULES
1. Laws and Regulations (e.g. HIPAA)
2. Standards
   * 2.1. Government Standards (NIST - ISO)
   * 2.2. Industry Standards (PCI-DSS)
3. Best Practices
4. Common Sense

### POLICY
>A document that defines how a job gonna be performed.
- Broad in nature (generalization)
- Used as directives (we will do this, we will do that)
- Define roles and responsabilities (Security Sector will be composed with 1 CSIO, 3 Security Engineers under etc...)

### ORGANIZATION STANDARD
- More detailed (defines the level of a policy)

### "SECURITY CONTROLS COME FROM THE POLICIES AND STANDARDS"

### - NOW, HOW TO DO IT?

### PROCEDURES
- step-by-step on how to do it.

### HOW IS COMPOSED THE GOVERNANCE
> take the **SOURCES** and begins to build **POLICIES** and **STANDARDS**, then end with **PROCEDURES** that tell us how-tos

### GUIDELINES
- Guidelines are optional
> Unlike everying else above
> considered somthing optional, an idea
> doesnt have to be cleary defined
> just how we tend to do things

### REVIEW
- Security controls are defined within the polcies and standards
- Sources of IT Governance come from Laws & Regulations, industry, best practices, and internal standards
- Policies, Security Controls and Standards help define and build procedures.
  
---
## 5.1 (1.11u) - Security Policies
*Explain the importance of policies, plans and procedures related to organizational security.*

### IMPORTANT POLICIES THAT WILL BE COVERED IN SECURITY+

### ACCEPTABLE USE POLICY
> AUP defines what a person can or can not do when using company assets

- Personal use of the computer
- not sell/buy stuff on internet during company hours
- can't look pornography
- where you can store stuff, where you can't

### DATA SENSITIVITY AND CLASSIFICATION POLICIES
> Data Classification define the importance or nature of the data

> Each organization will classify their own data sensitivity (CONFIDENTIAL, HIGHLY CONFIDENTIAL)

> It gives an idea for people of the importance of data

### ACCESS CONTROL POLICIES
> Defines HOW people get access to our data.

> Defines what type of data do users have access to. (could be defined on job titles)

### PASSWORD POLICIES
> Defines how we deal with passwords.

- Password recovery
- Bad Login (wrong password too many times)
- password retention
- password reuse

### CARE AND USE OF EQUIPMENT
> How users are maintaining their equipment
custumer

### PRIVACY POLICIES
> Privacy policies are often for customers as well as just in hause.

- Basically, when google/facebook says that will use your data to offer you costumized advertise

- When in house, ok! But when comming from these webapps, ensures that you read every single line

### PERSONNEL POLICIES
> Has to do with people that are dealing with our data.

- Mandatory vacation
- Job Rotation

### REVIEW
- Access Control Policy addresses data access and classification restrictions
- Given a scenarion, be able to describe the correct policy for a situation
- Privacy Policies define how your data, or data usage will be shared with other resources.

---
## 5.3 (1.13u) - Quantitave Risk Calculations
*Explain risk management processes and concepts.*

---
## 5.2 (1.14u) - Business Impact Analysis
*Explain the importance of policies, plans and procedures related to organizational security.*

---
## 5.8 (1.15u) - Organizing Data
*Given a scenario, carry out data security and privacy practices.*

---
## 5.1 (1.16u) - Security Training
*Explain the importance of policies, plans and procedures related to organizational security.*

---
## 5.1 (1.17u) - Third Party Agreements
*Explain the importance of policies, plans and procedures related to organizational security.*
