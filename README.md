# 🏏 BPL App

> Official mobile application for the **Bhalawani Premier League (BPL)**.

BPL App is a modern mobile application built with **React Native and Expo** to provide a complete digital experience for the Bhalawani Premier League.

The application is designed to bring tournament information, live matches, teams, players, points tables, auction updates, registration, news, gallery, and other BPL features into a single mobile experience.

---

## 📱 About BPL

**Bhalawani Premier League (BPL)** is a local cricket tournament designed to bring players, teams, supporters, and the community together through competitive cricket.

The BPL digital ecosystem consists of multiple applications and services:

```text
BPL Ecosystem
│
├── BPL Web
├── BPL App
├── BPL Admin
└── BPL API
```

The **BPL App** is the mobile application layer of this ecosystem.

---

## 🚀 Project Status

**Status:** 🚧 In Development

The application is being developed incrementally, starting with the core mobile experience and expanding toward real-time tournament features.

---

## 🛠️ Tech Stack

### Mobile

- React Native
- Expo
- Expo Router
- TypeScript

### State Management

- Zustand

### Networking

- Axios
- REST API

### Real-Time Features

- Socket.IO Client

### Forms & Validation

- React Hook Form
- Zod

### Storage

- AsyncStorage
- Secure Storage

### UI & Animation

- React Native Reanimated
- Expo Vector Icons
- Custom Design System

### Development

- ESLint
- Prettier
- Jest
- React Native Testing Library

### Backend Integration

```text
React Native App
        │
        ▼
   BPL REST API
        │
        ├── Authentication
        ├── Matches
        ├── Teams
        ├── Players
        ├── Points Table
        ├── Auction
        ├── Registration
        ├── Gallery
        └── News
        │
        ▼
    MongoDB
```

---

# ✨ Features

## 🏠 Home

The home screen provides a quick overview of the BPL tournament.

Planned sections include:

- Tournament overview
- Upcoming matches
- Recent results
- Live match indicator
- Points table preview
- Featured teams
- Latest news
- Tournament highlights
- Sponsors

---

## 🏏 Matches

View tournament matches and their current status.

Features:

- Upcoming matches
- Live matches
- Completed matches
- Match details
- Teams
- Venue
- Date and time
- Match result
- Score summary

---

## 🔴 Live Score

Real-time cricket score experience.

Planned features:

- Live score
- Current innings
- Batting details
- Bowling details
- Current over
- Ball-by-ball commentary
- Match status
- Required run rate
- Partnership information

Real-time updates will be powered by **Socket.IO**.

---

## 🏆 Points Table

View tournament standings.

Information includes:

- Position
- Team
- Matches
- Wins
- Losses
- Ties
- Points
- Net Run Rate

---

## 👕 Teams

Explore all participating BPL teams.

Team information may include:

- Team logo
- Team name
- Team captain
- Squad
- Matches
- Wins
- Losses
- Team statistics

---

## 👤 Players

Explore registered players participating in the tournament.

Player information may include:

- Profile image
- Name
- Team
- Role
- Batting style
- Bowling style
- Player statistics
- Match performance

---

## 🔨 Auction

The BPL auction module provides tournament auction information.

Planned features:

- Auction players
- Base price
- Current bid
- Team bidding
- Auction timer
- Sold / unsold status
- Auction history
- Real-time bidding updates

Auction functionality will use real-time communication where required.

---

## 📝 Player Registration

Players can register for the tournament through the mobile application.

Features may include:

- Player information
- Contact details
- Playing role
- Cricket experience
- Profile image
- Registration status
- Form validation
- Registration confirmation

---

## 🖼️ Gallery

View BPL tournament images.

Features:

- Match photos
- Team photos
- Player photos
- Tournament events
- Image viewer
- Cloud-hosted images

---

## 📰 News

Stay updated with BPL announcements and tournament news.

Features:

- Latest news
- Tournament announcements
- Match updates
- Player updates
- News details

---

## 🏢 Sponsors

Display BPL sponsors and partners.

