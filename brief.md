Version: NAFATH-V3
Track: Software

## Overview
A trustworthy public-service AI assistant depends on six connected technical fields. Software engineering provides stable APIs and ensures updates do not break existing services. Artificial intelligence uses Retrieval-Augmented Generation (RAG) to retrieve approved government information and produce reliable answers. Mobile development protects communication between applications and servers through secure connections. Networking supports reliable connectivity and prepares infrastructure for more connected devices through IPv4 and IPv6. Cybersecurity reduces threats such as prompt injection and restricts access to sensitive operations. Data governance protects citizens’ information by distinguishing anonymous data from pseudonymized personal data and applying privacy controls. These fields work together: AI needs accurate data, mobile applications need secure networks, and software updates must preserve compatibility while addressing security risks. Combining these practices helps the assistant provide dependable, secure, and accessible government services. For Software, an important decision is whether an API change requires a MAJOR, MINOR, or PATCH version update release.

## Software
Under Semantic Versioning, a MAJOR version increases when changes break backward compatibility, such as removing an API endpoint. MINOR increases when new features are added without affecting existing functionality, such as adding an optional field. PATCH increases for backward-compatible bug fixes. After a MAJOR increase, MINOR and PATCH reset to zero. After a MINOR increase, PATCH resets to zero. Following these rules helps maintain API compatibility and ensures mobile applications continue working correctly after updates.

Resource: Semantic Versioning 2.0.0 - https://semver.org/spec/v2.0.0.html

## AI
Retrieval-Augmented Generation (RAG) combines information retrieval with AI text generation. It retrieves relevant information from trusted sources, such as official government documents, and provides it to the AI model to support accurate answers. This reduces incorrect or unsupported responses by grounding answers in evidence. However, RAG does not guarantee accuracy, because retrieved information may be outdated or incomplete.

Resource: Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks - https://arxiv.org/abs/2005.11401

## Mobile
iOS App Transport Security (ATS) enforces secure connections between applications and servers using HTTPS, appropriate TLS settings, and valid certificates. By default, ATS blocks requests to plain HTTP endpoints because they lack required security. For example, a government application requesting citizen information over HTTP may fail to retrieve data. Developers should configure servers to support HTTPS and maintain ATS protections. This helps protect sensitive information from interception, unauthorized access, and security threats during transmission between mobile applications and servers.

Resource:  Apple. (n.d.). Preventing Insecure Network Connections. Apple Developer Documentation. https://developer.apple.com/documentation/security/preventing-insecure-network-connections

## Networking
IPv4 uses 32-bit addresses, providing approximately 4.3 billion unique addresses, while IPv6 uses 128-bit addresses, offering a vastly larger address space. As connected devices increase, IPv6 allows more devices to obtain unique addresses and reduces address shortages. In the government assistant project, IPv6 supports scalability by enabling more smartphones, servers, and connected systems to communicate efficiently, helping maintain reliable connectivity as demand for digital government services grows.

Resource:  Internet Engineering Task Force. (2017). *Internet Protocol, Version 6 (IPv6) Specification (RFC 8200).* RFC Editor. https://www.rfc-editor.org/rfc/rfc8200

## Cybersecurity
Prompt injection is an attack that manipulates an AI system into ignoring its instructions or performing unintended actions. Direct prompt injection occurs when a user enters malicious instructions directly. Indirect prompt injection occurs when harmful instructions are hidden in external content, such as websites or documents. Two ways to reduce risk are separating trusted instructions from untrusted input and validating AI outputs before taking actions. These measures help protect the government assistant from misuse and unauthorized access.

Resource: OWASP Foundation. (n.d.). *LLM01: Prompt Injection*. OWASP Gen AI Security Project. https://genai.owasp.org/llmrisk2023-24/llm01-24-prompt-injection/

## Data
Anonymization permanently removes identifying information from chat logs so individuals cannot be identified, even indirectly. Pseudonymization replaces personal identifiers with artificial labels, while the original identities can still be recovered using additional information. For the government assistant, anonymization helps protect citizens’ privacy when analyzing conversations. Under the GDPR, properly anonymized data falls outside data protection law, whereas pseudonymized data remains personal data and must still be protected.

Resource:  European Parliament and Council of the European Union. (2016). *Regulation (EU) 2016/679 (General Data Protection Regulation), Recitals 26 and Article 4(5).* Official Journal of the European Union. https://eur-lex.europa.eu/eli/reg/2016/679/oj

## Misconception in My Track
A common misconception in Software Engineering is that adding new features to an API always requires a MAJOR version increase. The correct version is that backward-compatible additions, such as optional fields, usually require a MINOR version increase under Semantic Versioning. A MAJOR version increase is necessary when changes break backward compatibility, such as removing an existing endpoint. PATCH increases are used for backward-compatible bug fixes. This distinction helps developers update government assistant services without disrupting existing mobile applications. The supporting resource section is “Semantic Versioning 2.0.0,” specifically the headings “Summary” and “MAJOR, MINOR, and PATCH.”

Resource:  Preston-Werner, T. (n.d.). *Semantic Versioning 2.0.0*. https://semver.org/

## Open Question
I would investigate how to test a government AI assistant against direct and indirect prompt injection attacks. I would learn which security tools can detect malicious instructions in user messages and external documents, and how to evaluate whether these protections effectively prevent unauthorized access to sensitive citizen information.

