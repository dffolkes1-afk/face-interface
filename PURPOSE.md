# FACE Interface — Product Purpose

## What this project is

FACE Interface is the member-facing application layer for FACE, the social platform. It is the place where a person signs in, creates and manages a profile, discovers people and communities, shares content, communicates, and controls their experience.

It is not a generic screen for displaying scores from internal engines. Its primary job is to make the FACE social product usable, clear, accessible, and safe.

## Member-facing areas

The interface is organized around these product areas:
- Account access, onboarding, and account settings.
- Member profile and profile privacy.
- Home feed and content creation.
- Post details, comments, replies, and reactions.
- People and community discovery.
- Groups and creator spaces.
- Direct and group messaging.
- Notifications and activity.
- Safety centre: block, report, mute, privacy controls, and account recovery.
- Optional voice entry points supplied by FACE–Voice Core.

## Interaction requirements

- Show a clear loading, empty, success, and error state for every major workflow.
- Respect server-side authorization; hiding a control is never a substitute for access control.
- Make privacy and audience selection understandable before content is published.
- Never expose private messages, hidden profiles, or restricted content through client state, URLs, caches, or search.
- Provide keyboard navigation, semantic controls, readable contrast, and responsive layouts.
- Do not make biometric capture mandatory for registration or ordinary social participation.

## Architecture boundary

FACE Interface presents and collects user actions. FACE's application services enforce business rules and authorization. FACE Interface must not contain private scoring algorithms, hidden decision logic, or direct credentials for internal services.

Voice features are optional and are integrated through documented FACE–Voice Core contracts. VoiceScore outputs are not used as social popularity scores, member rankings, or access-control decisions.

## Build order

1. Navigation and application shell.
2. Authentication and onboarding screens.
3. Profile and privacy settings.
4. Feed, posts, comments, and reactions.
5. Connections, groups, and discovery.
6. Messaging and notifications.
7. Safety and moderation flows.
8. Optional voice experiences.
9. Accessibility, responsive behaviour, and end-to-end tests.

## Current implementation status

This charter defines the interface's purpose and required areas. It does not claim that screens, services, or integrations are already implemented.
