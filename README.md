# EchoPulse

## Overview
From the Adelaide University website:
> Receiving instruction and guidance from experienced mentors, underpinned by theory, students develop prototypes that address a market need and then present these to a panel of judges where they receive feedback about their innovations.
	- [*Course description*](https://adelaideuni.edu.au/study/courses/busi-3901/)

My team's project was **EchoPulse**, an on-device conversational AI designed to guide untrained users through critical first-aid procedures when emergency services cannot be reached.

It is intended to **simulate the role of an emergency services operator** in remote environments, providing step-by-step voice guidance for medical emergencies such as CPR, snake bites, and heat stroke.

This repository contains some of the submission files for the project, including marketing materials and presentation documents. A recording of the initial pitch is hosted [here](https://www.dropbox.com/scl/fi/bqxowo352b2bi7ghwqw51/echopulse_initial_pitch.mp4?rlkey=4t6t9b164rjh9b6zeh6hpewo7&st=z9kpcu5v&dl=0), and the final pitch presentation (with prototype demonstration video) is hosted [here](https://www.canva.com/design/DAGn8mNsfZQ/yjrBhuGzVF8UMbwuiT61fg/edit).

## Team
- **Tobias Grice** — Design & Development Lead  
    Product and system design, graphic design, mock-up and prototype development
- **Bladen Chen** — Secretary  
    Market research, analytics, business modelling
- **Hargun Bains** — Project Manager  
    Finance, accounting, digital strategy
- **Valerie Wong** — Team Lead  
    Branding, marketing, strategic planning

---
## About the Project
### Motivation
Australia’s geography creates a dangerous gap between emergencies and professional help:
- Less than 5% of Australians have formal first aid training.
- In the twelve months leading up to April of 2025, there were 1,296 deaths on Australian roads, over three quarters of which were in remote areas. That’s 986 human lives lost.
- Around two thirds of Australia’s land mass does not have cell reception.

### System Design
**UX Overview**
- Users interface with an LLM entirely verbally through a mobile phone app.
- EchoPulse will ask questions to diagnose the issue then walk the user through providing first aid they may not be trained in, such as CPR.
- It will be able to field questions from the user and provide justification for its suggestions.
**Architecture Overview**
- The LLM uses on-device models provided by modern smartphones.
- All decision-making and advice will be outsourced to a rule based AI called EchoCore.
- The LLM will interface with EchoCore and relay guidance to the user as spoken word. 
- This dramatically reduces odds of hallucination and allows the app to operate with less computational strain and storage costs.

> **Medical reasoning is _never_ delegated to a probabilistic model.**

### User Experience
1. User presses **Emergency** button on home screen.
2. EchoPulse begins voice interaction with *“Tell me what you see.”*
3. The app walks the user through diagnosis and first aid.
4. Continuous verbal feedback keeps the user calm and focused.

Wireframes and scripted flows are included in the project materials (see final presentation).

### Validation & Evidence
We conducted market research by interviewing lawyers, nurses, doctors, and potential users:
- Strong preference for voice guidance over text.
- Users feel calmer when guided step-by-step.
- Clear requirement for medical professional validation before deployment.
- Early intervention was repeatedly confirmed as critical (e.g. stroke and cardiac events).

### Target Users
EchoPulse is designed for:
- People who live or work in remote areas
- Remote tourists (hikers, climbers, researchers)
- Carers and family members of at-risk individuals

### Legal & Ethical Considerations
We interviewed several legal professionals about the legal and ethical considerations of this project. We determined the following actions would be required:
- Ongoing legal consultation with medical and technology specialists
- Clear disclaimers and terms of use
- Explicit instruction to **contact emergency services first whenever possible**
- No claims of replacing professional medical care

This is the largest consideration in making this concept a reality. A single bug could cause someone's death - the ethical ramifications in deploying this product are immense.

### Funding & Model
- Initial funding via Kickstarter
- Future partnerships with:
    - St John Ambulance
    - EPIRB and emergency hardware manufacturers
- **Non-profit revenue model**
    - All proceeds reinvested into feature expansion and validation
