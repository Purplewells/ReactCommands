# 🚀 React Commands Cheat Sheet

A quick-reference guide for essential commands and concepts when building React apps.

---

## 1. 🛠️ Create a New React App

```bash
npx create-react-app my-app
```
- Scaffolds a new React app using Create React App (CRA).
- Sets up Webpack, Babel, and basic folder structure.

## 2. 🚀 Start the Development Server
```
npm start
```
- Runs the app in development mode.
- Opens at http://localhost:3000
- Hot-reloads the page on file save.

## 3. 🏗️ Build for Production
```
  npm run build
```
- Bundles the app into static files for deployment.
- Output is placed in the build/ directory.
- Minifies and optimises JS/CSS assets.

## 4. 🧪 Run Tests
```
npm test
```
- Runs unit tests using Jest.
- Supports snapshot testing out of the box.
- Runs in watch mode by default.

## 5. 📦 Install a Dependency
```
  npm install react-router-dom
```
- Installs a package (e.g., React Router).
- Use --save-dev for development-only packages.

## 6. 🔄 Update Dependencies
```
npm update
```
Updates all dependencies listed in package.json to the latest compatible versions.

## 7. 🧹 Remove a Dependency
```
npm uninstall <some-package>
```
- Remove a package and clean up package.json and node_modules

## 8. Use Vite for Faster Development ( Modern Alternative to CRA)
```
npm create vite@latest my-app --template react
```
-- Vite offers faster dev startup, instant hot module reload
-- Supports modern tooling and native ES modules

## 9. Bonus 
- Use .env files for environment variables (REACT_APP_ PREFIX REQUIRED)
- Consider TypeScript with React : ``` npx create-react-app my-app --template typescript ```
- Explore component libraries like Material UI or shadcn/ui for faster UI development.

## 10. Typical Structure of React + Vite project
```
my-app/
├── public/                   # Static assets (served directly)
│   └── favicon.svg
│   └── robots.txt
│
├── src/                      # Main source code
│   ├── assets/               # Images, fonts, logos, etc.
│   ├── components/           # Reusable UI components (Button, Modal, etc.)
│   ├── features/             # Feature-based folders (e.g., auth, posts, dashboard)
│   │   └── auth/             # auth-specific components, logic
│   │       ├── AuthPage.jsx
│   │       ├── authSlice.js  # (if using Redux or similar)
│   ├── hooks/                # Custom hooks (useAuth, useDebounce, etc.)
│   ├── pages/                # Route-level components (Home, About, Dashboard)
│   ├── routes/               # All route definitions (React Router config)
│   ├── services/             # API calls, external services
│   ├── store/                # State management (Redux, Zustand, etc.)
│   ├── styles/               # Global styles, Tailwind config, SCSS, etc.
│   ├── utils/                # Helper functions and utilities
│   ├── App.jsx               # Root component
│   ├── main.jsx              # Entry point for ReactDOM.createRoot
│
├── .env                      # Environment variables
├── index.html                # Vite entry point HTML
├── package.json              # Project metadata and scripts
├── vite.config.js            # Vite configuration file
├── tailwind.config.js        # Tailwind CSS configuration (if using)
└── README.md

```
### A few best practices 
Group by feature inside src/features for cleaner separation as the app grows

Keep src/components for reusable parts ( buttons, modals, inputs, etc.)

Prefer colocating files like ```Component.jsx + Component.modules.css``` if styles are component specific

Split route-level pages from nested components (helps with routing and lazy loading).

### Basic structure for a beginner friendly project structure
```
my-react-app/
├── public/                  # Static files (images, favicon, etc.)
│   └── favicon.svg
│
├── src/                     # Source code
│   ├── components/          # Reusable components (e.g., Header, Button)
│   │   └── Header.jsx
│   │
│   ├── pages/               # Full-page views (e.g., Home, About)
│   │   └── Home.jsx
│   │
│   ├── App.jsx              # Root component (layout, routes)
│   ├── main.jsx             # Entry point (ReactDOM)
│   └── index.css            # Global styles
│
├── .gitignore
├── index.html               # Vite HTML entry point
├── package.json             # Project metadata and scripts
├── vite.config.js           # Vite configuration
└── README.md
```

#### ✅ Beginner Tips:

- Only keep components/ and pages/ in the beginning.
- Create one component per file: Header.jsx, Button.jsx, etc.
- Keep routing inside App.jsx if using react-router-dom.
- Avoid state management libraries early on; use useState and useEffect.

#### Next Step Actions
Create a sample project 
- Understand the flow of the React application lifecycle ( How the various components and pages are called, and the order and dependencies )
- Learn about components ( functional & class-based)
    - Prop
    - State
    - Events Handling
    - Hooks
 
Links
[Create Project Structure](https://github.com/Purplewells/ReactCommands/wiki/Create-Project-Structure#react--vite-beginner-project-structure)
