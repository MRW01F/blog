---
title: SS7 & Why Everyone Should Know About It
published: true
---

<center><img width="1000" height="500" align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7.jpg"></center><br>

# What Is SS7 (OpenSS7)

OpenSS7 is a telephone network and next generation network Signalling System No. 7 (SS7) and Signalling Transport (SIGTRAN) protocol stack which provides source under AGPL-3.0. See what it is not.

OpenSS7 started as an open-source implementation of the Signalling System Number 7 protocol stack as specified by ITU-T, ETSI, ANSI, and other standards bodies. It derives primarily from an implementation of the ITU-T Q.700-Series Recommendations on Signalling System No. 7. For more information on Signalling System Number 7, see [Where can I find more information on SS7?](http://www.openss7.org/faq12.html) It has since evolved to encompass a wide range of communications protocols and network functions necessary for building advanced signalling and switching systems.

OpenSS7 was developed for the Linux kernel. It currently supports the 2.4, 2.6 and 3.x series kernels. OpenSS7 includes driver implementations for popular Linux WAN cards, and driver implementations are supported separately by the card vendor. For more information on which cards are supported, see [What hardware is supported?](http://www.openss7.org/faq10.html)

# Why SS7 Is not Just Any Protocol

Global mobile use has been on a major upswing for quite some time. From toddlers who learn to operate a mobile phone before they can even speak to professionals whose phones contain sensitive information. Mobile devices are now like opinions: everyone has at least one they hold very dear.

As 5G technology propagates and expands to reach new audiences and devices, the opportunities for mobile cyber attacks grow exponentially. While the YouTube browsing history of a toddler may be of little interest to hackers, anyone holding sensitive data or communicating privileged information is at risk. All thanks to legacy network protocols of global telecommunications.

The aging of legacy protocols with the evolution of hacking techniques create the perfect conditions to empower malicious activities on increasing crowded mobile networks. So it’s no wonder mobile malware attacks increased by 50% in 2019, and in 2020 are expected to continue to wreak mobile security havoc at an exponential rate.

Let’s meet one of the most prominent mobile network vulnerabilities threatening mobile service providers and users in the past years: SS7 loopholes.

Rather than target specific devices, sophisticated attacks are being perpetrated on entire networks. From a mobile service provider perspective, once your network’s SS7 protocol is successfully compromised, hackers are privy to your subscriber’s personal information. They can access text messages, phone calls, track device location, and all without your or the subscriber’s knowledge.

# How Does SS7 Work

The set of SS7 telephony signaling protocols is responsible for setting up and terminating telephone calls over a digital signaling network to enable wireless cellular and wired connectivity. It is used to initiate most of the world’s public telephone calls over PSTN (Public Switched Telephone Network).

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_2.jpg"></center><br>

Over time other applications were integrated into SS7. This allowed for the introduction of new services like SMS, number translation, prepaid billing, call waiting/forwarding, conference calling, local number portability, and other mass-market services.

Components and elements that make up the SS7 Protocol Stack –

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_3.jpg"></center><br>

# What are SS7 attacks?

SS7 attacks are mobile cyber attacks that exploit security vulnerabilities in the SS7 protocol to compromise and intercept voice and SMS communications on a cellular network. Similar to a Man In the Middle attack, SS7 attacks target mobile phone communications rather than wifi transmissions.

# How do SS7 attacks work?

SS7 attacks exploit the authentication capability of communication protocols running atop the SS7 protocol to eavesdrop on voice and text communications. According to telecommunications experts, all a cyber criminal would need to successfully launch an SS7 attack are a computer running Linux and the SS7 SDK – both free to download from the Internet.

Once connected to an SS7 network, the hacker can target subscribers on the network while fooling the network into thinking the hacker device is actually an MSC/VLR node.

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_4.jpg"></center><br>

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_5.jpg"></center><br>

# How do they Attack?

In order to attack, You need to dig deeper to find a suitable provider for your network.

> SigPloit, a signaling security testing framework used to exploit vulnerabilites in the signaling protocols

### 1.1 Installing SigPloit

```shell 
cd SigPloit

sudo pip2 install -r requirements.txt

python sigploit.py
```

### 1.2 Selecting the Module as SS7

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_6.jpg"></center><br>

### 1.3 Setting the options: client_pc, serve_pc, client and server IP, port, MSISDN (phone number)

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_8.jpg"></center><br>

### 1.4 Capturing packets from any packet analyzer

### 1.5 Gathering Information using “ HackRF one ” hardware tool.

<br>

# Hacking Whatsapp:

Let’s consider the Example of Whatsapp, where over 1 billion people in over 180 countries use daily. Although the Application is End-to-End Encrypted, the account verification for WhatsApp is still done via SMS or Mobile Call. Hackers use this as their advantage and target the SS7 network.

In this case, if the hacker gives your phone number to his phone’s WhatsApp account and also intercept your SMS verification messages through SS7 attack, it would be easy for him to access your account.

> Still, its considered as one of the “Zero-day attack” and its vulnerable at its peak.

# How to Survive the SS7 Attack?

Experts Suggest implementing a new methodology for the replacement of SS7 networks. But it was said that SS7 Vulnerability is not a Flaw, It was designed that way.

Later, A German Cybersecurity researcher came up with an Android application:

> SnoopSnitch, that would collect and analyze mobile radio data to make you aware of your mobile network security and to warn you about threats like fake base stations, user tracking, and SS7 attacks.

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_9.jpg"></center><br>

To install this application, the phone has to be rooted. Root privileges will be needed to collect mobile network data.

Currently, SnoopSnitch is compatible only with Android phones.

These are the web links that describe the incident happened on the loophole of SS7 Networks:

> Bank theft in O2-Telefonica Company, UK <br>
> Telecom confirms SS7 abuse in German

Although SS7 Attacks cannot be prevented from attack it can, however, be detected in Network Function Virtualisation using Machine Learning.

# Detecting SS7 Attack using ML

This is a research paper contributed by Tooba Qasim & Team, Pakistan.

<center><img align="center" src="{{ site.baseurl }}/assets/images/ss7/ss7_10.jpg"></center><br>


* Their idea was to apply Machine learning in SS7 network data obtained through packet analyzer
* It is then exported as CSV file to preprocess the nominal data to numeric one
* Suitable algorithms were to be chosen, according to the type of data selected. They have used WEKA ( a collection of ML algorithms)
* 4 classifiers are used to generate the model and results obtained by each classification algorithm is later analyzed and evaluated.
* The faster algorithm with good results is chosen always.

# How To prevent SS7 attacks?

The flaws and vulnerabilities inherent in the SS7 protocol are out of the jurisdiction of enterprises, small businesses as well as consumers. Being that, SS7 vulnerabilities cannot simply be removed or fixed. 

The [GSMA](https://www.gsma.com/) recommends that mobile network operations focus on consumer education. With consumers paying more attention to the security of their smartphones and IoT devices they are more likely to take action to secure their devices. Especially when it comes to critical applications and services like Smart Homes and Offices.

### 1. User Password Security

Two factor SMS authentication, flawed as it is, is still widely used. Security conscious businesses and services are gradually moving away from SMS and offer other methods of authenticating users which do not rely on antiquated telephone protocols like SS7.

### 2. Monitoring & Event Analysis

If an SS7 network is successfully compromised, companies need to have the ability to monitor the activity during the attack. They need to be informed on security events in the context of what is happening on corporate servers as well as devices. This needs to be part of any enterprise mobile security strategy. Ultimately, businesses need to implement a defense that identifies threats and takes action before any damage occurs.

### 3. Regular Updates

Cyber security is not a set it and forget it deal even if you employ automation. Cybercriminals are always coming up with new exploits and approaches to compromise systems to get their hands on confidential data or hijack devices for ransom. Effective Patch Management is critical and complements adaptive defense. By employing real time analysis of endpoint security, business can ensure known vulnerabilities are sealed as soon as possible through software and firmware updates.

# Conclusion

The research of the 2018 report has shown that the level of security of mobile communication networks is still low. Initially, Many Telecom companies thought SS7 attack as a low-level risk, but some unknown hackers have already proved them wrong by exploiting the flaws in it. So, It is always advised to stay safe and secured with your digital data.

There is a feature called “ Google Activity ” in everyone’s google account which tracks and stores all your data history, things searched for, places visited, contacts, and lot more…

If a hacker tries to retrieve your google account by using forget password, he/she would be prompted for a 2FA Verification which would be a 6-digit-code that would be sent as SMS. Hacker would easily intercept your SMS by attacking the SS7 Networ

# References

OpenSS7: <http://www.openss7.org/faq01.html><br>
Firstpoint: <https://www.firstpoint-mg.com/blog/ss7-attack-guide/><br>
Medium@vasanthavanan59439: <https://medium.com/@vasanthavanan59439/ss7-the-deadliest-attack-6423de7fe8c0><br>