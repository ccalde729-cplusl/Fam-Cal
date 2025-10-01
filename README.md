# Family Calendar App

A web-first family calendar application focused on helping families organize and coordinate their schedules. Built with React and Supabase, designed for simplicity with powerful family-specific features.

## 🎯 Overview

This family calendar app bridges the gap between generic calendar applications and the specific needs of family coordination. It provides intelligent scheduling, conflict detection, and family-focused features that make organizing multiple family members' schedules effortless.

## ✨ Core Features

### User Management
- **Two-tier system**: Admin (can edit everything) and Users (can edit assigned events)
- **Family structure**: Flat hierarchy with cosmetic labels (son, sister, uncle, etc.)
- **Setup flow**: Admin creates family → invites members → members join with labels

### Calendar Functionality
- **Multi-view support**: Month (primary), Week, Day views
- **Color coding**: Events colored by assigned family members
- **Member assignment**: Checkbox selection during event creation, editable after
- **Member visibility toggles**: Show/hide individual member's events

### Smart Organization
- **Conflict detection**: Same person, overlapping times
- **Location-aware scheduling**: Map integration for route planning between events
- **Weather integration**: 7-day forecasts for outdoor events (extendable with reduced accuracy)

### Communication & Coordination
- **In-app notifications**: Event reminders with optional push notifications
- **Family announcements**: Targeted to event participants only
- **RSVP functionality**: Simple accept/decline for family events

### Timezone Management
- **Default**: System/browser timezone
- **Trip mode**: Location-based timezone handling
  - Manual trip creation with date range + location
  - Auto-detection from flight events using keyword parsing
  - Trip types: Family vs Business with different visibility rules

## 🚀 Premium Features

### School Calendar Wizard
- Interactive wizard for setting school year dates
- Mark teacher planning days, winter/spring breaks
- Auto-generates weekends and holidays
- Stores as separate school calendar entity

### Smart Suggestions (LLM-powered)
- Trip optimization recommendations
- Schedule conflict resolution
- Prep reminders based on event types
- Pattern recognition for recurring events

### Event Checklists
- Assignable checklist items per event
- Member-specific assignments with completion tracking
- Smart alerts based on event timing
- Templates available with custom options
- Shared visibility (others' items greyed out)

### Advanced Trip Management
- Flight email/calendar sync integration
- Auto-trip creation from roundtrip flights
- Bulk timezone conversion for trip periods
- Business vs family trip categorization

## 🛠 Technical Stack

### Frontend
- **React**: Web-first development
- **Responsive design**: Mobile browser compatible for future app port

### Backend
- **Supabase**: Database, authentication, real-time subscriptions, file storage
- **Row Level Security**: Family-based data isolation
- **PDF storage**: For future school calendar upload feature

### Integrations
- **Weather API**: Weather.com for forecast data
- **Mapping service**: Route planning between events
- **LLM integration**: Small model for smart suggestions (premium)

## 📊 Data Structure

### Core Tables
- `families`: Family groups
- `family_members`: Users with roles and labels
- `events`: Calendar events with assignments
- `event_assignments`: Many-to-many event-member relationships

### Premium Tables
- `school_calendars`: Generated school year events
- `trips`: Location-based timezone periods
- `checklist_items`: Event-specific tasks with assignments

## 🗺 Development Roadmap

### Phase 1 (MVP - Free)
1. User management and family setup
2. Basic calendar CRUD with member assignments
3. Simple conflict detection
4. Weather integration
5. Manual school calendar entry

### Phase 2 (Beta)
1. Trip timezone management
2. Enhanced conflict detection with location awareness
3. In-app notification system
4. RSVP functionality

### Phase 3 (Premium Launch)
1. School calendar wizard
2. LLM smart suggestions integration
3. Event checklists with assignments
4. Advanced trip management

### Phase 4 (Post-Launch)
1. PDF school calendar parsing
2. Mobile app development
3. External calendar sync (Google, Apple, Outlook)
4. Advanced analytics and insights

## 💰 Monetization Strategy

### Free Tier
- Basic family calendar
- Manual entry
- Basic notifications
- Simple conflict detection

### Premium Tier
- School calendar wizard
- Smart suggestions (LLM-powered)
- Event checklists with assignments
- Advanced trip management
- Enhanced weather forecasting

**Target Users**: Organized families, business travelers, families with school-age children

## 🎯 Key Differentiators

- **Family-first design** vs generic calendar apps
- **Smart trip management** with auto-detection
- **School calendar wizard** (vs PDF upload requirement)
- **LLM-powered** family scheduling intelligence
- **Simple but powerful** conflict resolution
- **Location-aware** scheduling and routing

## 🚀 Getting Started

### Prerequisites
- Node.js 18+
- Supabase account
- Weather.com API key

### Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/family-calendar-app.git

# Navigate to project directory
cd family-calendar-app

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env.local
# Add your Supabase and Weather API credentials

# Start development server
npm run dev