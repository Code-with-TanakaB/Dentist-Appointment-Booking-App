# Technical Scope of Work Appendix
## Contract Attachment - Dentist Appointment Booking App

Document Version: 1.0  
Date: 08 April 2026

---

## 1) Purpose
This appendix defines the technical implementation scope, quality standards, security controls, and acceptance criteria for production launch.

## 2) System Overview
The solution is a web application comprising:
- Frontend user interface for browsing services and booking appointments.
- Backend API for authentication, appointments, and account operations.
- PostgreSQL database for persistent user and booking data.
- Notification layer for email confirmations and optional reminders.

## 3) In-Scope Technical Deliverables

### 3.1 Frontend
- Responsive patient-facing interface for mobile, tablet, and desktop.
- Service listing, booking wizard, booking management pages.
- Sign-up/sign-in UI and validation feedback.
- Chatbot UI and timed engagement prompts.

### 3.2 Backend API
- REST endpoints for:
  - Account registration
  - Account sign-in/sign-out
  - Password reset workflow
  - Appointment create/read/update/cancel
  - Basic profile read/update
- Server-side input validation and error handling.

### 3.3 PostgreSQL Database
- Schema creation and migration scripts.
- Required core tables:
  - users
  - appointments
  - auth_sessions (if custom auth)
  - audit_log
- Indexes and constraints for performance and integrity.

### 3.4 Security Controls
- Password hashing using bcrypt or Argon2id.
- Email verification for newly created accounts.
- Secure token/session handling.
- Rate limiting for sensitive endpoints.
- Basic bot mitigation for auth/booking forms.
- HTTPS-only production deployment.

### 3.5 DevOps and Deployment
- Production hosting setup (frontend + backend + database).
- Environment variables and secret management.
- Domain + SSL configuration.
- Basic monitoring/logging setup.

## 4) Out-of-Scope (Unless Added by Change Request)
- Native mobile applications.
- Advanced admin portal with role matrix and reporting suite.
- External enterprise integrations (medical aid switching, accounting, etc.).
- Full multilingual localization beyond current language set.

## 5) Non-Functional Requirements
- Performance: key pages should load quickly on typical 4G/5G and broadband.
- Availability: target stable uptime supported by chosen host plan.
- Accessibility: readable UI with clear form labels and visible focus states.
- Maintainability: structured code and environment configuration documentation.

## 6) Data Protection and Compliance Baseline
- Collect minimum personal data required for booking operations.
- Encrypt data in transit (TLS) and rely on managed DB encryption at rest.
- Restrict production DB credentials to least privilege.
- Maintain audit logs for sensitive account and booking actions.
- Prepare privacy policy and POPIA-aligned consent language.

## 7) Acceptance Criteria
Project is considered complete when:
1. Users can register, verify, sign in, and reset password successfully.
2. Appointment data persists in PostgreSQL across sessions.
3. Patient can create, view, and cancel bookings reliably.
4. Core validation and error states are handled on frontend and backend.
5. Security controls listed in section 3.4 are implemented and tested.
6. App is deployed to production URL with SSL enabled.
7. Handover documentation is provided.

## 8) Testing and QA
- Functional tests of auth and booking flows.
- Form validation tests for invalid/edge inputs.
- Cross-device responsive checks.
- Production smoke test after deployment.

## 9) Dependencies and Client Responsibilities
- Client provides:
  - Approved branding/assets/copy
  - Legal policy text (privacy/terms)
  - Access to domain registrar (if required)
- Provider requires timely feedback to maintain timeline.

## 10) Change Control
Any work outside this scope is documented as a change request including:
- Description of requested change
- Impact on timeline
- Additional cost in ZAR
- Approval sign-off before implementation

---

## Sign-Off
Client Representative: Dr. LM. Mankgele  
Signature: _____________________________  
Date: _________________________________  

Service Provider: WebGemini by Tanaka Bvekerwa  
Signature: _____________________________  
Date: _________________________________
