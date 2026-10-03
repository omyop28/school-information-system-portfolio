# School Information System

A full-stack school information and application platform developed for **SMA Negeri 1 Biak Kota**, built with **CodeIgniter 4, PHP, MySQL, JavaScript, HTML, and CSS**.

The project integrates public information services, administrative management, student admission, computer-based examinations, GPS-based teacher attendance, real-time content synchronization, image optimization, Android access, and Windows desktop integration.

> **Portfolio Notice**
>
> This repository is a technical portfolio showcase of a private production system.  
> Production source code, credentials, cryptographic keys, personal data, internal configuration, and other security-sensitive components are not publicly available.

---

## Overview

The system was designed as an integrated platform for school information management and digital services.

It combines multiple modules within one backend architecture while maintaining responsive access across desktop browsers, Android devices, and desktop applications.

The main development focus includes:

- Full-stack web development
- Backend architecture
- Database integration
- Responsive user interfaces
- Dynamic form systems
- Real-time content synchronization
- Mobile WebView integration
- Desktop application integration
- Security testing
- Performance optimization
- Debugging and production-oriented development

---

## Main Features

### Public Website

The public-facing website provides school information through responsive pages including:

- Home
- School Profile
- Academic Information
- News and Information
- Student Admission Information
- Examination Information
- Teacher Attendance Information

Content managed from the administration dashboard can be synchronized to public pages without requiring a full browser refresh.

---

## Administration Dashboard

The administration system provides centralized management for website content and operational modules.

Key capabilities include:

- Content management
- Image management
- Student admission configuration
- Examination management
- Teacher attendance management
- Dynamic form configuration
- Schedule management
- Registration monitoring
- Document management
- Administrative workflows

The development approach prioritizes preserving existing business logic and applying minimal, targeted changes when fixing or improving stable functionality.

---

## PPDB / SPMB — Student Admission System

The admission module supports dynamic registration workflows.

Selected capabilities include:

- Dynamic registration forms
- Configurable form sections
- Configurable fields
- Admission paths
- Admission quotas
- Registration schedules
- Registration status
- Document requirements
- Applicant data correction
- Re-registration
- Registration documents
- Audit records

The form structure can be configured through the administration system without requiring hard-coded registration forms for every admission period.

---

## USBK — Computer-Based Examination

The computer-based examination module provides digital examination functionality.

Selected areas include:

- Student participants
- Examination configuration
- Examination schedules
- Examination announcements
- Examination rules
- Waiting room
- Examination session handling

Real-time updates are intentionally controlled during active examinations to protect answers, timers, navigation state, and submission processes.

---

## GPS-Based Teacher Attendance

The teacher attendance module uses device location data as part of the attendance workflow.

Features include:

- Check-in
- Check-out
- GPS location acquisition
- Location accuracy validation
- Attendance status
- Late attendance handling
- Duplicate attendance protection

The system separates informational updates from sensitive GPS and submission operations to avoid disrupting an active attendance process.

---

## Live Sync

The project includes a live synchronization mechanism for selected public information.

Live synchronization is used for:

- Home content
- School profile
- Academic information
- Public announcements
- Student admission information
- Admission schedules
- Admission quotas
- Admission status
- Attendance information
- Examination portal information
- Examination schedules
- Examination announcements

Interactive processes such as active registration forms, GPS submissions, and live examinations are protected from unsafe full-page synchronization.

---

## Image Optimization

Uploaded website images can be processed through a reusable image optimization workflow.

The system supports:

- Automatic image processing
- WebP conversion
- File-size optimization
- Reusable upload handling
- Administrative image replacement

The goal is to reduce bandwidth and improve page-loading performance without requiring administrators to manually optimize every uploaded image.

---

## Android Application

An Android application was developed using:

- Java
- Android SDK
- Android WebView
- Gradle

The Android application acts as an application layer for accessing the school platform from mobile devices.

Development testing included installation and testing on a physical Android device.

---

## Windows Desktop Application

The project also includes desktop application development using:

- Electron
- Node.js
- Web technologies

The desktop application is intended to provide access to the same school platform through a Windows application environment.

---

## Technology Stack

### Backend

- PHP
- CodeIgniter 4
- MySQL
- REST-oriented backend integration

### Frontend

- HTML5
- CSS3
- JavaScript
- Responsive Web Design

### Mobile

- Java
- Android SDK
- Android WebView
- Gradle

### Desktop

- Electron
- Node.js

### Development & Security

