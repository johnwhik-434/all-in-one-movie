# 🎬 VegaMovies - 3D Movie Streaming Platform

A stunning, modern movie streaming/download website with **3D animations**, **admin panel**, and **complete movie management system**.

![VegaMovies](https://img.shields.io/badge/VegaMovies-v1.0-purple?style=for-the-badge)
![React](https://img.shields.io/badge/React-18-61dafb?style=for-the-badge&logo=react)
![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=for-the-badge&logo=typescript)
![Tailwind CSS](https://img.shields.io/badge/Tailwind-3-38bdf8?style=for-the-badge&logo=tailwind-css)

## ✨ Features

### 🎨 User Interface
- ✅ **3D Card Effects** - Interactive hover animations with depth
- ✅ **Glass Morphism** - Modern frosted glass UI elements
- ✅ **Smooth Animations** - Fade, slide, scale, and glow effects
- ✅ **Responsive Design** - Perfect on mobile, tablet, and desktop
- ✅ **Animated Particles** - Floating background particles for depth
- ✅ **Auto-Sliding Hero** - Featured movies carousel
- ✅ **Trending Section** - Horizontal scrollable movie showcase
- ✅ **Search Functionality** - Real-time movie search with trending suggestions
- ✅ **Category Filters** - Browse by Bollywood, Hollywood, South Indian, Web Series
- ✅ **Custom Scrollbar** - Gradient purple-pink design

### 🔐 Admin Panel (ENHANCED SECURITY)
- ✅ **Advanced Login System** - Multi-layer authentication
- ✅ **Password Encryption** - Base64 encrypted passwords
- ✅ **Security Question** - Additional verification layer
- ✅ **Login Attempt Limiting** - Max 3 attempts before lockout
- ✅ **Account Lockout** - 5-minute lockout after failed attempts
- ✅ **Session Timeout** - 30-minute auto-logout
- ✅ **Real-time Countdown** - Live lockout timer
- ✅ **Add Movies** - Complete form with validation
- ✅ **Delete Movies** - Two-step confirmation
- ✅ **Success Notifications** - Animated feedback
- ✅ **Real-time Stats** - Dashboard with category breakdown
- ✅ **Data Persistence** - LocalStorage with encryption
- ✅ **Beautiful Dashboard** - Modern animated interface
- ✅ **Movie List Table** - View and manage all movies

### 📊 Statistics
- ✅ **Animated Counters** - Smooth counting animations
- ✅ **Total Movies Count**
- ✅ **Category Breakdown**
- ✅ **User Statistics**
- ✅ **Download Metrics**

## 🚀 Quick Start

### Installation
```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build
```

### Access the Application
- **Homepage:** `http://localhost:5173/`
- **Admin Panel:** `http://localhost:5173/admin`

## 🔑 Admin Credentials

**Username:** `admin`  
**Password:** `admin123`  
**Security Answer:** `inception` (for security question: "What is your favorite movie?")

> **Note:** These are demo credentials. For production, implement proper authentication.

## 📱 Pages & Routes

### Public Pages
- **/** - Homepage with all movies
- **#movies** - Movies section
- **#trending** - Trending movies
- **#series** - Web series section

### Admin Pages
- **/admin** - Admin login page
- **/admin** (after login) - Admin dashboard

## 🎯 How to Use Admin Panel

### Step 1: Access Admin
Click the **floating admin button** (bottom-right) or navigate to `/admin`

### Step 2: Login
Use the default credentials:
- Username: `admin`
- Password: `admin123`
- Security Answer: `inception`

**Security Features:**
- Maximum 3 login attempts
- 5-minute lockout after failures
- 30-minute session timeout
- Password encryption
- Real-time attempt counter

### Step 3: Manage Movies

#### Add New Movie
1. Click "Add New Movie" button
2. Fill in the form:
   - **Title** (required)
   - **Year** (required)
   - **Rating** (required, e.g., 8.5)
   - **Quality** (4K, 1080p, 720p, 480p)
   - **Category** (Bollywood, Hollywood, South Indian, Web Series)
   - **Genre** (Action, Comedy, Thriller, Drama, etc.)
   - **Image URL** (required, poster image link)
   - **Description** (optional)
3. Click "Add Movie"

#### Delete Movie
1. Find the movie in the list
2. Click "Delete" button
3. Confirm deletion

## 🏗️ Tech Stack

- **Frontend Framework:** React 18 with TypeScript
- **Styling:** Tailwind CSS
- **Build Tool:** Vite
- **State Management:** React Context API
- **Data Storage:** LocalStorage
- **Animations:** Custom CSS animations + Tailwind

## 📂 Project Structure

```
src/
├── components/          # Reusable UI components
│   ├── Navbar.tsx
│   ├── Hero.tsx
│   ├── MovieCard.tsx
│   ├── MovieGrid.tsx
│   ├── Categories.tsx
│   ├── SearchBar.tsx
│   ├── Stats.tsx
│   ├── Trending.tsx
│   ├── Footer.tsx
│   └── AdminFloatingButton.tsx
├── pages/              # Page components
│   ├── AdminLogin.tsx
│   └── AdminDashboard.tsx
├── context/            # React Context providers
│   ├── MovieContext.tsx
│   └── AuthContext.tsx
├── App.tsx             # Main app component
├── App.css             # Custom animations
└── main.tsx            # Entry point
```

## 🎨 Color Scheme

- **Primary:** Purple (#9333ea)
- **Secondary:** Pink (#ec4899)
- **Background:** Dark gradient (Gray-900 → Purple-900 → Black)
- **Text:** White with various opacities
- **Accents:** Glass morphism effects

## 🔄 Data Flow

1. **MovieContext** manages all movie data
2. Data is stored in **localStorage** for persistence
3. **AuthContext** handles admin authentication
4. Components consume contexts using hooks

## 🌟 Key Features Explained

### 3D Card Effect
```css
.card-3d:hover {
  transform: rotateY(5deg) rotateX(5deg) translateZ(10px);
}
```

### Glass Morphism
```css
.glass {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}
```

### Animated Particles
Floating particles in the background using React-generated elements with random positions and animations.

## 📝 API Structure

### MovieContext
```typescript
{
  movies: Movie[],
  addMovie: (movie) => void,
  deleteMovie: (id) => void,
  updateMovie: (id, data) => void
}
```

### AuthContext
```typescript
{
  isAuthenticated: boolean,
  login: (username, password) => boolean,
  logout: () => void
}
```

## 🔒 Security Considerations

⚠️ **Important for Production:**
- Implement backend authentication
- Use environment variables for credentials
- Add JWT/session management
- Implement rate limiting
- Add CSRF protection
- Use HTTPS only

## 🎯 Future Enhancements

- [ ] User registration and authentication
- [ ] Video player integration
- [ ] Comments and ratings system
- [ ] Watchlist/favorites
- [ ] Multiple admin roles
- [ ] Movie recommendations
- [ ] Advanced search filters
- [ ] Database integration (Firebase/MongoDB)

## 📸 Screenshots

### Homepage
- Modern hero section with auto-sliding carousel
- Animated statistics counters
- Trending movies showcase
- Category-based filtering
- Search functionality

### Admin Panel
- Secure login page
- Dashboard with statistics
- Add movie form
- Movies management table

## 🤝 Contributing

This is a demo project. Feel free to fork and customize as needed!

## 📄 License

This project is created for educational purposes.

## 👨‍💻 Author

**VegaMovies Team**

## 🙏 Acknowledgments

- Unsplash for placeholder images
- Tailwind CSS for styling utilities
- React team for the amazing framework

---

**Built with ❤️ using React, TypeScript, and Tailwind CSS**

🎬 **VegaMovies** - Your Ultimate Movie Destination
