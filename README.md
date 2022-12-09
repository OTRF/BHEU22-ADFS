# Black Hat Europe 2022

Writing Your Own Ticket to the Cloud Like APT: A Deep-dive to AD FS Attacks, Detections, and Mitigations

<p align="center">
  <a href="#abstract">Abstract</a> •
  <a href="#speakers">Speakers</a> •
  <a href="Slide-Deck.pdf">Slides</a>
</p>

## Abstract

Azure Active Directory (Azure AD) is Microsoft's cloud-based identity and access management solution used by Microsoft 365, Azure, and thousands of third-party service providers. Almost all Fortune 500 companies have adopted Azure AD, mainly by consuming Microsoft 365 services like Exchange, Teams, and SharePoint. Of these companies, the majority have chosen identity federation as their authentication method.

Microsoft Active Directory Federation Services (AD FS) is a technology often used to implement the identity federation for Azure AD. As with any other identity federation solution supported by Azure AD, it is based on industry standards, such as cryptographically signed Security Assertion Markup Language (SAML) tokens. To prevent attackers from altering or counterfeiting security tokens and gaining unauthorized access to federated resources, federation servers use a token-signing certificate. By default, this token-signing certificate is stored in the AD FS configuration database and encrypted using Distributed Key Manager (DKM) APIs.

In the last couple of years, we have witnessed state-sponsored threat actors like NOBELIUM compromising AD FS token-signing certificates by accessing the AD FS configuration database and the DKM master key. Compromising token-signing the certificates allows them to impersonate any user in a federated environment using a technique known as the Golden SAML. Due to the high adoption rate, the AD FS remains a lucrative target for the years to come.

This talk will introduce in detail all known attack vectors to access the configuration database, extract the DKM master key and decrypt the token-signing certificate. As the capability to detect such attacks is crucial to any response activities, we will also cover how to detect these attacks. Finally, we will share best practices for protecting against these attacks.

## Speakers

* [Nestori Syynimaa](https://www.blackhat.com/eu-22/briefings/schedule/speakers.html#nestori-syynimaa-37068)  |  Senior Principal Security Researcher, Secureworks
* [Roberto Rodriguez](https://www.blackhat.com/eu-22/briefings/schedule/speakers.html#roberto-rodriguez-37952)  |  Principal Threat Researcher, Microsoft