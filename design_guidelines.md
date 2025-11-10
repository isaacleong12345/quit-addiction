# Design Guidelines: Addiction Recovery Support App

## Design Approach
**System Selected**: Apple Human Interface Guidelines (HIG)
**Rationale**: Content-focused minimalism creates the calm, supportive environment essential for recovery. Clean hierarchy and accessibility features ensure quick access to critical tools like the panic button during moments of stress.

## Core Design Principles
1. **Calm & Supportive**: Reduce visual noise to create a peaceful environment
2. **Instant Access**: Critical features (panic button, urge logging) prominently placed
3. **Privacy-First**: Visual cues that reinforce data security
4. **Progress-Focused**: Clear visual feedback on recovery journey

## Typography
- **Primary Font**: Inter or SF Pro (Google Fonts CDN)
- **Display**: 32px/36px, semi-bold for streak counter
- **Headings**: 24px, medium weight
- **Body**: 16px, regular weight
- **Captions**: 14px for timestamps, metadata

## Layout System
**Spacing Units**: Tailwind units of 3, 4, 6, 8, 12, 16
- Component padding: p-4 to p-6
- Section spacing: py-8 to py-12
- Card gaps: gap-4
- Generous whitespace between major sections

## Component Library

### Navigation
- Bottom tab bar (mobile-first): Home, Journal, Resources, Profile
- Clean icons with labels
- Active state with subtle indicator

### Dashboard (Home)
**Hero Section**: Streak counter as centerpiece
- Large numerical display (days count)
- Subtle circular progress indicator
- Encouraging subtitle ("You're doing great!")

**Critical Actions Row**:
- Panic Button: Full-width, prominent placement below streak
- Urge Log Button: Secondary prominence, quick-tap positioned

### Cards & Containers
- Rounded corners (rounded-xl)
- Subtle shadows (shadow-sm)
- Benefits tracker: Checkbox list with completion states
- Milestones: Badge grid with unlock states (locked/unlocked visual distinction)

### Forms & Input
- Journal: Full-screen textarea with auto-save indicator
- Goal setting: Simple number input with increment/decrement controls
- All inputs: Clear focus states, adequate touch targets (min 44px)

### Modals & Overlays
- Panic button activation: Full-screen takeover with calming activity
- Milestone celebrations: Center modal with confetti animation (brief, 2s)
- Educational content: Slide-up panel with close action

### Status Indicators
- Streak progress: Linear bar showing progress to next milestone
- Urge patterns: Simple bar chart visualization
- Benefits checklist: Checkmark icons with completion percentage

## Animation Strategy
**Minimal & Purposeful**:
- Milestone celebrations only: Brief confetti (2 seconds)
- Smooth transitions for modal entry/exit (300ms ease)
- No scroll animations, hover effects, or decorative motion
- Focus on instant responsiveness over visual flair

## Images
**No hero image required** - this is a utility-focused app. 

**Icon System**: 
- Use Heroicons (outline style) via CDN
- Consistent 24px size throughout
- Icons for: panic button (shield), urge log (chart), journal (book), milestones (trophy), resources (lightbulb)

## Accessibility
- High contrast ratios (WCAG AAA where possible)
- Large touch targets for panic button (min 60px height)
- Clear focus indicators on all interactive elements
- Screen reader labels for all icons and actions
- Consistent tab order prioritizing critical functions

## Privacy Visual Cues
- Lock icon in footer with "Your data stays private" text
- Local storage indicator (no cloud sync symbol)
- Simple privacy statement in onboarding/settings

## Responsive Behavior
- Mobile-first design (primary use case)
- Single column layouts throughout
- Full-width components on mobile
- Maximum width constraint (max-w-2xl) on tablet/desktop for focused experience