The sponsor section may include:

- Sponsor logo
- Sponsor name
- Sponsor category
- Website / social links

---

# 🧭 Navigation

The application uses **Expo Router** for navigation.

Main navigation:

```text
Home
├── Matches
├── Points
├── Teams
└── More
```

The **More** section can provide access to:

```text
More
├── Players
├── Auction
├── Registration
├── Gallery
├── News
├── Sponsors
└── About
```

---

# 📁 Project Structure

The project follows a feature-based architecture designed for scalability.

```text
BPL-App/
│
├── app/
│   ├── _layout.tsx
│   ├── index.tsx
│   │
│   ├── (tabs)/
│   │   ├── _layout.tsx
│   │   ├── index.tsx
│   │   ├── matches.tsx
│   │   ├── points.tsx
│   │   ├── teams.tsx
│   │   └── more.tsx
│   │
│   ├── match/
│   ├── team/
│   ├── player/
│   ├── live/
│   ├── auction/
│   ├── registration/
│   ├── gallery/
│   ├── news/
│   └── sponsors/
│
├── src/
│   │
│   ├── features/
│   │   ├── home/
│   │   ├── matches/
│   │   ├── live-score/
│   │   ├── teams/
│   │   ├── players/
│   │   ├── points-table/
│   │   ├── auction/
│   │   ├── registration/
│   │   ├── gallery/
│   │   └── news/
│   │
│   ├── components/
│   │   ├── ui/
│   │   ├── layout/
│   │   └── feedback/
│   │
│   ├── services/
│   │   ├── api/
│   │   ├── storage/
│   │   ├── notifications/
│   │   └── analytics/
│   │
│   ├── store/
│   ├── hooks/
│   ├── theme/
│   ├── config/
│   ├── utils/
│   └── types/
│
├── assets/
│   ├── images/
│   │   ├── logo/
│   │   ├── teams/
│   │   ├── players/
│   │   ├── banners/
│   │   └── gallery/
│   │
│   ├── icons/
│   └── fonts/
│
├── tests/
│   ├── components/
│   ├── features/
│   └── utils/
│
├── scripts/
│
├── .env
├── .env.example
├── app.json
├── eas.json
├── package.json
├── tsconfig.json
├── eslint.config.js
├── prettier.config.js
└── README.md
```

---

# 🏗️ Architecture

The application follows a **feature-based architecture**.

### `app/`

Contains Expo Router routes and navigation.

```text
app/
```

Routes should primarily handle:

- Navigation
- Route parameters
- Screen composition

Business logic should not be placed directly inside route files.

---

### `src/features/`

Contains domain-specific functionality.

For example:

```text
src/features/matches/
```

contains everything related to matches:

```text
components/
hooks/
services/
types/
index.ts
```

This keeps each feature independent and easier to maintain.

---

### `src/components/`

Contains reusable components that are not specific to a single feature.

Examples:

```text
Button
Card
Badge
Input
Modal
Loader
```

---

### `src/services/`

Contains application-wide infrastructure.

```text
services/
├── api/
├── storage/
├── notifications/
└── analytics/
```

---

### `src/store/`

Contains global application state.

Potential stores:

```text
app.store.ts
auth.store.ts
settings.store.ts
```

---

### `src/theme/`

Contains the application's design system.

```text
colors.ts
typography.ts
spacing.ts
radius.ts
shadows.ts
```

---

# 🎨 Design Direction

The BPL App aims for a modern sports application experience.

Design principles:

- Premium
- Modern
- Clean
- Fast
- Mobile-first
- Cricket-focused
- Easy to navigate
- Consistent design system

The interface will use reusable design tokens instead of styling each screen independently.

---

# 🔌 API Architecture

The mobile application will communicate with the BPL backend through APIs.

```text
BPL App
   │
   ▼
BPL API
   │
   ├── Authentication
   ├── Matches
   ├── Teams
   ├── Players
   ├── Points
   ├── Auction
   ├── Registration
   ├── Gallery
   └── News
   │
   ▼
MongoDB
```

