# Instituto Apontar — Public Report (Module 2)

# Project Overview

This document summarizes the work developed throughout Module 2 for the Instituto Apontar project. The platform was designed to deliver adaptive digital learning paths aligned with the BNCC (Brazilian National Common Core Curriculum) and targeted especially at gifted students in the public education system. The project was structured in five sprints.

Initially, the project was scoped for Instituto Ponte, but due to data privacy restrictions, it was restructured to meet the needs of Instituto Apontar. The new scope, stakeholders, timeline, and feature set were successfully redefined at the beginning of Sprint 2.

## Sprint 1 — Initial Concept (Instituto Ponte)

* Contextual research and data exploration based on ENEM microdata.

* Initial data visualization in Google Sheets.

* Objective: Identify educational gaps in vulnerable students.

* Key tools: BigQuery, SQL, Google Sheets, ENEM Microdata.


## Sprint 2 — Redefining Scope and Planning for Instituto Apontar

* Project pivot to Instituto Apontar.

* New target audience: public school students with high abilities/giftedness (AH/SD).

* Co-creation of the project’s backlog with stakeholders.

* Functional and non-functional requirements defined.

* Tech stack chosen: React (frontend), NestJS (backend), PostgreSQL (database).

* Sprint planning and risk management framework created.

* BNCC-aligned diagnostic assessments and adaptive paths defined.

## Sprint 3 — User Interface Design (Student Side)

- Mascot & Branding

    * Young Falcon chosen as mascot: represents sharp vision, growth, and potential.

    * Mascot designed with expressive variations to enhance emotional engagement.

- Student Experience Screens

    * Login Screen with Google SSO and mascot for engagement.

    * Home Screen:

        * Diagnostic test initiation.

        * Personalized progress by subject.

        * Motivational quote + mascot.

-  Simulation Flow:

    * Subject selection (Math/Portuguese).

    * Time-limited questions with teaching-style mascot.

    * Visual feedback for answers (correct/incorrect).

- Results Screen:

    *  Tracks simulation history and results.

- Practice by Topic:

    * Modular structure by BNCC skills.

    * Subject toggle (Math/Portuguese).


## Sprint 4 — Supervisor Interface

Development of an exclusive interface for supervisors and teachers.

- Supervisor Functionalities

* Student list with school year and BNCC-based level.

* Simulation dashboard:

    * View/edit simulations.

    * Track status (draft/open/completed).

* Question creation:

    * Fill in enunciado, discipline, BNCC skill, and correct answer.

    * View number of questions created per subject.

* Question Bank:

    * Manage reusable questions.

    * View BNCC skills mapped per grade.

BNCC Skills Reference: https://docs.google.com/document/d/1qnaQrdR4dNyB9A0KbcHqlIWySUIEXAGuQu3eIoKXh6E/edit

## Sprint 5 — Final Revisions Based on Partner Feedback

- Stakeholder Meeting

    * On June 26th, 2025, a final review meeting was held with stakeholder Rômulo Nunes.

    * Feedback received led to refinements in both student and supervisor experiences.

- Student Side Updates

    * "Fazer Simulado" renamed to "Fazer Estudo" to reduce pressure.

    * New button: "Fale com a coordenação" opens WhatsApp chat with school staff.

    * Progress tracking split into Math and Portuguese.

- Supervisor Side Updates

    * New Home screen for supervisors:

        * Charts per class for Math and Portuguese.

        * Bimonthly tracking of average level vs. official grade.

        * Gap analysis by subject.

    * Updated student table:

        * Shows subject-separated proficiency.

        * Enables more accurate pedagogical planning.

- Individual Student Modal

    * Clicking a student opens a modal with:

        * Bar charts showing level evolution over time (per subject).

        * Identified learning gaps.

- New Feature: Image Upload in Alternatives

    * Teachers can now attach images to each multiple-choice alternative.

    * Enables visual learning assessments:

        * "Which graph shows a quadratic function?"

        * "Select the figure with 8 equal sides."

        * "Identify the histogram with correct data."


## Conclusion

Over the course of 5 sprints, the platform evolved from a concept to a well-structured adaptive learning system. It provides:

- Engaging experiences for students through gamified design and emotional elements.

- Robust tools for supervisors to track, evaluate, and support student growth.

- BNCC-aligned simulations and practice exercises.

The integration of stakeholder feedback throughout the project ensured that the solution meets real classroom needs. The project is now ready for the development phase.

    "Like a young falcon taking flight, every student at Instituto Apontar is supported to reach higher and farther than ever before."

