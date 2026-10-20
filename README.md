# DeutschZiel

DeutschZiel is a modern web platform that helps students who want to study in Germany prepare their German student visa application with professional guidance.

It focuses exclusively on education-related German national visas and offers application preparation, document review, personal guidance, and consulting.

Website: https://deutsch-ziel.com (in Turkish, for students in Turkey)

## Overview

DeutschZiel makes the student visa preparation process clearer, more organized, and easier to manage, both for the student and for the consultant.

The platform brings together:

- A professional public website
- Service and package information
- A pre-application form for students
- An admin dashboard for the consultant
- Payment by bank transfer (IBAN)
- Email notifications for new applications
- WhatsApp and Google Meet communication
- Search engine optimization and privacy-friendly analytics
- A responsive design for desktop and mobile

## What We Do

DeutschZiel supports students who want to study in Germany with:

- German university student visas
- Language course + university routes
- Studienkolleg and preparatory education routes
- Student visa application preparation
- Document and application file review
- Guidance on the application forms
- Support with the motivation letter and CV, based on the student's own information
- Review of financing documents
- A final check of the complete application file

DeutschZiel does not submit visa applications on behalf of students. The student submits the official application from their own account and with their own approval. DeutschZiel does not guarantee any visa result; the decision belongs to the German authorities.

### What We Do Not Offer

DeutschZiel does not provide consulting for work visas, the Chancenkarte, tourist visas, family reunification, asylum, residence permit extensions, or other immigration categories.

## Website Features

### Public Website

The website includes:

- Home page
- Services page, with a detail page for each of the three services (document check, application support, full student visa support)
- Consulting packages with prices
- How It Works page
- About page
- Frequently asked questions
- Contact page
- Consultation application form
- Legal and privacy pages (privacy notice, privacy policy, distance service contract, pre-information form, cancellation and refund policy, legal notice)

Every page has its own title and description, a sitemap helps search engines, and private areas are kept out of search results.

The design is built around the idea of a path toward a goal, which is what the name "DeutschZiel" (German for "German goal") stands for.

### Consultation Application

A student describes their situation through a short, step-by-step application form. It asks about:

- Personal and contact details
- Current education
- Target university and program in Germany
- Planned start date and admission status
- Visa route and current stage of the application
- Previous visa applications or refusals
- German language level and certificates
- How the studies will be financed
- Which documents the student already has
- What kind of support they need

The form is checked both in the browser and on the server. It includes spam protection, limits on repeated submissions, and protection against sending the same application twice. The student must agree to the privacy notice and service terms before sending, and the time of this agreement is saved.

Applications are stored in the database and reviewed by the consultant in the admin dashboard.

### Admin Dashboard

The admin dashboard is a private area used only by the consultant. It lets the consultant:

- See an overview of new, pending, active, and completed cases
- Search and filter all applications
- Read everything a student submitted
- Move an application through the consulting process
- Write private notes that are never visible to students
- Choose a package and create a payment record
- Mark a payment as paid, cancelled, or refunded
- Contact a student with one click through WhatsApp or email

Documents are currently exchanged with students through WhatsApp.

### Payment

Payments are made by bank transfer (IBAN). The process is:

1. After reviewing an application, the consultant contacts the student and agrees on a package.
2. The consultant creates a payment record for that package in the admin dashboard and shares the bank details with the student directly.
3. Once the transfer is confirmed, the consultant marks the payment as paid, and the case moves on to the consulting phase.

Card payment through an online provider was prepared but is not in use, because the provider applications were not approved. The code for it is still part of the project and can be reactivated if an approved provider becomes available.

### Notifications

The consultant receives an email whenever a new consultation application arrives. The email contains only basic contact and route information, not the full application.

### Everyday User Experience

Visitors always see clear loading indicators, success messages, helpful error messages, and form validation feedback.

### Responsive Design

DeutschZiel works on desktop, laptop, tablet, and mobile devices. On phones, navigation is simplified into a menu, and WhatsApp and consultation request buttons are easy to reach.

## Tech Stack

The platform is built with widely used, modern tools:

- **Next.js, React, and TypeScript:** the website and its server-side logic
- **Tailwind CSS and shadcn/ui:** the look and feel of the interface
- **Supabase (PostgreSQL):** the database, plus the protected administrator login
- **Resend:** email notifications
- **Cloudflare:** hosting and the domain
- **Google Analytics:** optional visitor statistics, only used with the visitor's consent
- **GitHub:** source code storage and automatic publishing of every update

## Architecture

The website and the application logic run together in one Next.js application. Supabase provides the database and the login for the administrator. All access to stored data goes through the server, never directly from the visitor's browser.

How a visitor becomes a client:

Visitor → Website → Consultation Form → Database → Admin Dashboard

How a client starts a service:

Client → Consultant Review and Contact → Package Confirmed → Bank Transfer → Payment Confirmed in Admin → Consulting

## Security

Security matters because the platform handles personal information related to visa applications. In plain terms, the project includes:

- Checking every form on the server, not only in the browser
- A database where nothing is publicly readable; all access goes through the server
- A protected administrator login, with public sign-ups disabled and every admin page and action checking the administrator's identity
- Spam protection and limits on repeated attempts for the application form and the admin login
- Secret keys and passwords kept outside the code and never exposed to visitors
- Protective browser settings that reduce the risk of malicious scripts and unwanted embedding
- Analytics and cookies that only work with the visitor's explicit consent
- Error messages that never reveal technical details
- Private consultant notes that are never shown to students

## Design

The visual identity is based on a simple idea:

Start → Path → Goal

The interface uses:

- A light, easy-to-read page with a dark navy hero section and footer
- Germany-inspired black, red, and gold accents, including thin flag-colored stripes
- A softly moving, abstract flag background in the hero section, deliberately stylized rather than a literal flag
- Elegant serif headings
- Clean cards and sections
- Subtle animations
- Clear calls to action
- Consistent spacing and a layout that adapts to every screen size

The design intentionally avoids generic visa-agency imagery such as passports, airplanes, and official-looking government visuals.

## Customer Journey

Discovery → Website → Consultation Application → Application Review → Client Contact → Package Selection → Payment → Consulting → Document & Application Preparation

The application form lets the consultant understand a student's situation before the service begins. The first 15-minute consultation is free.

## Business Model

DeutschZiel is a bootstrapped online consulting business focused on German education and student visa preparation. The platform manages customer acquisition, consultation requests, payments, and application-related work in one place, with very low running costs.

## Scalability

The project is built so that new features can be added without starting over. Possible next steps:

- A sticky WhatsApp and consultation button bar on mobile
- A contact form with an inbox in the admin dashboard
- Online card payment, if an approved provider becomes available
- Secure document upload for clients
- Client accounts and personal dashboards
- Application progress tracking
- Automatic document checklists and reminders
- Document recognition and AI-assisted document analysis
- Customer relationship management features
- Automated email workflows

## Project Status

DeutschZiel is live and developed as a production-ready commercial platform.

Working today:

- Public website, application form, and admin dashboard
- Payment records and payments by bank transfer
- Email notifications for new applications
- Search engine optimization, consent-based analytics, and security measures

Next:

- Making payment confirmation and agreement approval more automatic
- Secure document upload
- Mobile quick-action bar

## License

This project is proprietary software developed for DeutschZiel.

The source code, branding, content, design, and business logic are not licensed for redistribution, modification, or commercial reuse without permission.
