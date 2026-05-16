# Attendrix

Attendrix is a modern academic management and student engagement platform built for NIT Calicut.

The platform combines attendance tracking, semester scheduling, academic productivity tools, realtime synchronization, and a gamified engagement system into a unified ecosystem designed specifically around institute workflows.

Unlike traditional ERP systems that focus primarily on administrative data storage, Attendrix is designed around the day-to-day academic experience of students.

---

# Core Philosophy

Attendrix is built around a few core architectural principles:

* Attendance should be frictionless.
* Academic systems should reflect real institutional workflows.
* Data should have a single source of truth.
* Realtime updates should eliminate stale state.
* Gamification should reinforce academic consistency.
* Semester structure should act as the backbone of the platform.

---

# Key Features

## Academic Scheduling Engine

Attendrix models NIT Calicut’s slot-based academic system using a two-tier scheduling architecture:

* Institute-defined slot timings
* Department-configurable lab schedules

The full semester schedule is generated upfront using the academic calendar, allowing students to access their entire semester plan from day one.

---

## Inverted Attendance System

Students are considered present by default.

Instead of storing attendance for every student in every class, Attendrix stores only absences.

This significantly reduces:

* duplicate records
* race conditions
* write amplification
* attendance inconsistency

Attendance percentages and analytics are computed directly from the source schedule and absence records.

---

## Streak & Amplix Gamification Engine

Attendrix includes a fully integrated engagement system:

* attendance streaks
* academic challenges
* achievements
* Amplix reward currency

Students earn rewards through consistent attendance and academic participation.

The system uses:

* immutable reward ledgers
* realtime updates
* automated challenge generation
* transactional reward claiming

---

## Tasks & Academic Productivity

Students can manage:

* assignments
* exams
* deadlines
* tutorials
* academic reminders

through a centralized academic workspace.

---

## Realtime Synchronization

Attendrix uses Supabase Realtime infrastructure to instantly synchronize:

* attendance updates
* streak changes
* rewards
* challenge completions
* schedule changes
* notifications

across all connected clients.

---

# High-Level Architecture

```text
Student App / Admin Dashboard
            ↓
      RPC & API Layer
            ↓
    Automation & Cron Jobs
            ↓
  Event & Realtime Systems
            ↓
 PostgreSQL + Supabase Backend
```

Core backend components:

* PostgreSQL
* Supabase Auth
* Row Level Security (RLS)
* Edge Functions
* Realtime Subscriptions
* Cron-based automation
* Transactional RPC functions

---

# Repository Structure

| Repository      | Purpose                                           |
| --------------- | ------------------------------------------------- |
| backend         | Database schema, RPCs, triggers, edge functions   |
| mobile-app      | Flutter application                               |
| admin-dashboard | Administrative dashboard                          |
| docs            | Architecture diagrams and technical documentation |
| infrastructure  | CI/CD and deployment configuration                |

---

# Technology Stack

| Layer            | Technology           |
| ---------------- | -------------------- |
| Mobile App       | Flutter              |
| Admin Dashboard  | Next.js + TypeScript |
| Backend          | Supabase             |
| Database         | PostgreSQL           |
| Authentication   | Supabase Auth        |
| State Management | Riverpod             |
| Infrastructure   | GitHub Actions       |
| Realtime         | Supabase Realtime    |

---

# Development Principles

The project follows:

* schema-first backend design
* migration-driven database evolution
* protected branching workflow
* feature-based architecture
* structured issue tracking
* milestone-driven development
* mandatory code reviews
* centralized architectural ownership

---

# Current Development Milestones

| Milestone | Focus Area           |
| --------- | -------------------- |
| M1        | Scheduling Engine    |
| M2        | Attendance Core      |
| M3        | Streak System        |
| M4        | Amplix Engine        |
| M5        | Challenges           |
| M6        | Tasks & Exams        |
| M7        | Notifications        |
| M8        | Admin Dashboard      |
| M9        | Production Readiness |

---

# Contribution Workflow

```text
feature branch
    ↓
pull request
    ↓
review
    ↓
staging
    ↓
main
```

All changes are expected to:

* pass linting
* pass testing
* follow architectural conventions
* include documentation updates where required

---

# Long-Term Vision

Attendrix aims to evolve beyond a conventional academic tracker into a scalable academic operating system capable of supporting:

* institutional scheduling
* student productivity
* engagement systems
* analytics
* academic insights
* campus-scale operational workflows

while remaining aligned with the real academic structure of engineering institutions.