The mobile application **will never connect directly to MongoDB**.

All database operations are handled by the backend API.

---

# ⚡ Real-Time Architecture

Real-time functionality will use Socket.IO.

```text
BPL App
   │
   │ Socket Connection
   ▼
BPL API
   │
   ▼
Socket.IO Server
   │
   ├── Live Score
   ├── Commentary
   └── Auction
```

This allows users to receive important tournament updates without manually refreshing the application.

---

# ☁️ Media Storage

Tournament images will be managed through cloud storage.

Potential media categories:

```text
Teams
Players
Gallery
News
Sponsors
Banners
```

Cloudinary will be used for image hosting and media management through the backend.

The mobile application will consume media URLs provided by the API.

---

# 🔐 Environment Variables

Environment-specific configuration should be stored in `.env`.

Example:

```env
EXPO_PUBLIC_API_URL=http://localhost:5000/api
EXPO_PUBLIC_SOCKET_URL=http://localhost:5000
```

Create a local environment file:

```text
.env
```

Use `.env.example` as the template.

### Important

Never commit:

```text
.env
```

or any file containing:

- API secrets
- Private keys
- Authentication secrets
- Production credentials

---

# 💻 Requirements

Before running the project, install:

- Node.js
- npm
- Expo CLI / Expo tooling
- Android Studio
- Android SDK
- Git

For Android development, configure:

- Android SDK
- Android Emulator
- Environment variables
- USB debugging if using a physical device

---

