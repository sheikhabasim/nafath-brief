Version: NAFATH-V4
Track: Cybersecurity

## Overview

A national service provider relies on an interconnected digital software supply chain where threats across software, AI, mobile apps, networking, cybersecurity, and data management directly impact service integrity and operational resilience. Storing credentials directly in application source code creates immediate exposure vulnerabilities, while machine learning systems face adversarial risks such as data poisoning and evasion attacks that alter model behavior. Mobile applications require rigorous verification against OWASP MASVS guidelines to prevent unauthorized local security breaches. At the infrastructure layer, internet routing remains vulnerable to BGP hijacking, which requires RPKI cryptographic validation to protect traffic pathways. Furthermore, widespread critical vulnerabilities like Log4Shell demonstrate how third-party library flaws propagate rapidly through software ecosystems. Establishing a comprehensive Software Bill of Materials (SBOM) provides complete transparency over software components, ensuring robust enterprise defense and resilience across the entire technical ecosystem.
## Software

According to the Twelve-Factor App methodology, configuration and secrets should be stored in environment variables rather than hardcoded within the application code. Keeping secrets out of the codebase prevents accidental exposure in public repositories, enhances security posture, and allows seamless configuration changes across different deployment environments without requiring code recompilation.

Resource: The Twelve-Factor App - Factor III: Config - https://12factor.net/config

## AI

Adversarial attacks on machine learning systems primarily include evasion attacks, data poisoning, model extraction, and membership inference. Evasion attacks manipulate inputs at inference time to cause misclassification, whereas data poisoning corrupts training datasets to inject backdoors or degrade overall model accuracy.

Resource: NIST AI 100-1: Adversarial Machine Learning Taxonomy - https://nvlpubs.nist.gov/nistpubs/ai/NIST.AI.100-1.pdf
## Mobile

The OWASP Mobile Application Security Verification Standard (MASVS) is a comprehensive security standard for mobile app development and testing. It is used to verify the security of a mobile app by establishing baseline security requirements across reverse engineering resistance, authentication mechanisms, and secure data storage.

Resource: OWASP Mobile Application Security Verification Standard - https://github.com/OWASP/owasp-mastg
## Networking

BGP route hijacking redirects internet traffic by maliciously or accidentally announcing unauthorized IP route prefixes, diverting data flows through illegitimate autonomous systems. RPKI (Resource Public Key Infrastructure) prevents this by using cryptographic certificates to validate legitimate IP address ownership, though it does not protect against path interception or internal router compromise.

Resource: RFC 6480 - An Infrastructure to Support Secure Internet Routing - https://www.rfc-editor.org/rfc/rfc6480

## Cybersecurity

The Log4Shell vulnerability (CVE-2021-44228) is a critical remote code execution flaw in the Apache Log4j logging library. It was rated with the maximum severity score of 10.0 because Log4j is ubiquitous in enterprise Java applications, and the vulnerability could be triggered easily via untrusted string inputs, allowing attackers to take full control of affected servers. It was fixed by releasing patches that disable JNDI lookups by default and upgrading to sanitized versions of the library.

Resource: National Vulnerability Database - CVE-2021-44228 - https://nvd.nist.gov/vuln/detail/CVE-2021-44228
## Data

A Software Bill of Materials (SBOM) is a formal, structured inventory of software components and dependencies used to build an application, functioning like an ingredient list for software. At a minimum, an SBOM should contain data fields such as supplier name, component name, version string, component unique identifier, dependency relationship, and the author of the SBOM data.

Resource: NTIA - Minimum Elements for a Software Bill of Materials - https://www.ntia.doc.gov/files/ntia/publications/sbom_minimum_elements_report.pdf

## Misconception in My Track

## Open Question
