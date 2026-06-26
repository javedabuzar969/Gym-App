# 🏋️ GymPro — Professional Gym Management System

<div align="center">

[![React](https://img.shields.io/badge/React-18.2-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://reactjs.org/)
[![Vite](https://img.shields.io/badge/Vite-5.1-646CFF?style=for-the-badge&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4-38B2AC?style=for-the-badge&logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Supabase](https://img.shields.io/badge/Supabase-PostgreSQL-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)](https://supabase.com/)
[![Capacitor](https://img.shields.io/badge/Capacitor-Android-119EFF?style=for-the-badge&logo=capacitor&logoColor=white)](https://capacitorjs.com/)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)

**GymPro** is a comprehensive, all-in-one management solution for modern fitness centers.  
From member registration to financial reporting, attendance tracking to supplement inventory —  
manage your **entire gym** from a single, beautiful dashboard.

[🚀 Live Demo](#) · [📖 Docs](#getting-started) · [🐛 Report Bug](https://github.com/javedabuzar969/Gym-App/issues) · [💡 Request Feature](https://github.com/javedabuzar969/Gym-App/issues)

</div>

---

## 📸 Screenshots

> _Dashboard · Members · Attendance · Financial Reports_

_(Screenshots coming soon — stay tuned!)_

---

## ✨ Features

### 👥 Member Management
- 🖼️ **Digital Profiles** — Full member records with photo, contact info & status tracking
- 📲 **QR Code IDs** — Auto-generated QR codes for every member for fast check-ins
- 🔄 **Subscription Tracking** — Monitor Active / Inactive / Expired status at a glance
- 🔍 **Smart Search & Filters** — Find any member instantly by name, ID or status

### 🧾 Financial Operations
- 🧾 **Smart Billing** — Generate professional PDF invoices with a single click
- 💳 **Payment Tracking** — Handle full & partial payments, track revenue and expenses
- 📈 **Financial Reports** — Visual charts for income trends, sales data & monthly comparisons

### 📊 Attendance & Scheduling
- 📷 **QR Scanner** — Browser-based QR attendance tracking (no extra hardware needed)
- 🗓️ **Class Schedules** — Timetables with instructor assignment and capacity management
- 📋 **Real-time Logs** — Full attendance history, streaks, and trend monitoring

### 💊 Advanced Modules
- 🛒 **Supplements Store** — Inventory management with low-stock alerts and sales tracking
- 🏃 **Training Plans** — PT (Personal Training) and Cardio package management
- 📊 **Dashboard Analytics** — Interactive charts for a full business health overview
- 📴 **Offline Support** — IndexedDB (Dexie) powered offline-first data layer
- 📱 **PWA & Android** — Installable as a Progressive Web App and deployable to Android via Capacitor

---

## 🛠️ Tech Stack

| Layer | Technology | Purpose |
|---|---|---|
| **Frontend** | [React 18](https://reactjs.org/) + Context API | UI & State Management |
| **Styling** | [Tailwind CSS 3](https://tailwindcss.com/) | Utility-first CSS Framework |
| **Build Tool** | [Vite 5](https://vitejs.dev/) + PWA Plugin | Fast Dev Server & Bundler |
| **Backend / DB** | [Supabase](https://supabase.com/) (PostgreSQL + Auth + RLS) | Cloud Database & Auth |
| **Offline DB** | [Dexie](https://dexie.org/) (IndexedDB wrapper) | Offline-first Storage |
| **Mobile** | [Capacitor 8](https://capacitorjs.com/) (Android) | Native Android Wrapper |
| **Charts** | [Recharts](https://recharts.org/) | Data Visualization |
| **PDF Generation** | `jspdf` + `html2canvas` | Invoice Generation |
| **QR Code** | `qrcode.react` + `html5-qrcode` | QR Generate & Scan |
| **Icons** | [Lucide React](https://lucide.dev/) | Icon Library |
| **Routing** | [React Router DOM v7](https://reactrouter.com/) | Client-side Routing |

---

## 🚀 Getting Started

### Prerequisites

Before you begin, make sure you have the following installed:

- ✅ **Node.js 18+** and npm — [Download here](https://nodejs.org/)
- ✅ A free **[Supabase](https://supabase.com/)** account
- ✅ **Git** — [Download here](https://git-scm.com/)

---

### Step 1 — Clone & Install

```bash
git clone https://github.com/javedabuzar969/Gym-App.git
cd Gym-App
npm install
```

---

### Step 2 — Configure Environment Variables

Create a `.env` file in the project root:

```env
VITE_SUPABASE_URL=your_supabase_project_url
VITE_SUPABASE_ANON_KEY=your_supabase_anon_key
```

> 💡 **Tip:** Find these values in your Supabase Dashboard under **Project Settings → API**.

---

### Step 3 — Set Up the Database

1. Log in to your [Supabase Dashboard](https://supabase.com/dashboard)
2. Navigate to the **SQL Editor**
3. Run the script in `COMPLETE-GYM-DATABASE.sql` to create all tables, RLS policies, and seed data

📖 For detailed instructions, see the [SUPABASE-SETUP-GUIDE.md](./SUPABASE-SETUP-GUIDE.md).

---

### Step 4 — Run Locally

```bash
npm run dev
```

Open **[http://localhost:5173](http://localhost:5173)** in your browser. 🎉

---

## 📂 Project Structure

```
Gym-App/
├── public/                    # Static public assets
├── src/
│   ├── assets/                # Images, logos, icons
│   ├── components/            # Reusable UI (Sidebar, Layout, Cards, Modals)
│   ├── context/               # Global state (Context API providers)
│   ├── pages/                 # App views (Dashboard, Members, Reports, etc.)
│   └── supabaseClient.js      # Supabase connection config
├── android/                   # Capacitor Android project
├── .env                       # 🔑 Environment variables (not committed)
├── capacitor.config.json      # Capacitor mobile configuration
├── tailwind.config.js         # Tailwind CSS configuration
├── vite.config.js             # Vite build configuration
├── vercel.json                # Vercel deployment config
├── SUPABASE-SETUP-GUIDE.md    # Detailed database setup guide
├── COMPLETE-GYM-DATABASE.sql  # Full DB schema + seed data
└── package.json
```

---

## 📱 Android / Mobile Build

This app supports Android via **Capacitor**:

```bash
# 1. Build the web app
npm run build

# 2. Sync with Android project
npx cap sync android

# 3. Open in Android Studio
npx cap open android
```

> 📌 Make sure **Android Studio** and **Java JDK 17+** are installed before running the above commands.

---

## 🌐 Deployment (Vercel)

The project includes a `vercel.json` for one-command deployment:

```bash
# Install Vercel CLI (once)
npm install -g vercel

# Deploy to production
vercel --prod
```

> 🔗 Your app will be live at `https://your-project-name.vercel.app`

---

## 🔒 Security Notes

Your `.gitignore` protects sensitive files:

```gitignore
.env
node_modules/
dist/
android/
```

> ⚠️ **IMPORTANT: Never commit your `.env` file** — it contains your Supabase secret keys.  
> If you accidentally exposed keys, immediately rotate them in the Supabase Dashboard.

---

## 🤝 Contributing

Contributions, issues, and feature requests are **very welcome**! 🙌

1. 🍴 **Fork** the repository
2. 🌿 Create your feature branch: `git checkout -b feature/amazing-feature`
3. ✏️ Commit your changes: `git commit -m "feat: Add amazing feature"`
4. 📤 Push to the branch: `git push origin feature/amazing-feature`
5. 🔁 Open a **Pull Request**

Please make sure to update tests as appropriate and follow the existing code style.

---

## 🐞 Known Issues

- QR Scanner may require HTTPS or `localhost` for camera access (browser security restriction)
- Offline mode sync requires manual trigger after reconnecting

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](./LICENSE) file for details.

---

## 👨‍💻 Author

**Javed Abuzar**  
[![GitHub](https://img.shields.io/badge/GitHub-javedabuzar969-181717?style=flat&logo=github)](https://github.com/javedabuzar969)

---

<div align="center">
  <b>⭐ If you found this project helpful, please give it a star! ⭐</b><br/><br/>
  <b>GymPro — Simplify Your Gym Management 💪</b><br/>
  Built with ❤️ using React · Supabase · Tailwind CSS · Capacitor
</div>