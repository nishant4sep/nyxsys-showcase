# NYX SYS — Northern Bloom

A desktop-first, offline-capable business management platform, built and deployed for a live salon client (Northern Bloom, Kathua). Built end to end — architecture, UI, backend, and the sync layer.

> Source is private — client data and business logic live in this codebase. This repo is a walkthrough of what it does. Screenshots with real customer/staff data have been redacted; the underlying UI is untouched.

**Stack:** Electron · React · TypeScript · SQLite · Express · Monorepo (desktop, booking, server, shared package)

---

## Architecture

- **Monorepo** — separate apps for desktop, booking site, and server, sharing a common package so business logic isn't duplicated across the desktop app and the public booking site.
- **Offline-first** — the desktop app works without a live connection and syncs when back online ("Synced · just now" in the header reflects this).
- **Role-based access** — distinct permission levels for Owner, Staff, Counter, and Developer, each seeing a different view of the same system.

---

## Login

PIN-based login, branded per salon.

![Login](./screenshots/login.png)

## Dashboard

Revenue trends, peak hours, staff performance, and service popularity at a glance.

![Dashboard](./screenshots/dashboard.png)

## POS Counter

A guided 3-step billing flow: find customer → select services → payment.

![POS Counter](./screenshots/pos-counter.png)

## Appointments

Calendar-based scheduling, filterable by status, with a live feed of bookings coming in from the public booking website.

![Appointments](./screenshots/appointments.png)

## Customers

Customer database with visit history and quick search by name or phone.

![Customers](./screenshots/customers.png)

## Attendance

Daily staff attendance tracking — present / half-day / absent, exportable to CSV.

![Attendance](./screenshots/attendance.png)

---

## Also in the system (not pictured here)

Counter billing with QR payments, staff commission tracking, inventory management, a developer-only admin panel for system config and backups, and a separate public booking website that syncs live with the desktop app.

---

## Status

Actively running for a real client. Still evolving — not a finished, feature-frozen product, but genuinely in daily use.
