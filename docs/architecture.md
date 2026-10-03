# System Architecture

## Overview

The system follows a modular web application architecture built primarily with CodeIgniter 4 and MySQL.

Multiple client environments access the same backend platform:

- Web browsers
- Android application
- Windows desktop application

## High-Level Architecture

```text
                    ┌─────────────────────┐
                    │        Users        │
                    └──────────┬──────────┘
                               │
           ┌───────────────────┼───────────────────┐
           │                   │                   │
           ▼                   ▼                   ▼
     Web Browser        Android Application    Windows App
                            WebView              Electron
           │                   │                   │
           └───────────────────┼───────────────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Web / Gateway    │
                    │       Layer         │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   CodeIgniter 4     │
                    │                     │
                    │ Routing             │
                    │ Controllers         │
                    │ Validation          │
                    │ Authentication      │
                    │ Authorization       │
                    │ Business Logic      │
                    │ Services            │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │        MySQL        │
                    │                     │
                    │ Website Content     │
                    │ PPDB / SPMB         │
                    │ USBK                │
                    │ Attendance          │
                    │ Audit Data          │
                    └─────────────────────┘
```

## Backend

The backend is built using PHP and CodeIgniter 4.

Responsibilities include:

- Request routing
- Validation
- Authentication
- Authorization
- Business-rule enforcement
- Database access
- File handling
- Administrative workflows
- Public content delivery

## Database

MySQL is used as the primary relational database.

Application data is organized by functional domain, including:

- Website content
- Student admission
- Registration answers
- Registration documents
- Re-registration
- Examination data
- Attendance data
- Schedules
- Audit information

Production database content is not included in this repository.

## Public and Administrative Layers

The system separates public-facing functionality from administrative functionality.

The public layer focuses on:

- Information delivery
- Registration access
- Examination access
- Attendance interfaces

The administrative layer manages:

- Content
- Configuration
- Registration workflows
- Examination configuration
- Attendance information
- Operational settings

## Live Synchronization

Live Sync provides targeted information updates.

The architecture intentionally avoids indiscriminate full-DOM replacement.

Protected states include:

- Registration forms currently being completed
- File selections
- GPS acquisition
- Attendance submission
- Examination answers
- Examination timers
- Examination navigation

This reduces the risk of real-time updates interfering with active user workflows.

## Android Integration

The Android client uses Java, Android WebView, the Android SDK, and Gradle.

The application acts as a mobile client for the existing platform while retaining the backend as the primary source of business rules and authorization.

## Desktop Integration

The Windows desktop client uses Electron and Node.js.

The desktop application provides access to the same backend without duplicating the primary business logic in the client.

## Application Gateway

A separate application-authentication layer is being developed for controlled application access.

The architecture separates:

1. Application or device verification
2. User authentication
3. User authorization
4. Business permissions

This ensures that successful application verification alone does not automatically grant access to protected functionality.

Detailed production gateway configuration and cryptographic material are not published.

## Design Principle

The architecture follows one important rule:

> Stable production business logic should not be changed unless there is a clear technical requirement.

Bug fixes and improvements are therefore designed to be targeted, reversible, and validated against existing system behavior.
