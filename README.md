# CogniCare – AI-Based Cognitive Gaming and Memory Assistance Platform

> **AI-Based Cognitive Gaming and Memory Assistance Platform for Elderly Dementia Patients in North Eastern Region (NER)**

CogniCare is a web-based cognitive care and memory assistance platform designed to support elderly dementia patients and their caregivers, with a particular focus on accessibility, personalization, regional relevance, and low-connectivity environments in the North Eastern Region of India.

The project was developed by **Team TechMates**.

---

## Table of Contents

- [Overview](#overview)
- [Problem Statement](#problem-statement)
- [Our Solution](#our-solution)
- [Objectives](#objectives)
- [Key Features](#key-features)
- [How CogniCare Works](#how-cognicare-works)
- [System Architecture](#system-architecture)
- [Technology Stack](#technology-stack)
- [Core Modules](#core-modules)
- [Accessibility and NER Focus](#accessibility-and-ner-focus)
- [Offline and Low-Bandwidth Approach](#offline-and-low-bandwidth-approach)
- [AI and Personalization](#ai-and-personalization)
- [Expected Impact](#expected-impact)
- [Feasibility and Viability](#feasibility-and-viability)
- [Future Scope](#future-scope)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [Database Setup](#database-setup)
- [Running the Project](#running-the-project)
- [Configuration](#configuration)
- [Data and Content](#data-and-content)
- [Research and References](#research-and-references)
- [Limitations](#limitations)

---

## Overview

Dementia can affect memory, attention, reasoning, communication, and the ability to follow everyday routines. In the North Eastern Region, additional challenges can arise from language differences, cultural differences, limited access to specialized care, intermittent connectivity, and low digital literacy among some elderly users.

CogniCare addresses these challenges through a **simple, elderly-friendly website** that combines:

- Cognitive games for memory, attention, reasoning, and mental engagement.
- Memory assistance and smart reminders for medication, appointments, meals, and other daily routines.
- Performance tracking and progress reporting for caregivers.
- AI-assisted personalization based on observed performance trends.
- Multilingual and regional-language support as the platform is expanded.
- Offline/low-bandwidth support for environments with unreliable connectivity.
- A caregiver dashboard for monitoring cognitive activity and providing timely support.

The overall goal is to provide a single integrated platform rather than separating cognitive games, memory support, reminders, and caregiver monitoring into different systems.

---

## Problem Statement

The project targets the following challenges faced by elderly dementia patients in the NER:

1. **Declining cognitive abilities and memory loss** – Patients may experience difficulty remembering information and performing cognitive tasks.
2. **Language and cultural gaps** – General-purpose digital tools may not adequately reflect regional languages, cultural practices, and familiar contexts.
3. **Limited access to specialized care** – Some areas may have fewer specialized dementia-care facilities and support resources.
4. **Technology usability** – Complicated interfaces can be difficult for elderly users, particularly users with cognitive difficulties or low digital literacy.
5. **Connectivity limitations** – Intermittent or low-bandwidth connectivity can reduce the usefulness of cloud-dependent services.
6. **Caregiver coordination** – Caregivers need understandable progress information and routine-related alerts in one place.

---

## Our Solution

CogniCare provides a web platform centered around two roles: **Patient** and **Caregiver**.

### Patient

The patient receives a simple interface for:

- Playing cognitive games.
- Viewing game results where appropriate.
- Receiving memory and routine assistance.
- Following medication, meal, and daily-task reminders.
- Using large, easy-to-understand controls and accessible navigation.

The design also supports the privacy principle that sensitive progress information can remain available to caregivers rather than being unnecessarily exposed to the patient.

### Caregiver

The caregiver can:

- Register and log in securely.
- Add and manage patients.
- Set routines and reminders.
- Monitor patient activity and progress.
- Review performance trends and reports.


---

## Objectives

The main objectives of CogniCare are to:

- Encourage regular cognitive stimulation through engaging activities.
- Support memory and everyday routine management.
- Personalize cognitive activities using performance trends.
- Give caregivers a centralized monitoring interface.
- Improve accessibility for elderly users with cognitive difficulties.
- Support regional language and culturally relevant content.
- Function in environments where connectivity may be intermittent.

---

## Key Features

### 1. Cognitive Games

The prototype demonstrates multiple game types intended to exercise different cognitive skills, including memory, attention, pattern recognition, matching, sequencing, word skills, and basic reasoning.

Examples shown in the prototype include:

- Memory Cards
- Image Matching
- Number Puzzle
- Sequence Recall
- Word Search
- Sorting Game
- Math Quiz
- Attention Tap
- Color Match
- Matching/Pattern activities
- Other expandable cognitive game formats

The platform is designed so that additional games can be added as the project grows.

### 2. Adaptive Difficulty and Personalization

CogniCare is designed to observe performance trends such as accuracy, scores, timing, and session results. These trends can be used to adjust future activities and game difficulty toward the individual user's observed performance.

### 3. Game Results and Level Progression

After a cognitive activity, the platform can present performance information such as score, accuracy, and completion time. The prototype also demonstrates a **Level Up** flow, allowing the patient to progress to a higher difficulty level after completing an activity successfully.

### 4. Memory Assistance

The platform includes routine-support concepts for:

- Medication schedules
- Meals
- Daily tasks
- Other recurring routines

### 5. Smart Reminders and Alerts

Caregivers can configure routines, while the system can provide reminders and alerts related to missed routines or notable changes in activity/performance.

### 6. Caregiver Dashboard

The caregiver dashboard brings relevant patient information together in one place, including:

- Patient list
- Performance indicators
- Progress reports
- Trend information
- Patient-management tools

### 7. Patient Progress Privacy

The prototype includes a protected patient-progress view so that detailed cognitive progress is intended to be accessible through the caregiver side rather than being unnecessarily exposed to the patient.

### 8. Multilingual and Regional Adaptation

The concept supports regional-language content with human review and is intended to adapt to regional languages, cultural practices, and daily routines relevant to the NER.

### 9. Accessibility-Oriented Interface

The platform aims to use:

- Large controls
- Simple navigation
- Clear visual hierarchy
- Reduced interface complexity

### 10. Offline / Low-Bandwidth Support

The architecture includes an offline-first direction using local storage/service-worker concepts and background synchronization so that essential interactions can continue during intermittent connectivity.

---

## How CogniCare Works

The proposed user flow is:

```text
                CogniCare
                    |
             Select Your Role
              /            \
          Patient         Caregiver
             |                |
       Patient Home      Register / Login
        /    |    \              |
           Games           Add Patient
       |      |                 |
    Results Alerts             Set Routine
       \      /                  |
        AI / Analytics <---------+
              |
        Daily Progress
              |
       Caregiver Monitor
```

### Typical patient workflow

1. Open the CogniCare website.
2. Select the **Patient** role.
3. Enter the patient area.
4. Start a cognitive game or review routine assistance.
5. Complete the activity.
6. Store/review the session result as defined by the system.
7. Feed performance information into the analysis/personalization layer.

### Typical caregiver workflow

1. Open CogniCare.
2. Select the **Caregiver** role.
3. Register or log in.
4. Configure routines and reminders.
5. Review game activity and performance trends.
6. Monitor daily progress and respond to relevant alerts.

---

## System Architecture

The architecture presented in the project proposal is divided into three major layers.

### 1. View Layer – Client

The client layer is accessed through a web browser by elderly patients and caregivers.

Responsibilities include:

- User interface rendering.
- Patient/caregiver interaction.
- Accessible navigation.
- Game interfaces.
- Dashboard presentation.
- Asynchronous requests where applicable.

### 2. Controller Layer – Server

The controller layer is hosted through the servlet container and manages HTTP requests and application flow.

The proposal identifies controllers such as:

- `PatientProfileServlet`
- `GameSessionServlet`
- `MemoryAssistanceServlet`
- `AIAnalyticsController`

Responsibilities include:

- Request routing.
- Input validation.
- Session handling.
- Application orchestration.
- Calling data/model components.
- Returning HTML/JSON responses where required.

### 3. Model Layer – Data and Logic

The model/data layer contains application objects and data-access components.

The proposal shows example model objects such as:

- `Patient.java`
- `GameScore.java`
- `MemoryLog.java`

Example data-access objects include:

- `PatientDAO.java`
- `GameDAO.java`
- `AIRepo.java`

The database layer uses **MySQL**, with **JDBC** providing Java-to-database connectivity.

### High-level data flow

```text
Browser / Client
      |
      | HTTP GET / POST
      v
Java Servlet Controller Layer
      |
      | CRUD / business logic
      v
Model + DAO Layer
      |
      | JDBC
      v
MySQL Database
      |
      v
Analytics / AI Layer
      |
      v
Personalized results + caregiver insights
```

---

## Technology Stack

The project proposal identifies the following technologies:

| Layer / Purpose | Technology |
|---|---|
| Frontend | HTML5, CSS3, JavaScript |
| Server-side web | Java Servlets, JSP |
| Servlet container | Apache Tomcat 10.1 |
| Database | MySQL |
| Java database connectivity | JDBC |
| AI/API integration | Python API |
| AI/ML integration direction | TensorFlow Lite / PyTorch APIs |
| Offline support | Service Worker, local storage / storage layer |
| Development environment | Java web application setup / Eclipse-compatible workflow |

The proposal also describes an offline system using Java adaptive logic, a service worker, and local storage.

> **Note:** The exact dependency versions and environment variables should be documented in the repository according to the current source code. This README does not invent version numbers that are not specified in the project material.

---

## Core Modules

### Authentication and Role Management

Provides role selection and authentication flows for patients and caregivers.

### Patient Management

Allows caregivers to add and manage patient profiles and associated information.

### Cognitive Game Engine

Hosts game sessions, records performance information, and supports multiple cognitive activity types.

### Results and Progress Tracking

Stores and displays relevant game and activity performance for monitoring and analysis.

### Memory Assistance

Supports reminders and structured daily routines.

### AI / Analytics

Uses performance trends as an input to personalization and insight generation.

### Caregiver Monitoring

Presents patient activity, progress, routines, alerts, and trend information through the caregiver dashboard.

### Localization and Accessibility

Supports an interface direction suitable for elderly users and future regional-language adaptation.

---

## Accessibility and NER Focus

CogniCare is intentionally designed around the context of elderly users in the North Eastern Region rather than assuming a single, uniform user population.

The project proposes:

- **Simple interfaces** to reduce technology barriers.
- **Large controls and voice guidance** for users with low digital literacy.
- **Regional-language support** to reduce language barriers.
- **Cultural adaptation** for familiar content, routines, and contexts.
- **Offline-first support** for intermittent connectivity.
- **Centralized caregiver monitoring** to reduce the need for constant direct supervision.

This NER focus is one of the central aspects of the project rather than simply a geographic deployment detail.

---

## Offline and Low-Bandwidth Approach

Connectivity can be inconsistent in some areas. The proposal addresses this with an **offline-first + background synchronization** approach.

The intended flow is:

```text
Online
  |
  +--> Fetch / Sync data
  |
Offline
  |
  +--> Continue supported local interactions
  |
  +--> Store pending data locally
  |
Connection restored
  |
  +--> Background synchronization
```

This approach is intended to reduce dependence on continuous internet connectivity while keeping important information synchronized when a connection becomes available.

---

## AI and Personalization

The project proposes AI-assisted personalization based on observed performance trends.

Possible signals include:

- Game accuracy.
- Score trends.
- Completion time.
- Session history.
- Activity patterns.

These signals can support decisions such as selecting suitable game difficulty and identifying changes in cognitive performance over time.

The proposal describes an overall pipeline of:

```text
Onboarding
    ↓
Baseline
    ↓
AI Profile
    ↓
Game / Recall
    ↓
Analysis
    ↓
Insight
```

The project documentation also identifies on-device inference and secure synchronization as technical directions for AI integration.

---

## Expected Impact

### Elderly Dementia Patients

- Increased cognitive engagement.
- Regular memory, attention, and reasoning activities.
- Personalized activities based on performance trends.
- Support for structured daily routines.

### Patients and Families

- Better support for medication, appointments, and daily routines through reminders.
- Greater involvement of family members in ongoing care.

### Caregivers

- Centralized monitoring of cognitive activity and routines.
- Easier review of progress and performance trends.
- Alerts for missed routines or notable changes.
- Reduced supervision burden through structured digital support.

### Healthcare Providers

- Useful performance trends and reports that can support follow-up and informed intervention.

### NER Communities

- Greater accessibility to dementia-support resources, particularly where specialized services may be limited.
- Potential for regional-language and culturally adapted support.

### Broader Social Impact

- Greater awareness of dementia and cognitive care.
- Encouragement of regular cognitive activities.
- Better family participation.
- Support for healthy ageing and social inclusion.

---

## Feasibility and Viability

The proposal evaluates the idea across three dimensions.

### Desirability

CogniCare addresses the needs of elderly dementia patients and caregivers, aims to improve engagement and well-being, and is designed to be user-friendly and culturally relevant to the NER.

### Feasibility

The proposal uses mature web, AI/ML, and database technologies. The system is designed to support lightweight models, offline operation, scalability, and regional-language adaptation.

### Viability

The project is intended as a low-cost web-based solution that can support clinics, NGOs, and elder-care centers, with a focus on long-term impact and sustainability in the NER.

---

## Risk and Mitigation

| Risk | Proposed Mitigation |
|---|---|
| Low digital literacy | Large controls + voice guidance |
| Limited connectivity | Offline-first + background sync |
| Privacy / sensitive data | Consent + encryption + minimal data |
| Language and cultural differences | Regional-language support + human review |
| Elderly usability challenges | Simple navigation and accessible interface |

---

## Future Scope

The project can be expanded with:

- More cognitive games.
- Advanced AI / ML personalization.
- Clinician-facing summaries.
- Hospital or healthcare-system integration.
- Wearable-device context.
- A dedicated mobile application.
- Larger NER deployment with additional languages.
- More advanced analytics and longitudinal reporting.
- Stronger offline capabilities and synchronization.

These extensions are intended to increase coverage and usefulness without changing the central goal of cognitive care and memory assistance.

---

## Project Structure

A suggested GitHub structure for a Java web implementation is:

```text
CogniCare/
├── src/
│   └── ... Java Servlets, DAOs, models and backend code
├── WebContent/ or src/main/webapp/
│   ├── css/
│   ├── js/
│   ├── images/
│   ├── jsp/
│   └── WEB-INF/
├── python-api/
│   └── ... AI / analytics API code
├── database/
│   ├── schema.sql
│   └── sample_data.sql
├── docs/
│   ├── architecture.md
│   ├── screenshots/
│   └── presentation/
├── README.md
└── LICENSE
```

Adjust the folders to match the actual project files. The structure above is a documentation template, not a claim about the exact current repository layout.

---

## Installation and Setup

### Prerequisites

Install the software required by the current project implementation, including:

- Java Development Kit compatible with the application's servlet/JSP configuration.
- Apache Tomcat compatible with the project (the proposal shows Tomcat 10.1).
- MySQL Server.
- MySQL JDBC Driver.
- Python and the dependencies used by the AI API, if the AI API is enabled.
- An IDE such as Eclipse for development, deployment, and debugging.

### Clone the repository

```bash
git clone https://github.com/<your-username>/CogniCare.git
cd CogniCare
```

Replace `<your-username>/CogniCare` with the actual GitHub repository path.

---

## Database Setup

1. Start the MySQL server.
2. Create the required database.
3. Import the SQL schema from the repository's `database/` folder.
4. Add sample data only when required for development/testing.
5. Configure the database connection used by the Java/JDBC layer.

Example MySQL setup:

```sql
CREATE DATABASE cognicare;
```

Then import your actual schema file, for example:

```bash
mysql -u <username> -p cognicare < database/schema.sql
```

> The exact database name, tables, columns, and credentials should match the SQL files in the repository.

---

## Running the Project

A typical Java web deployment flow is:

1. Configure the MySQL database and JDBC credentials.
2. Configure the Java web project in Eclipse.
3. Configure Apache Tomcat.
4. Add the MySQL JDBC driver to the application.
5. Deploy the project to the Tomcat server.
6. Start Tomcat.
7. Open the application in a browser using the configured local URL and port.
8. Start the Python AI API separately if the project requires it.

Example local URL format:

```text
http://localhost:<tomcat-port>/CogniCare/
```

Replace `<tomcat-port>` and the context path with the values used by your local Tomcat configuration.

---

## Configuration

Do not commit real credentials or sensitive information to GitHub.

Use environment variables or a local configuration file for values such as:

```text
DB_HOST=
DB_PORT=
DB_NAME=
DB_USER=
DB_PASSWORD=
AI_API_URL=
```

A safe repository should include an example configuration file such as `.env.example` or `application-example.properties` instead of real credentials.

---

## Data and Content

The project proposal identifies these content/data sources:

- Public-domain cognitive task concepts.
- Consent-based caregiver photos, names, and places.
- Regional-language content with human review.

For a real deployment, data collection should follow appropriate consent, privacy, retention, and security requirements.

---

## Research and References

The project proposal cites the following supporting resources:

- **Alzheimer's Association** – *Alzheimer's Disease Facts and Figures*.
- **World Health Organization (WHO)** – *Global status report on dementia*.
- Literature on cognitive training, reminiscence, and digital interventions.
- **PubMed** – *Computerized Cognitive Training*, cited in the proposal as directly relevant to cognitive games and digital training: https://pubmed.ncbi.nlm.nih.gov/38172429/
- **W3C Cognitive Accessibility** – guidance relevant to interfaces for people with cognitive difficulties: https://www.w3.org/WAI/cognitive/

### Implementation research directions from the proposal

- AI personalization using performance trends.
- Offline-first architecture for intermittent connectivity.
- Privacy-by-design using consent, encryption, and minimal collection.
- W3C cognitive accessibility guidance.
- On-device inference and secure synchronization.

---

## Limitations

CogniCare is a supportive cognitive-care platform and should not be presented as a diagnostic system or as a replacement for professional medical care.

The proposal also represents some features as implementation directions or future scope. Production use would require additional validation, security testing, usability testing with the target population, clinical/ethical review where applicable, robust multilingual review, and reliable deployment infrastructure.

---

## Acknowledgement

CogniCare was prepared for **Smart India Hackathon 2026**, addressing **SIH26003 – AI-Based Cognitive Gaming and Memory Assistance Platform for Elderly Dementia Patients in North Eastern Region (NER)**.

The project's proposal emphasizes cognitive stimulation, personalized activities, memory assistance, caregiver monitoring, regional accessibility, offline/low-bandwidth support, and privacy-aware handling of sensitive information.
