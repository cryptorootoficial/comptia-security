# THREATS, ATTACKS AND VULNERABILITIES


## 1.1 - Given a scenario, analyze indicators of compromise and determine the type of malware.

<details closed>
<summary>Content</summary>
<br>
<pre>
<img src="../../images/1.1.png">
</pre>
</details>
<br>

**Udemy videos:**

- [x] *5.61 - MALWARE*
- [x] *9.115 - ATTACKING APPLICATIONS*

#### VIRUS

- Attached to files
- Propagate
- Spread other devices
- Activation

#### ADWARE

- Tries to put Ads up

#### SPYWARE

- Hide itself
- Tracks what user does
- Steals cookie information

#### TROJAN HORSE / TROJANS

- Running through something nice
- Don't propagate on their own

#### RATs (Remote Access Trojans)

- Same as a common trojan
- It doesn't do anything naughty until somebody in a remote location turns it on something bad

#### RANSOMWARE / CRYPTOMALWARE

- Locks the system through cryptography
- Asks for money to unlock

#### LOGIC BOMB

- Similar to RATs
- It doesn't propagate
- It has to be activate

#### ROOTKITs

- Grabs administrative privileges 
- Escalates privileges to execute other things
- Challenging to detect

#### BACKDOOR

- Breach intentionally left to get access

#### POLYMORPHIC MALWARE

- Malware that changes itself
- Tries to mislead anti-malware softwares

#### ARMOURED VIRUSES

- Hard for anti-malware to detect, due confusing memory allocations

#### KEYLOGGERS

- Records keyboard typing information

#### INJECTION ATTACKS

when some extra input (code) is added into an application through its forms.

#### SQL

- `inner join`
- `select from`
- `insert into`

#### LDAP Injection

- Query directories
- based on X.500 auth protocol

```
DN = Distinguished Name
CN = Common Name
OU = Organization Unit
DC = Domain Component
```

#### Buffer Overflow

![buffer overflow](../../images/bf.png)

**Buffer:**

> is a part of memory that sets aside to store data before it actually get put into the application itself.

### REVIEW 1.1

- Viruses do things to files and propagate, 
- Malware collects keystrokes and information
- Ransomware and logic bombs can devastate systems
- Polymorphic and Armoured malware are hard to detect and destroy
- Injection attacks is the inserting into an application )code injection, command injection, etc.)
- LDAP is based on the x.500 protocol
- Buffer and integer overflow attacks are inputs into applications forms that exceed the maximum allowed bits.

---

## 1.2 Compare and contrast types of attacks.

<details closed>
<summary>Content</summary>
<br>
<pre>
<img src="../../images/1.2.png">
</pre>
</details>
<br>

**Udemy videos:**

- [x] *5.47 - Denial of Service*
- [x] *5.48 - Host Threats*
- [x] *5.49 - Man in the Middle*
- [x] *7.78 - Living in Open Networks*
- [x] *7.79 - Vulnerabilities with Wireless Access Points*
- [x] *9.112 - Social Engineering Principles*
- [x] *9.113 - Social Engineering Attacks*
- [x] *9.114 - Attacking Web Sites*

## DoS

> Tries to DENY any kind of service (Web, Email, DNS etc).

### 1. Volume attack

> Not doing something naughty, it just does a lot of it.

***Examples:***

- **PING FLOOD**

A machine starts to send tons of `pings`.

- **UDP FLOOD**

A machine starts to send all kinds of UDP requests to different ports.

### 2. Protocol attack

> It misleads a communication with a particular protocol.

***Example:***

- **SYN Flood / TCP SYN Attack**

Clint send a lot of SYNs, and servers needs to answer SYN/ACK, but client never responds.

### 3. Application Attack

> Do naughtiness to a communication Application.

***Examples:***

- **SLOW LORIS ATTACK**

Client starts a normal communication with an APACHE WEBSERVER, and then stop to talk.
After that, it opens new communications.

- **APPLIFICATION**

I.E. SMURF ATTACK: Attacker spoofs the victim (apache) IP and it sends an ICMP package via broadcast.
So that, everybody starts to respond to the real IP breaking down the service.

### DDoS (Distributed)

> Bunch of computers attacking simultaneously

### BOTNETS

Pre infected computers (Zombies) controlled by a remote attacker to cause DDoS.

### SPAM

- unsolicited email
- not consider a threat in most of cases.

### PHISHING

- a spam
- tries to get information
- generic way

### SPEAR PHISHING

- phishing but more specific, like i.e. the attacker know your name

*Usually Phishing and Spear Phishing came from other sources, but for the exam SIMPLIFY IT TO EMAILS.*

### SPIM

- receive spam via instant messaging (whatsapp, facebook etc).

### VISHING

- voice messaging trying to bring urgency for the victim aiming information gathering.

### CLICKJACKING

- ad windows that moves and difficult user to close or click.

### TYPO SQUATTING & DOMAIN HIJACKING

- register domains that takes advantage of people mistyping. i.e. `www.gogle.com` or `fcebook.com`.

### PRIVILEDGE ESCALATION

- Attackers tries to get higher power across the system.

### MAN-IN-THE-MIDDLE

- Aims gather data (username, passwords etc.)

Could be perform via:

