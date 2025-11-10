# MindTrack Frontend

A modern, responsive React application for personal wellness and habit tracking. Built with React 18, Tailwind CSS, and Chart.js for comprehensive health and habit management.

## 📋 Table of Contents

- [Features](#features)
- [Tech Stack](#tech-stack)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Project Structure](#project-structure)
- [Available Scripts](#available-scripts)
- [Pages & Routes](#pages--routes)
- [Components](#components)
- [State Management](#state-management)
- [Styling](#styling)
- [Building for Production](#building-for-production)

## ✨ Features

- **User Authentication**: Secure login and registration
- **Dashboard**: Overview of habits, moods, and goals
- **Habit Tracking**: Create, edit, and track daily habits with progress visualization
- **Mood Tracking**: Record daily moods with calendar view and analytics
- **Goal Management**: Set and monitor personal goals with progress tracking
- **Analytics**: Comprehensive charts and insights for habits, moods, and goals
- **Social Features**: Share progress and view leaderboards
- **AI Assistant**: AI-powered insights and recommendations
- **Responsive Design**: Mobile-friendly interface with Tailwind CSS
- **Real-time Updates**: React Query for efficient data fetching and caching

## 🛠 Tech Stack

- **Framework**: React 18.2.0
- **Routing**: React Router DOM 6.8.1
- **State Management**: React Context API, React Query
- **Styling**: Tailwind CSS 3.3.6
- **Forms**: React Hook Form 7.48.2
- **HTTP Client**: Axios 1.6.2
- **Charts**: Chart.js 4.4.0 with react-chartjs-2
- **Date Handling**: date-fns 2.30.0
- **Icons**: Lucide React 0.294.0
- **Notifications**: React Hot Toast 2.4.1
- **Calendar**: React Calendar 4.6.0
- **Build Tool**: Create React App (react-scripts 5.0.1)

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v14 or higher)
- **npm** (v6 or higher) or **yarn**
- **Git**
- **Backend API** running (see backend README)

## 🚀 Installation

1. **Navigate to the frontend directory**:
   ```bash
   cd frontend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Configure the API endpoint** (if needed):
   - The default proxy is set to `http://localhost:5000` in `package.json`
   - Update the `proxy` field if your backend runs on a different port

## ⚙️ Configuration

The frontend is configured to connect to the backend API. The proxy is set in `package.json`:

```json
"proxy": "http://localhost:5000"
```

If your backend runs on a different port or URL, update this value accordingly.

For production builds, you may need to configure the API base URL in `src/services/api.js`.

## 🏃 Running the Application

### Development Mode

Start the development server:

```bash
npm start
```

The application will open in your browser at `http://localhost:3000`.

The page will automatically reload when you make changes to the code.

### Running Tests

Run the test suite:

```bash
npm test
```

### Building for Production

Create an optimized production build:

```bash
npm run build
```

This creates a `build` folder with optimized production files.

## 📁 Project Structure

```
frontend/
├── public/
│   ├── index.html          # HTML template
│   ├── favicon.ico         # App icon
│   └── manifest.json       # PWA manifest
├── src/
│   ├── components/         # Reusable React components
│   │   ├── AIAssistant.js
│   │   ├── AnalyticsChart.js
│   │   ├── CreateHabitModal.js
│   │   ├── EditHabitModal.js
│   │   ├── GoalAnalytics.js
│   │   ├── GoalCard.js
│   │   ├── GoalModal.js
│   │   ├── GoalProgress.js
│   │   ├── HabitAnalytics.js
│   │   ├── HabitCard.js
│   │   ├── Header.js
│   │   ├── InsightsCard.js
│   │   ├── Layout.js
│   │   ├── LeaderboardCard.js
│   │   ├── LoadingSpinner.js
│   │   ├── MobileMenu.js
│   │   ├── MoodAnalytics.js
│   │   ├── MoodCalendar.js
│   │   ├── MoodEntry.js
│   │   ├── MoodEntryModal.js
│   │   ├── MoodTracker.js
│   │   ├── MotivationalMessage.js
│   │   ├── QuickStats.js
│   │   ├── ShareProgressModal.js
│   │   ├── Sidebar.js
│   │   ├── TrendAnalysis.js
│   │   ├── UpdateProgressModal.js
│   │   └── WeeklyChart.js
│   ├── contexts/
│   │   └── AuthContext.js  # Authentication context
│   ├── hooks/
│   │   └── useAuth.js      # Custom authentication hook
│   ├── pages/              # Page components
│   │   ├── Analytics.js
│   │   ├── Dashboard.js
│   │   ├── Goals.js
│   │   ├── Habits.js
│   │   ├── Login.js
│   │   ├── Moods.js
│   │   ├── Profile.js
│   │   ├── Register.js
│   │   └── Social.js
│   ├── services/
│   │   ├── api.js          # API service layer
│   │   └── dataService.js  # Data management service
│   ├── utils/
│   │   └── dataConsistencyTest.js
│   ├── App.js              # Main App component
│   ├── index.js            # Entry point
│   └── index.css           # Global styles
├── build/                  # Production build (generated)
├── package.json            # Dependencies and scripts
├── tailwind.config.js      # Tailwind CSS configuration
└── README.md               # This file
```

## 📜 Available Scripts

- `npm start` - Start the development server
- `npm run build` - Build the app for production
- `npm test` - Run the test suite
- `npm run eject` - Eject from Create React App (irreversible)

## 🗺️ Pages & Routes

### Public Routes
- `/login` - User login page
- `/register` - User registration page

### Protected Routes (require authentication)
- `/dashboard` - Main dashboard with overview
- `/habits` - Habit tracking and management
- `/moods` - Mood tracking with calendar view
- `/goals` - Goal setting and progress tracking
- `/analytics` - Comprehensive analytics and insights
- `/social` - Social features and leaderboard
- `/profile` - User profile management

## 🧩 Components

### Layout Components
- **Layout**: Main application layout with sidebar and header
- **Header**: Top navigation bar
- **Sidebar**: Side navigation menu
- **MobileMenu**: Mobile-responsive navigation menu

### Habit Components
- **HabitCard**: Display individual habit with progress
- **CreateHabitModal**: Modal for creating new habits
- **EditHabitModal**: Modal for editing existing habits
- **UpdateProgressModal**: Modal for updating habit progress
- **HabitAnalytics**: Analytics visualization for habits

### Mood Components
- **MoodTracker**: Main mood tracking interface
- **MoodEntry**: Individual mood entry display
- **MoodEntryModal**: Modal for creating/editing mood entries
- **MoodCalendar**: Calendar view for mood history
- **MoodAnalytics**: Analytics visualization for moods

### Goal Components
- **GoalCard**: Display individual goal with progress
- **GoalModal**: Modal for creating/editing goals
- **GoalProgress**: Progress visualization for goals
- **GoalAnalytics**: Analytics visualization for goals

### Analytics Components
- **AnalyticsChart**: Reusable chart component
- **WeeklyChart**: Weekly data visualization
- **TrendAnalysis**: Trend analysis visualization
- **QuickStats**: Quick statistics display
- **InsightsCard**: Display insights and recommendations

### Social Components
- **LeaderboardCard**: Leaderboard display
- **ShareProgressModal**: Modal for sharing progress

### Utility Components
- **LoadingSpinner**: Loading indicator
- **AIAssistant**: AI-powered assistant component
- **MotivationalMessage**: Motivational messages display

## 🔄 State Management

### Authentication Context
- **AuthContext**: Provides authentication state and methods
- **useAuth Hook**: Custom hook for accessing auth context
- Stores user information and authentication status

### Data Fetching
- **React Query**: Used for efficient data fetching, caching, and synchronization
- Automatic background refetching
- Optimistic updates support

### Local State
- React hooks (`useState`, `useEffect`) for component-level state
- React Hook Form for form state management

## 🎨 Styling

### Tailwind CSS
The project uses Tailwind CSS for styling:
- Utility-first CSS framework
- Responsive design utilities
- Custom configuration in `tailwind.config.js`
- PostCSS and Autoprefixer for processing

### Global Styles
- Custom styles in `src/index.css`
- Tailwind directives included
- Global resets and base styles

## 🏗️ Building for Production

1. **Create production build**:
   ```bash
   npm run build
   ```

2. **The build folder contains**:
   - Optimized and minified JavaScript
   - Optimized CSS
   - Static assets
   - Production-ready HTML

3. **Deploy the build folder** to your hosting service:
   - Netlify
   - Vercel
   - AWS S3 + CloudFront
   - Any static hosting service

## 🔌 API Integration

The frontend communicates with the backend API through:
- **API Service** (`src/services/api.js`): Axios instance with interceptors
- **Data Service** (`src/services/dataService.js`): Higher-level data operations
- All API calls are authenticated using JWT tokens stored in localStorage

## 🐛 Troubleshooting

### Port Already in Use
If port 3000 is already in use, the app will prompt you to use a different port.

### API Connection Issues
- Verify the backend server is running
- Check the proxy configuration in `package.json`
- Verify CORS settings on the backend

### Build Errors
- Clear `node_modules` and reinstall: `rm -rf node_modules && npm install`
- Clear npm cache: `npm cache clean --force`
- Delete `build` folder and rebuild

### Styling Issues
- Ensure Tailwind CSS is properly configured
- Check `tailwind.config.js` for correct content paths
- Verify PostCSS configuration

## 📱 Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## 🔒 Security Notes

- JWT tokens are stored in localStorage
- API requests include authentication headers
- Protected routes require authentication
- Input validation on forms

## 📝 Development Tips

- Use React DevTools for debugging
- Check browser console for API errors
- Use Network tab to monitor API calls
- Hot reload is enabled in development mode

## 🤝 Contributing

1. Create a feature branch
2. Make your changes
3. Test thoroughly
4. Submit a pull request

## 📄 License

This project is part of the MindTrack application.