# 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/amolpawar24/BPL-App.git
```

Navigate into the project:

```bash
cd BPL-App
```

Install dependencies:

```bash
npm install
```

Start Expo:

```bash
npx expo start
```

---

# 📱 Run on Android

Start the development server:

```bash
npx expo start
```

Then press:

```text
a
```

or run:

```bash
npx expo start --android
```

---

# 🌐 Run on Physical Android Device

Make sure:

1. The phone and computer are connected to the same network.
2. Developer Options are enabled.
3. USB Debugging is enabled if using USB.
4. The device is recognized by ADB.

Then:

```bash
npx expo start
```

Scan the QR code using the appropriate Expo development workflow.

---

# 🧪 Testing

Run tests with:

```bash
npm test
```

The project will use tests for:

- Components
- Features
- Utility functions
- Business logic

Example structure:

```text
tests/
├── components/
├── features/
└── utils/
```

---

# 🧹 Code Quality

Lint the project:

```bash
npm run lint
```

Format the project:

```bash
npm run format
```

The project should maintain consistent:

- TypeScript
- ESLint
- Prettier
- Naming conventions
- Component structure

---

# 🌿 Git Workflow

The project follows a simple Git workflow.

### Check status

```bash
git status
```

### Add changes

```bash
git add .
```

### Commit

```bash
git commit -m "feat: add match screen"
```

### Push

```bash
git push
```

Recommended commit prefixes:

```text
feat:
fix:
refactor:
style:
docs:
test:
chore:
perf:
```

Examples:

```text
feat: add live score screen
fix: resolve match card layout
refactor: improve API client
style: update team card UI
docs: update README
test: add points table tests
chore: update dependencies
perf: optimize gallery rendering
```

---

# 🌳 Branch Strategy

Recommended branches:

```text
main
│
├── develop
│
├── feature/home-screen
├── feature/live-score
├── feature/auction
├── feature/registration
└── fix/navigation
```

### `main`

Production-ready code.

### `develop`

Integration branch for ongoing development.

### `feature/*`

New features.

### `fix/*`

Bug fixes.

---

# 🔄 Development Workflow

Recommended development process:

```text
Requirement
     ↓
Feature Planning
     ↓
Create Feature Branch
     ↓
Build UI
     ↓
Connect API
     ↓
Add Validation
     ↓
Testing
     ↓
Code Review
     ↓
Merge
     ↓
Production
```

---

# 📦 Build & Deployment

The application will use **Expo Application Services (EAS)** for production builds.

Install EAS CLI:

```bash
npm install -g eas-cli
```

Login:

```bash
eas login
```

Configure the project:

```bash
eas build:configure
```

Android production build:

```bash
eas build --platform android
```

Development build:

```bash
eas build --platform android --profile development
```

Preview build:

```bash
eas build --platform android --profile preview
```

---

# 📊 Application Modules

| Module | Status |
|---|---|
| Home | 🚧 |
| Matches | 🚧 |
| Live Score | 📋 Planned |
| Points Table | 📋 Planned |
| Teams | 📋 Planned |
| Players | 📋 Planned |
| Auction | 📋 Planned |
| Registration | 📋 Planned |
| Gallery | 📋 Planned |
| News | 📋 Planned |
| Sponsors | 📋 Planned |
| Notifications | 📋 Planned |
| Authentication | 📋 Planned |

---

# 🗺️ Development Roadmap

## Phase 1 — Project Foundation

- Expo setup
- TypeScript
- Expo Router
- Folder architecture
- Theme system
- Navigation
- Reusable UI components

## Phase 2 — Core Screens

- Home
- Matches
- Points Table
- Teams
- More

## Phase 3 — Tournament Data

- Players
- Match details
- Team details
- Player details
- API integration

## Phase 4 — Live Features

- Live score
- Commentary
- Current over
- Real-time match updates

## Phase 5 — Auction

- Auction players
- Bidding
- Timer
- Sold / unsold status
- Real-time auction updates

## Phase 6 — Community Features

- Player registration
- Gallery
- News
- Sponsors

## Phase 7 — Production

- Performance optimization
- Error handling
- Offline states
- Notifications
- Analytics
- Testing
- Android production build
- Play Store preparation

---

# 🔒 Security Principles

The mobile application follows these principles:

- Never store database credentials in the app.
- Never expose backend private keys.
- Validate data on both client and server.
- Use secure authentication mechanisms.
- Use HTTPS in production.
- Keep sensitive values out of Git.
- Handle API errors safely.
- Validate user input.
- Keep authorization logic on the backend.

---

# ⚡ Performance Principles

The application will focus on:

- Optimized images
- Lazy loading
- Efficient FlatList usage
- Memoized components where necessary
- Minimal unnecessary re-renders
- API caching where appropriate
- Efficient state management
- Optimized navigation
- Proper loading states
- Offline/error states

---

# 📴 Offline & Error Handling

The application should provide proper states for:

```text
Loading
   ↓
Success
   ↓
Empty
   ↓
Error
   ↓
Offline
```

Reusable components will be used for:

- Loading
- Empty data
- API errors
- Network errors
- Offline mode

---

# 🔔 Notifications

Future notification support may include:

- Match reminders
- Match start notifications
- Live match updates
- Match results
- Auction notifications
- Tournament announcements
- News notifications

---

# 🧩 BPL Ecosystem

The mobile application is part of a larger BPL system.

```text
                    ┌──────────────────┐
                    │   BPL Web App    │
                    └────────┬─────────┘
                             │
                             │
┌──────────────────┐         ▼         ┌──────────────────┐
│   BPL Mobile     │ ───► BPL API ◄─── │   BPL Admin      │
│      App         │         │         │     Panel        │
└──────────────────┘         │         └──────────────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │     MongoDB      │
                    └──────────────────┘
                             │
                             ▼
                    ┌──────────────────┐
                    │    Cloudinary    │
                    └──────────────────┘
```

This architecture allows the web application, mobile application, and admin panel to work with the same backend infrastructure.

---

# 👨‍💻 Development

Developed by **Amol Pawar**.

GitHub:

`https://github.com/amolpawar24`

BPL Web Application:

`https://bpl-official.vercel.app/`

---

# 📄 License

This project is currently intended for the **Bhalawani Premier League** project.

License information will be added when the project's distribution and licensing requirements are finalized.

---

# 🏏 Bhalawani Premier League

**BPL App — Bringing the tournament experience to mobile.**

```text
Built with React Native + Expo
Powered by the BPL ecosystem
```