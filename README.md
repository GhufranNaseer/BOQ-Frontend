# BOQ Task Management - Frontend

Professional event management system frontend built with React, Vite, and TypeScript for Badar Expo Solutions.

## 🚀 Tech Stack

- **Framework:** React 18
- **Build Tool:** Vite 5
- **Language:** TypeScript
- **Styling:** TailwindCSS
- **HTTP Client:** Axios
- **Routing:** React Router DOM v6

## 📋 Prerequisites

- Node.js >= 18.x
- npm or yarn
- Backend API running (see [Backend Repository](https://github.com/GhufranNaseer/BOQ-Backend))

## 🛠️ Local Development Setup

### 1. Clone Repository

```bash
git clone https://github.com/GhufranNaseer/BOQ-Frontend.git
cd BOQ-Frontend
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Environment Configuration

Create `.env.development` file:

```env
VITE_API_URL=http://localhost:3000/api
```

> **Note:** All environment variables MUST be prefixed with `VITE_` to be accessible in the application.

### 4. Start Development Server

```bash
npm run dev
```

The application will be available at `http://localhost:5173`

## 📦 Build for Production

```bash
npm run build
```

This creates an optimized production build in the `dist/` folder.

### Preview Production Build

```bash
npm run preview
```

## 🌍 Environment Variables

| Variable | Description | Example |
|----------|-------------|---------|
| `VITE_API_URL` | Backend API endpoint | `https://api.boq.yourdomain.com/api` |

See `.env.example` for more details.

## 🚢 Hostinger Deployment

### Prerequisites

- Hostinger account with Static Site hosting
- Backend API deployed and accessible
- Domain configured

### Deployment Steps

1. **Push to GitHub:**
   ```bash
   git push origin main
   ```

2. **Create Static Site in Hostinger:**
   - Navigate to: Hosting → Websites
   - Click "Create Website" → "Git Deployment"

3. **Configure Git Import:**
   - Repository URL: `https://github.com/GhufranNaseer/BOQ-Frontend.git`
   - Branch: `main`
   - Application root: `/`

4. **Build Settings:**
   - Build command: `npm install && npm run build`
   - Publish directory: `dist`

5. **Environment Variables:**
   Add in Hostinger Environment Variables:
   ```
   VITE_API_URL=https://api.boq.yourdomain.com/api
   ```

6. **Deploy:**
   - Click "Deploy"
   - Wait for build completion

7. **Configure Domain:**
   - Set up your domain (e.g., `boq.yourdomain.com`)
   - Wait for DNS propagation

8. **Verify Deployment:**
   - Visit your domain
   - Test login functionality
   - Check browser console for errors

## 🔐 Default Credentials

**Admin Account:**
- Email: `admin@badarexpo.com`
- Password: (Set via backend `SEED_ADMIN_PASSWORD`)

**Department Users:**
- Tech: `tech@badarexpo.com`
- Logistics: `logistics@badarexpo.com`
- Operations: `operations@badarexpo.com`
- HR: `hr@badarexpo.com`

> **Important:** Change default passwords immediately after first login.

## 📁 Project Structure

```
src/
├── components/         # Reusable React components
│   ├── admin/         # Admin-specific components
│   ├── common/        # Shared components
│   └── ...
├── pages/             # Page components
│   ├── admin/         # Admin pages
│   ├── auth/          # Authentication pages
│   └── user/          # User pages
├── routes/            # Route configuration
├── services/          # API service layer
├── context/           # React Context providers
├── hooks/             # Custom React hooks
├── types/             # TypeScript type definitions
├── utils/             # Utility functions
└── constants/         # Application constants
```

## 🧪 Available Scripts

| Script | Description |
|--------|-------------|
| `npm run dev` | Start development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Run ESLint |

## 🔧 Key Features

- **Role-Based Access Control:** Admin and department user roles
- **Event Management:** Create and manage events
- **CSV Upload:** Bulk task import via CSV
- **Task Assignment:** Assign tasks to departments/users
- **Responsive Design:** Mobile-friendly interface
- **Real-time Updates:** Live task status tracking

## 🐛 Troubleshooting

### Build Fails

**Issue:** Build fails with module errors  
**Solution:** Delete `node_modules` and reinstall:
```bash
rm -rf node_modules package-lock.json
npm install
```

### API Connection Errors

**Issue:** Cannot connect to backend  
**Solution:** Verify `VITE_API_URL` is correct and backend is running

### CORS Errors

**Issue:** CORS policy errors in browser console  
**Solution:** Ensure backend `FRONTEND_URL` includes your frontend domain

### Environment Variables Not Working

**Issue:** `import.meta.env.VITE_API_URL` is undefined  
**Solution:** Ensure variable is prefixed with `VITE_` and restart dev server

## 📞 Support

For issues or questions:
- Check [Backend Repository](https://github.com/GhufranNaseer/BOQ-Backend)
- Review Hostinger deployment logs
- Verify all environment variables are set correctly

## 📄 License

Private - Badar Expo Solutions

---

**Related Repositories:**
- [Backend API](https://github.com/GhufranNaseer/BOQ-Backend)
