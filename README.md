# Zoolee™  — Oral Hygiene Habit Tracker

A mobile-first habit-tracking app that helps users build consistent brushing and flossing routines through timed sessions, streak tracking, and positive reinforcement.

## About This Project

Built by a licensed dental hygienist (CompTIA Security+, Network+) currently pivoting into tech, combining clinical oral health expertise with product design and AI-assisted development. This project is being used to demonstrate technical judgment, specification writing, and system design thinking as part of that transition — not just to ship an app, but to prove the process behind it.

# Security Policy

## Reporting a Vulnerability

Please report security issues privately using GitHub's [private vulnerability reporting](../../security/advisories/new) feature — do not open a public issue.

Expect an initial response within 72 hours.

## Scope
This is a pre-launch project. Findings related to auth, RLS, data exposure,
webhook verification, and encryption are especially welcome.


## What It Does

- Guided, timed brushing and flossing sessions that auto-complete tracking on finish
- Manual logging fallback for sessions completed outside the app
- Streak tracking with milestone recognition
- Positive reinforcement system designed around real habit-formation principles, not just generic gamification
- Evergreen oral hygiene guidance, written from a licensed hygienist's perspective
- (Planned) Curated product recommendations
- (Planned, future phase) Subscription access to professional guidance, pending legal/compliance review

## Tech Stack

- Built with [Lovable](https://lovable.dev) (AI-assisted full-stack development)
- Frontend: React, Tailwind CSS
- Backend/Database: Supabase
- Hosted/deployed via [deployment platform]

## Development Approach

This project was built by writing detailed feature specifications — including expected behavior, edge cases, and "done" criteria - before implementation, then using AI tooling to execute against those specs. Notable design decisions include:

- Deliberate handling of edge cases in timer-based logging (e.g., interrupted sessions, ambiguous session states)
- Differentiated reward feedback between real-time completions and manual/fallback logging, to preserve incentive design integrity
- Data handling built with user privacy in mind from the start

## Status

In active development - not yet publicly launched.

## Getting Started

This project is deployed on Lovable and requires provisioned backend services (Supabase, Paddle, Lovable AI Gateway) to run locally. See [docs/ARCHITECTURE.md](docs/ARCHITECTURE.md) for the full setup.

## Roadmap

**Phase 1 - Core Habit Loop (current)**
- Timed brushing and flossing sessions with auto-completion
- Manual logging fallback
- Streak tracking and milestone rewards
- Core oral hygiene guidance content

**Phase 2 - Commerce**
- Curated product recommendations, tied to usage context rather than shown up front
- Shopify integration for direct purchase

**Phase 3 - Professional Access (pending legal/compliance review)**
- Subscription tier for professional guidance
- Scope-of-practice safeguards and required legal disclaimers
- State-by-state licensing compliance review before any rollout

**Future considerations**
- Expanded personalization (custom reminder schedules, detailed stats)
- Broader platform support

## Author

Rachel Sady — Licensed Dental Hygienist | CompTIA Security+, Network+ | Career pivot into cybersecurity/tech

## License

All rights reserved. This project is not licensed for public use, reproduction, or distribution at this time.
