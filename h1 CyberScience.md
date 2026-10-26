# H1 CyberScience

**Article**
Hoseini, S. V., Suutala, J., Partala, J. & Halunen, K. 2024. Threat Modeling AI/ML With the Attack Tree. IEEE Access. Vol. 12, pp. 172610-172637. DOI: 10.1109/ACCESS.2024.3497011

- Name: Threat Modeling AI/ML With the Attack Tree
- Authors: Seied Veria Hoseini, Jaakko Suutala, Juha Partala, Kimmo Halunen
- Published: 13 November 2024
- Publisher: IEEE access
- JUFO rating: 1

  
**Review the review**

*What are the key areas being researched?:*
- Threat modeling for AI/ML systems using attack trees
- Adversarial attacks such as evasion attacks, poisoning attacks, backdoor attacks, and model stealing
- Privacy attacks and data reconstruction
- Security of ML components across the whole lifecycle (data collection, training, deployment, monitoring)
- Risk assessment methods for estimating attack likelihood and impact
- Defenses against attacks on confidentiality, integrity, availability, and privacy


*What's widely agreed upon?:*
- AI/ML systems have many security vulnerabilities and are attractive targets for attackers
- Threat modeling is important and should be done early in system design
- Attacks can happen during both training and inference phases
- Data and models are valuable assets that need protection
- Traditional cybersecurity measures alone are not enough for AI/ML systems
- Confidentiality, integrity, availability, and privacy are the main security goals in AI/ML systems

*What are the open questions?:*
- How to build a complete defense tree that matches attack trees
- How to protect ML models from adversarial attacks using cryptography
- What new risks Quantum Machine Learning (QML) introduces
- How homomorphic encryption can be made practical for secure ML
- How to detect poisoned data and hidden backdoors more reliably
- How watermarking can prevent model stealing and protect intellectual property
- How Zero-Knowledge Machine Learning (ZKML) can improve privacy without revealing training data
- How to make ML models better against adversarial examples and new attack techniques

**Threat modelling quickrun**

*Crown jewels*
- Model weights and training data (IP worth billions)
- Availability of Claude services (business continuity)
- Customer data and prompts
- Brand reputation and trust
- Revenue from enterprise subscriptions

*Bad Guys1*
- **Government grade actor / advanced competitor**
- Capability: High
- Opportunity: Public APIs, employees, supply chain
- Intent: Steal model capabilities and IP
- Why Anthropic: Frontier AI models have enormous strategic value

*Bad Guys2*
- **Cybercriminal group**
- Capability: Medium-High
- Opportunity: Public-facing services and cloud infrastructure
- Intent: Extortion, ransom, reputation damage
- Why Anthropic: High-profile target with low tolerance for outages


*Risk1*
- Model extraction via API abuse and query attacks, resulting in theft of model behavior/IP
- Likelihood 10%
- Impact 750M€
- Estimated risk 75M€

*Risk2*
- DoS/DDoS causing online service outage
- Likelihood 30%
- Impact 30M€
- Estimated risk 9M€

*Biggest risk*
Model extraction via API abuse and query attacks, resulting in theft of model behavior/IP
Estimated risk value 75M€









