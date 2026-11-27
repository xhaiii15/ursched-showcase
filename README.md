<div align="center">

<img src="assets/ursched-logo.png" alt="UrSched logo" width="96" height="96">

# UrSched

### Intelligent scheduling, simplified.

Describe your plans in plain language. See them on a clean calendar. Never miss a thing.

<br>

[![Live Demo](https://img.shields.io/badge/LIVE_DEMO-ursched--two.vercel.app-168A83?style=for-the-badge&logo=vercel&logoColor=white)](https://ursched-two.vercel.app)
[![Status](https://img.shields.io/badge/STATUS-IN_DEVELOPMENT-F59E0B?style=for-the-badge)](docs/ROADMAP.md)
[![License](https://img.shields.io/badge/LICENSE-ALL_RIGHTS_RESERVED-555555?style=for-the-badge)](LICENSE)

<br>

[**Overview**](#-overview) ·
[**Features**](#-features) ·
[**Screenshots**](#-screenshots) ·
[**Tech Stack**](#-tech-stack) ·
[**Security**](#-security--privacy) ·
[**Roadmap**](#-roadmap) ·
[**Contact**](#-about-the-developer)

<br>

<img src="assets/screenshots/calendar-month.png" alt="UrSched month calendar view" width="900">

</div>

<br>

> [!NOTE]
> **UrSched is currently in active development.** Expect bugs and rough edges, and expect frequent updates as new features and fixes ship. If you run into something broken, please [open an issue](https://github.com/xhaiii15/ursched-showcase/issues/new/choose). Feedback is genuinely appreciated.

<br>

## 📖 Overview

**UrSched** is a scheduling web app built to remove the busywork from planning your time. Instead of filling out forms, you type what you have planned, such as _"Lunch with Ana tomorrow at 12:30"_, and UrSched turns it into a calendar event. Month and agenda views keep your schedule readable, and conflicts are flagged before you save.

<table>
  <tr>
    <td><b>Product</b></td>
    <td>Responsive scheduling web application</td>
  </tr>
  <tr>
    <td><b>Status</b></td>
    <td>Live, in active development</td>
  </tr>
  <tr>
    <td><b>Try it</b></td>
    <td><a href="https://ursched-two.vercel.app">ursched-two.vercel.app</a></td>
  </tr>
  <tr>
    <td><b>Source code</b></td>
    <td>Private. This repository holds documentation and media only.</td>
  </tr>
</table>

<br>

## ✨ Features

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>✍️ Plain-language events</h4>
      Type a sentence instead of filling out a form. UrSched handles the title, date, and time.
    </td>
    <td width="50%" valign="top">
      <h4>🗓️ Month and agenda views</h4>
      A broad monthly overview, or a focused list grouped by date with the newest first.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>⚠️ Conflict checks</h4>
      Overlapping events are flagged before you save, so double-booking is hard to do by accident.
    </td>
    <td width="50%" valign="top">
      <h4>🎨 Status at a glance</h4>
      Upcoming, ongoing, and past events are color-coded so you can scan your day in seconds.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>✨ AI-created markers</h4>
      Events made from plain language carry a clear label, so you always know where they came from.
    </td>
    <td width="50%" valign="top">
      <h4>🔔 Reminders</h4>
      Keep upcoming plans visible so nothing slips past you.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>🌓 Light and dark themes</h4>
      A consistent color system that looks right in both modes.
    </td>
    <td width="50%" valign="top">
      <h4>📱 Fully responsive</h4>
      Designed to work comfortably on phones, tablets, and desktops.
    </td>
  </tr>
</table>

<br>

### How plain-language creation works

```mermaid
flowchart LR
  A["Type a sentence<br/><i>Dentist next Friday 3pm</i>"] --> B["UrSched interprets<br/>title, date, time"]
  B --> C{"Overlaps an<br/>existing event?"}
  C -- Yes --> D["Conflict flagged<br/>before saving"]
  C -- No --> E["Event added<br/>to your calendar"]
  D --> E
```

This shows the user-facing experience only. Prompts and model internals are not published.

<br>

## 📸 Screenshots

> All screenshots use sample data only.

<table>
  <tr>
    <td align="center" width="50%">
      <img src="assets/screenshots/agenda.png" alt="Agenda view grouped by date" width="100%"><br>
      <sub><b>Agenda view</b><br>Events grouped by date with status colors</sub>
    </td>
    <td align="center" width="50%">
      <img src="assets/screenshots/ai-event-creation.png" alt="Creating an event from a sentence" width="100%"><br>
      <sub><b>Plain-language creation</b><br>Type a sentence, get an event</sub>
    </td>
  </tr>
</table>

<div align="center">
  <img src="assets/screenshots/mobile-calendar.png" alt="UrSched on mobile" width="240"><br>
  <sub><b>Mobile</b><br>Responsive down to the smallest screens</sub>
</div>

<br>

## 🛠️ Tech Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=react,ts,tailwind,nodejs,postgres,vercel&theme=dark" alt="React, TypeScript, Tailwind CSS, Node.js, PostgreSQL, Vercel">

</div>

| Layer        | Technologies                               |
| :----------- | :----------------------------------------- |
| **Frontend** | React, TypeScript, Tailwind CSS, shadcn/ui |
| **Backend**  | Node.js                                    |
| **Database** | Neon (serverless Postgres)                 |
| **Hosting**  | Vercel                                     |

### Architecture at a glance

```mermaid
flowchart LR
  Browser["🌐 Browser"] --> UI["⚛️ React frontend"]
  UI --> API["🔌 Application API"]
  API --> DB[("🗄️ Neon Postgres")]
  API --> AI["✨ AI service"]
```

A high-level view only. Endpoints, schema, and implementation details are intentionally omitted. For a plain-language walkthrough, see [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md).

<br>

## 🔒 Security & Privacy

UrSched takes a layered, defense-in-depth approach to session security and is served over HTTPS. Privacy is part of the product: the policies below are public, and sign-up asks for explicit agreement to them.

[Terms of Service](https://ursched-two.vercel.app/terms) · [Privacy Policy](https://ursched-two.vercel.app/privacy) · [Cookie Policy](https://ursched-two.vercel.app/cookies)

Found a vulnerability in the live app? Please follow the steps in [SECURITY.md](SECURITY.md).

<br>

## 🗺️ Roadmap

UrSched is evolving quickly. These are planned directions, not delivery commitments. More detail lives in [docs/ROADMAP.md](docs/ROADMAP.md).

- [x] Natural-language event creation
- [x] Month and agenda views
- [x] Conflict checks and event status colors
- [x] Light and dark themes
- [ ] Clearer onboarding and reminder setup
- [ ] Calendar readability and accessibility refinements
- [ ] Optional calendar integrations
- [ ] Richer planning views

<br>

## 👨‍💻 About the Developer

Built by **Charlie Melorin**, an independent developer focused on creating useful, approachable web products.

[![Portfolio](https://img.shields.io/badge/Portfolio-charliemelorin.vercel.app-0F172A?style=flat-square&logo=vercel&logoColor=white)](https://charliemelorin.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-charliemelorin-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/charliemelorin)
[![GitHub](https://img.shields.io/badge/GitHub-xhaiii15-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/xhaiii15)

Have feedback or an idea? [Open an issue](https://github.com/xhaiii15/ursched-showcase/issues/new/choose). If you like what you see, a ⭐ on this repo is always appreciated.

<br>

## 📄 License

This repository contains documentation and media only, and its contents are **All Rights Reserved** ([LICENSE](LICENSE)). The UrSched application source code is private and proprietary, and no license to it is granted by this repository.

<br>

<div align="center">
  <sub>Built with care in the Philippines 🇵🇭</sub>
</div>
