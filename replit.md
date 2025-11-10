# Recovery Journey - Addiction Recovery Support App

## Overview
A compassionate, privacy-focused web application designed to support individuals recovering from pornography addiction. The app provides tracking tools, educational resources, and motivational support in a calm, non-judgmental environment.

## Purpose
- Help users track their recovery progress with a visual streak counter
- Provide immediate support through a panic button with calming activities
- Enable private journaling for reflection and emotional processing
- Track recovery benefits to maintain motivation
- Offer educational resources about addiction and recovery
- Celebrate milestones to reinforce positive behavior

## Project Architecture

### Tech Stack
- **Frontend**: React + TypeScript with Vite
- **Backend**: Express.js with TypeScript
- **Styling**: Tailwind CSS + Shadcn UI components
- **Data Storage**: In-memory storage with localStorage persistence (privacy-focused)
- **Routing**: Wouter (lightweight React router)
- **State Management**: TanStack Query (React Query v5)
- **Forms**: React Hook Form with Zod validation

### Key Design Principles
1. **Privacy First**: All data stored locally on user's device, no cloud sync or tracking
2. **Calm & Supportive**: Soft color palette (blues/neutrals), generous whitespace, minimal animations
3. **Instant Access**: Critical features (panic button, urge logging) prominently placed
4. **Progress-Focused**: Visual feedback on recovery journey through streak counter and milestones

### Project Structure
```
client/
├── src/
│   ├── components/
│   │   ├── ui/              # Shadcn UI components (pre-configured)
│   │   ├── theme-provider.tsx
│   │   ├── theme-toggle.tsx
│   │   ├── bottom-nav.tsx
│   │   ├── panic-button-modal.tsx
│   │   └── milestone-celebration.tsx
│   ├── pages/
│   │   ├── dashboard.tsx    # Home page with streak counter
│   │   ├── journal.tsx      # Private journaling
│   │   ├── resources.tsx    # Education & benefits tracker
│   │   ├── profile.tsx      # Stats & settings
│   │   └── not-found.tsx
│   ├── lib/
│   │   ├── queryClient.ts
│   │   └── utils.ts
│   ├── App.tsx
│   ├── index.css
│   └── main.tsx
server/
├── routes.ts               # API endpoints
└── storage.ts             # In-memory storage with CRUD operations
shared/
└── schema.ts              # Shared TypeScript types and Zod schemas
```

## Current State

### Completed (Task 1 - Schema & Frontend)
- ✅ Complete data model with TypeScript types for all features
- ✅ All page components with exceptional visual design
- ✅ Dark mode support with theme toggle
- ✅ Bottom navigation for mobile-first experience
- ✅ Panic button modal with breathing exercises and resources
- ✅ Milestone celebration with confetti animation
- ✅ SEO meta tags and proper HTML structure
- ✅ Beautiful loading states and empty states throughout

### In Progress (Task 2 - Backend)
- Implementing storage interface for all recovery data
- Creating API endpoints for CRUD operations
- Setting up data validation with Zod

### Pending (Task 3 - Integration)
- Connect frontend to backend APIs
- Implement localStorage persistence
- Add comprehensive error handling
- Test all user journeys

## Key Features

### 1. Dashboard (Home)
- **Streak Counter**: Large, motivating display of current recovery days
- **Panic Button**: Prominent red button for immediate support
  - Breathing exercises (4-7-8 technique)
  - Quick meditation
  - Distraction games
  - Calming music suggestions
  - Support hotline numbers
- **Urge Logging**: Quick button to track urges with timestamps
- **Progress to Next Milestone**: Visual progress bar
- **Daily Motivational Quote**: Rotating inspirational messages
- **Today's Stats**: Quick view of daily progress

### 2. Journal
- **Private Writing Space**: Full-screen textarea for reflection
- **Auto-save**: Drafts saved to localStorage
- **Entry History**: View past entries organized by date
- **Privacy Notice**: Clear indication of local-only storage

### 3. Resources
- **Benefits Tracker**: Checkbox list of recovery benefits
  - Improved focus
  - Better self-esteem
  - Increased energy
  - Stronger relationships
  - Progress percentage visualization
- **Educational Content**: Expandable sections
  - Understanding Addiction
  - The Recovery Process
  - Benefits of Recovery
- **Support Resources**: Helpline numbers and online resources

### 4. Profile
- **Recovery Statistics**:
  - Current streak
  - Longest streak
  - Journey start date
  - Current goal
- **Achievements Display**: Earned milestone badges
- **Privacy Information**: Clear data privacy statements
- **Danger Zone**: Streak reset option with confirmation

## User Preferences

### Design System
- **Color Scheme**: Calming blue primary (hsl(210 65% 42%)) with neutral grays
- **Typography**: Inter font family for clean, modern readability
- **Spacing**: Consistent padding (p-4 to p-6) with generous whitespace
- **Components**: Using Shadcn UI for consistency and accessibility
- **Interactions**: Subtle hover elevations, minimal animations (except milestone celebrations)

### Dark Mode
- Fully implemented with theme toggle in profile
- Uses class-based dark mode switching
- All colors have proper dark mode variants
- Persistent theme preference in localStorage

## Data Model

### Core Entities
1. **RecoveryGoal**: User's target days for recovery
2. **StreakData**: Current and longest streak tracking
3. **UrgeLog**: Timestamped urge records with notes
4. **Benefit**: Recovery benefits checklist items
5. **JournalEntry**: Private journal entries
6. **Milestone**: Achievement system (1 day, 1 week, 1 month, etc.)

## Privacy & Security
- **Local-Only Storage**: All data stored in browser localStorage
- **No Analytics**: No tracking or data collection
- **No Cloud Sync**: Data never leaves user's device
- **Clear Communication**: Privacy notices throughout app
- **User Control**: Easy data clearing through browser settings

## Development Workflow
1. Run `npm run dev` to start both frontend (Vite) and backend (Express)
2. Frontend available at http://localhost:5000
3. Backend API endpoints at http://localhost:5000/api/*
4. Hot reload enabled for rapid development

## Future Enhancements (Next Phase)
- Web content filtering integration
- Urge pattern analytics dashboard
- Customizable panic button resources
- Export functionality for journal/progress data
- Optional accountability partner feature
- Advanced statistics and insights

## Notes
- Mobile-first design approach
- All components use data-testid attributes for e2e testing
- Following Apple HIG-inspired minimalism for calm UX
- Motivational quotes rotate daily based on day of week
