<!--
Sync Impact Report:
- Version change: None → 1.0.0
- List of modified principles:
  - `[PRINCIPLE_1_NAME]` → `I. Absolute Anonymity`
  - `[PRINCIPLE_2_NAME]` → `II. Simplicity and Speed`
  - `[PRINCIPLE_3_NAME]` → `III. User Safety and Control`
  - `[PRINCIPLE_4_NAME]` → `IV. Mobile-First and Responsive Design`
  - `[PRINCIPLE_5_NAME]` → `V. Unrestricted Content Access`
- Added sections: `Non-Functional Requirements`, `Content Policy`
- Removed sections: None
- Templates requiring updates:
  - `.specify/templates/plan-template.md` (✅ aligned)
  - `.specify/templates/spec-template.md` (✅ aligned)
  - `.specify/templates/tasks-template.md` (✅ aligned)
- Follow-up TODOs: None
-->
# Anonymous Advice Board Constitution

## Core Principles

### I. Absolute Anonymity
The service MUST operate without any user login or account creation. User identification is temporary and browser-based (using Cookies or LocalStorage). No personally identifiable information (PII) such as names, emails, or phone numbers SHALL be stored. The server MUST NOT log IP addresses in a way that can be linked to user activity.

### II. Simplicity and Speed
The user experience MUST be straightforward, focusing on core features (posting, reading, commenting). The application MUST be a Single Page Application (SPA) with an initial load time under 5 seconds and API responses under 1 second. Unnecessary animations and complex features like nested comments are forbidden to maintain a lean and fast interface.

### III. User Safety and Control
A profanity filter MUST be applied to all user-generated content (posts and comments) to maintain a healthy community environment. Users MUST have the ability to delete their own posts and comments at any time, without restriction, based on their browser identifier.

### IV. Mobile-First and Responsive Design
The UI MUST be designed with a mobile-first approach and be fully responsive across mobile, tablet, and desktop devices. The visual theme is fixed to a dark mode to ensure a consistent and emotionally stable user experience.

### V. Unrestricted Content Access
All content (posts and comments) is public and accessible to anyone without authentication. This includes reading posts, comments, and using the search functionality.

## Non-Functional Requirements

- **Performance**: Initial page load MUST be under 5 seconds. API responses MUST be under 1 second.
- **Platform**: The application MUST be a responsive web application. A SPA structure is recommended.
- **Technology Stack**: No specific stack is mandated, but the chosen stack MUST meet all performance requirements.

## Content Policy

- A profanity/slur filter MUST be implemented for post titles, content, and comments.
- Posts and comments are stored permanently and are not automatically deleted by the system.
- Image uploads are not supported; the platform is text-only.

## Governance

All development MUST adhere to the principles and rules outlined in this constitution. Any changes to these core principles require a formal amendment to this document, including a version increment and updated amendment date.

**Version**: 1.0.0 | **Ratified**: 2026-01-13 | **Last Amended**: 2026-01-13