- Spoofing (IP, DNS spoofing...)
- Ettercap
- TCP Dump
- Wireshark
- Typosquatting
- Domain Hijacking *
- Replay Attack
- Downgrade attack *
- Firesheep *
- Session Hijacking (don't know how it works)

## REPLAY ATTACKS

### Cookie Cadger

when the attacker intercepts authentication cookies to REPLAY the login process with the stolen cookies.

### SSL Stripping

Attackers downgrade HTTPS by intercepting the traffic and user replies the server in a plaintext form.

**Protecting the assets:**

- Use secure protocol on unsecure networks
- Use https on Web sites that collect information
- Use VPN in non-secure environments

### HSTS (HTTP strict transport security)
- when the server requires the user's browser to use HTTPS

### Rogue Access Point (Rogue AP)

Access point with no authorization

### Evil Twin

Fraudulent wireless access point that masquerades as a legitimate AP.
Can be followed by a MITM attack by filtering all the traffic from the people connected on attackers fraudulent AP.

### Deauthentication attack

Gather info of the network clients and tell to disconnect and connects to an evil network.

## Social Engineering

People tricking people :)

### Principles:

- **Authority:** To impersonate or imply a position of authority
- **Intimidation:** to frighten by threat
- **Consensus:** To convince of a general group agreement
- **Scarcity:** To describe a lack of something
- **Familiarity:** To imply a closer relationship
- **Trust:** To assure reliance on their honesty and integrity
- **Urgency:** To call immediate action

## LOGS

*Exam will challenge the ability to read log files.*

### CLF (Common Log Format)

```
127.0.0.1 - - [10/Oct/2017:10:05:24 - 0600] "GET /CompTIA09_small.gif HTTP/1.0" 200 42213"
```

- **Host** - the fully qualifies domain name of the CLIENT, or its IP.
- **Ident** - If the IdentifyCheck directive is enabled and the client machine runs ident, then this is the identity information reported by the client.
- **Authuser** - If requested, URL requires a successful basic HTTP authentication then the username is the value of this token.
- **Date** - Date and Time (GMT)
- **Request** - The request line from the client enclosed in double quotes ("_").
- **Status** - The three-digit HTTP status code returned to the client
- **Bytes** - The number of bytes in the object returned to the client excluding all HTTP headers.

### cPanel

If configured, it sends admins emails when scary things goes up.

```
Time: -------
PID: 3948 (Parent PID: 2934)
Account: Admin25
Uptime: 62 seconds


Executable:
/usr/local/bin/php
Command Line (often faked in exploits):
/usr/local/bin/php/home/totalcentral/public_html/generator/runcrawl.php
Network connections by the process (if any):
TCP: 74.26.29.16:36864 -> 74.26.29.16:80
```

## Web applications attacks

### Cross-site scripting (XSS)

Client-side script injected into trusted web sides.
When somebody tries to get another person to run a script from another site.

```
`<script>source=http://evilsite</script>
```

### XML injection

Used to manipulate or compromise the logic of an XML application or service.
Insert XML information that shouldn't be there.

```
http://www.example.com/Newuser.php?user=mike&password=12345&product=VoucherGeneric&price=450&email=mike@totalsem.com
```

With an evil tool the attacker can perform XML injection and be able to modify a field that is filled automatically, e.g. the **price**:

```
http://www.example.com/Newuser.php?user=mike&password=12345&product=VoucherGeneric&price=50&email=mike@totalsem.com
```

### REVIEW 1.2

- Denial of Service attacks prevent others from accessing a sustem
- Distributed Denial of Service uses multiple systems to attack a single host
- Denial of Service attacks can broadly be broken down into volumetric, protocol and application attacks
- Phishing is unsolicited emails that typically request information from you.
- Visher is voice-based (voice + phishing) solicitations requesting information about you that is confidential
- To start a man-in-the-middle attack a third-party must "get in the middle".
- Once an attack is successful you must use all information obtained.
- The type of network can make the man-in-the-middle attack easier or more difficult.
- Open networks are dangerous because they are insecure
- Understand how an attacker can get your information and use it against you
- Use encryption protocols to prevent these attacks
- Rogue access points can be accidental, but evil twins are intentional
- 802.11 jammers are illegal, but can knock anyone off a network
- Rogue access points and evil twins can cause a lot of headaches
- Social engineering principles are focused more on people's behaviour as opposed to their physical actions
- Be comfortable with these principles and how each are applied
- Never give out any sensitive information
- Recognize the different types of social engineering attacks
- Practice save processes to prevent these attacks
- Cross-site scripting (XSS) is a common type of injection attack that affects web sites and web applications
- XML injections are very small changes that have big consequences

---

## 1.3 - Explain threat actor types and attributes.

<details closed>
<summary>Content</summary>
<br>
<pre>
<img src="../../images/1.3.png">
</pre>
</details>
<br>

**Udemy videos:**

- [ ] *1.3 - Threat Actors*

### REVIEW 1.3

---

## 1.4 - Explain penetration testing concepts.

<details closed>
<summary>Content</summary>
<br>
<pre>
<img src="../../images/1.4.png">
</pre>
</details>
<br>

**Udemy videos:**

- [ ] *9.116 - Exploiting a Target*

### REVIEW 1.4

---

## 1.5 - Explain vulnerability scanning concepts.

<details closed>
<summary>Content</summary>
<br>
<pre>
<img src="../../images/1.5.png">
</pre>
</details>
<br>

**Udemy videos:**

- [ ] *9.111 - Vulnerability Scanning Assessment*

### REVIEW 1.5

---

## 1.6 - Explain the impact associated with types of vulnerabilities.

<details closed>
<summary>Content</summary>
<br>
<pre>
<img src="../../images/1.6.png">
</pre>
</details>
<br>

**Udemy videos:**

- [ ] *9.117 - Vulnerability Impact*

### REVIEW 1.6
