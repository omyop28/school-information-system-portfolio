# Features

This portfolio represents a private production-oriented school information system developed for SMA Negeri 1 Biak Kota.

The platform integrates public information services, administrative management, student admission, computer-based examinations, teacher attendance, mobile access, and desktop access within one application ecosystem.

## Public Website

The public website provides responsive access to school information across desktop, tablet, and Android devices.

Main areas include:

- Home
- School Profile
- Academic Information
- News and Announcements
- Student Admission Information
- Examination Information
- Teacher Attendance Information

Selected public information can be updated through Live Sync without requiring a full page reload.

## Administration Dashboard

The administration dashboard provides centralized management of the platform.

Key functions include:

- Website content management
- Image management
- Student admission configuration
- Examination administration
- Teacher attendance management
- Schedule management
- Dynamic form management
- Registration monitoring
- Document management
- Operational status management

## PPDB / SPMB

The student admission module supports configurable admission workflows.

Features include:

- Dynamic form builder
- Configurable form sections
- Dynamic input fields
- Admission paths
- Quota management
- Registration schedules
- Registration status
- Upload requirements
- Applicant data correction
- Re-registration
- Re-registration documents
- Administrative audit records

Dynamic forms allow administrators to configure registration requirements without rebuilding the complete form structure.

## USBK

The computer-based examination module supports digital examination workflows.

Main capabilities include:

- Participant management
- Examination configuration
- Examination schedules
- Waiting room
- Examination announcements
- Examination rules
- Examination session management
- Controlled real-time updates

Active examination states are protected from unsafe full-page synchronization to preserve answers, timers, navigation state, and submission processes.

## GPS-Based Teacher Attendance

The attendance system integrates device location into the teacher attendance workflow.

Features include:

- Check-in
- Check-out
- GPS location acquisition
- Location accuracy handling
- Attendance status
- Late attendance status
- Duplicate attendance protection

Sensitive GPS and submission operations are isolated from live content updates to avoid interrupting an active attendance process.

## Live Sync

Live Sync is used for selected informational areas of the system.

Supported areas include:

- Home
- School Profile
- Academic Information
- Public Information
- PPDB information
- PPDB schedules
- Admission paths and quotas
- Admission availability status
- Attendance information
- USBK portal information
- Examination schedules
- Examination announcements

Interactive states such as partially completed admission forms, active GPS submission, and active examinations are protected.

## Image Processing

The system includes reusable image handling for website content.

Capabilities include:

- Image upload
- WebP conversion
- File-size optimization
- Reusable upload processing
- Administrative image replacement

The objective is to improve delivery performance while keeping the administration workflow simple.

## Android Application

The Android application is implemented using:

- Java
- Android SDK
- Android WebView
- Gradle

The application provides mobile access to the school platform and has been tested on a physical Android device.

## Windows Desktop Application

Desktop application integration uses:

- Electron
- Node.js
- Web technologies

The Windows application provides another controlled access layer to the same backend platform.

## Security and Access Control

Security-related implementation and development work includes:

- Authentication
- Authorization
- Access control
- CSRF protection
- Input validation
- File-upload validation
- Application gateway architecture
- Device registration and approval
- Browser-access restriction research
- Security testing
- Vulnerability assessment

Security-sensitive production configuration is intentionally excluded from this public portfolio.

## Development and Maintenance

The project follows a conservative maintenance approach:

- Preserve stable business logic
- Identify root causes before modifying code
- Apply minimal targeted changes
- Validate changes after implementation
- Avoid unnecessary rewrites
- Maintain compatibility with existing workflows