- Git
- GitHub
- OWASP ZAP
- Nuclei
- Browser Developer Tools
- Android debugging tools

---

## Architecture

High-level architecture:

```text
                     ┌──────────────────────┐
                     │      End Users       │
                     └──────────┬───────────┘
                                │
              ┌─────────────────┼─────────────────┐
              │                 │                 │
              ▼                 ▼                 ▼
      Web Browser       Android Application   Windows App
                           WebView              Electron
              │                 │                 │
              └─────────────────┼─────────────────┘
                                │
                                ▼
                    ┌──────────────────────┐
                    │  CodeIgniter 4 App   │
                    │                      │
                    │ Controllers          │
                    │ Validation           │
                    │ Business Logic       │
                    │ Authentication       │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │        MySQL         │
                    │                      │
                    │ Website Content      │
                    │ PPDB / SPMB          │
                    │ USBK                 │
                    │ Attendance           │
                    │ Audit Data           │
                    └──────────────────────┘
```

More detailed architecture documentation will be available in:

```text
docs/architecture.md
```

---

## Security Engineering

Security is treated as part of the development process rather than as a separate final step.

Security-related work includes:

- Authentication
- Authorization
- Access control
- CSRF protection
- Input validation
- Output handling
- File upload validation
- Security testing
- Vulnerability scanning
- Application access architecture
- Device-access research and development

Security testing tools used during development include:

- OWASP ZAP
- Nuclei

Application authentication gateway and stronger device-level access controls are being developed separately from the public portfolio repository.

Sensitive implementation details are intentionally excluded from this repository.

---

## Development Principles

This project follows several practical engineering principles:

1. Preserve stable business logic whenever possible.
2. Identify the root cause before applying a fix.
3. Prefer small and targeted changes.
4. Validate changes after implementation.
5. Protect user data and private configuration.
6. Separate public information updates from sensitive active workflows.
7. Test changes on the actual target environment when possible.

---

## Screenshots

Screenshots will be organized by module:

```text
screenshots/
├── public/
├── admin/
├── ppdb/
├── usbk/
├── attendance/
├── android/
└── windows/
```

Only screenshots that do not expose personal information, credentials, private documents, internal security configuration, or production-sensitive information will be published.

---

## Project Structure

```text
school-information-system-portfolio/
│
├── README.md
│
├── screenshots/
│   ├── public/
│   ├── admin/
│   ├── ppdb/
│   ├── usbk/
│   ├── attendance/
│   ├── android/
│   └── windows/
│
├── docs/
│   ├── architecture.md
│   ├── features.md
│   └── security-overview.md
│
├── diagrams/
│   ├── system-architecture.png
│   └── authentication-flow.png
│
└── demo/
    └── README.md
```

---

## My Role

**Full-Stack Web & Application Developer**

Responsibilities include:

- Backend development
- Frontend development
- Database integration
- Dynamic form implementation
- Administrative dashboard development
- Android application integration
- Windows desktop application integration
- Debugging
- Performance optimization
- Security testing
- Git and GitHub workflow
- Deployment preparation
- System maintenance and iterative improvement

---

## Technical Challenges

Some of the main engineering challenges addressed during development include:

- Maintaining multiple integrated school modules within a single application
- Protecting active user workflows during real-time content synchronization
- Building dynamic admission forms
- Managing examination state safely
- Integrating GPS-based attendance
- Maintaining responsive layouts across desktop and Android devices
- Optimizing uploaded images automatically
- Integrating a web platform into Android WebView
- Preparing the platform for desktop application access
- Improving security without breaking established business logic

---

## Privacy

This project involves systems that may process sensitive school information.

For privacy and security reasons, this repository does **not** contain:

- Student personal data
- Teacher personal data
- Production database dumps
- Registration documents
- Examination answers
- GPS attendance records
- `.env` files
- Database credentials
- API tokens
- Private keys
- Application signing keys
- Administrative credentials
- Sensitive production configuration

---

## Project Status

**Active Development / Private Production System**

The complete production source code is maintained privately.

This repository exists specifically as a professional portfolio and technical documentation showcase.

A controlled demonstration may be provided upon request where appropriate.

---

## Developer

**Full-Stack Web & Application Developer**

Primary areas:

`PHP` · `CodeIgniter 4` · `MySQL` · `JavaScript` · `HTML` · `CSS` · `Android WebView` · `Electron` · `REST API` · `Application Security` · `Git` · `GitHub`
