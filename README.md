# NYX SYS

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

## Booking Website

A separate, public-facing app (Next.js) that lets customers book appointments directly — syncs with the desktop app in real time through the shared package. Live and in daily use.

**Live: [northernbloom.in](https://northernbloom.in)** — 4.5★ on Google, 780+ reviews.

<table>
  <tr>
    <td align="center"><img src="./screenshots/booking-home.jpg" width="200"/><br/><sub>Home</sub></td>
    <td align="center"><img src="./screenshots/booking-home-light.jpg" width="200"/><br/><sub>Home (Light)</sub></td>
    <td align="center"><img src="./screenshots/booking-packages.jpg" width="200"/><br/><sub>Packages</sub></td>
    <td align="center"><img src="./screenshots/booking-reviews.jpg" width="200"/><br/><sub>Reviews</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="./screenshots/booking-select-service.jpg" width="200"/><br/><sub>Select Service</sub></td>
    <td align="center"><img src="./screenshots/booking-select-service-gents.jpg" width="200"/><br/><sub>Gents Services</sub></td>
    <td align="center"><img src="./screenshots/booking-select-staff.jpg" width="200"/><br/><sub>Select Staff</sub></td>
    <td align="center"><img src="./screenshots/booking-select-time.jpg" width="200"/><br/><sub>Select Time</sub></td>
  </tr>
  <tr>
    <td align="center"><img src="./screenshots/booking-your-details.jpg" width="200"/><br/><sub>Your Details</sub></td>
    <td align="center"><img src="./screenshots/booking-review-confirm.jpg" width="200"/><br/><sub>Review & Confirm</sub></td>
    <td align="center"><img src="./screenshots/booking-confirmed.jpg" width="200"/><br/><sub>Confirmed</sub></td>
    <td></td>
  </tr>
</table>

## Also in the system (not pictured here)

Counter billing with QR payments, staff commission tracking, inventory management, and a developer-only admin panel for system config and backups.

---

## Status

Actively running for a real client. Still evolving — not a finished, feature-frozen product, but genuinely in daily use.
