# SensAi - AI Career Coach 🚀

A comprehensive full-stack AI-powered career coaching platform that helps professionals advance their careers with personalized guidance, interview preparation, and intelligent career tools.


## ✨ Features

- **🎯 Personalized Career Dashboard** - Track your career progress and get AI-powered insights
- **💼 Industry Insights** - Real-time salary data, market trends, and skill recommendations for your industry
- **🎤 Mock Interview Practice** - AI-generated technical interview questions tailored to your skills and industry
- **📄 AI Resume Builder** - Create ATS-optimized resumes with AI feedback and scoring
- **✍️ Cover Letter Generator** - Generate personalized cover letters for specific job applications
- **📊 Performance Analytics** - Track your interview performance and identify areas for improvement
- **🔐 Secure Authentication** - Powered by Clerk for seamless user management

## 🛠️ Tech Stack

- **Frontend:** Next.js 15, React 19, Tailwind CSS, Shadcn UI
- **Backend:** Next.js API Routes, Prisma ORM
- **Database:** PostgreSQL (Neon)
- **AI:** Google Gemini 2.5 Flash
- **Authentication:** Clerk
- **Background Jobs:** Inngest
- **Styling:** Tailwind CSS, Radix UI

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js 18+ and npm
- Git
- A Neon account (for PostgreSQL database)
- A Clerk account (for authentication)
- A Google AI Studio account (for Gemini API)

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/Venkat-Kolasani/SensAi---AI-Career-Coach.git
cd SensAi---AI-Career-Coach
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory:

```env
# Database Configuration
DATABASE_URL=your_neon_database_url

# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=your_clerk_publishable_key
CLERK_SECRET_KEY=your_clerk_secret_key

# Clerk URL Configuration
NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
NEXT_PUBLIC_CLERK_AFTER_SIGN_IN_URL=/onboarding
NEXT_PUBLIC_CLERK_AFTER_SIGN_UP_URL=/onboarding

# Google Gemini AI
GEMINI_API_KEY=your_gemini_api_key
```

### 4. Get Your API Keys

#### Neon Database (PostgreSQL)
1. Go to [neon.tech](https://neon.tech)
2. Create a new project
3. Copy the connection string
4. Paste it as `DATABASE_URL` in your `.env` file

#### Clerk Authentication
1. Go to [clerk.com](https://clerk.com)
2. Create a new application
3. Navigate to **API Keys** in the dashboard
4. Copy the **Publishable Key** and **Secret Key**
5. Add them to your `.env` file

#### Google Gemini API
1. Go to [Google AI Studio](https://aistudio.google.com/app/apikey)
2. Sign in with your Google account
3. Click **Create API Key**
4. Copy the key and add it to your `.env` file

### 5. Set Up the Database

```bash
# Generate Prisma Client
npx prisma generate

# Push the schema to your database
npx prisma db push
```

### 6. Run the Development Server

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## 📁 Project Structure

```
├── actions/              # Server actions for data operations
├── app/                  # Next.js app directory
│   ├── (auth)/          # Authentication pages
│   ├── (main)/          # Main application pages
│   └── api/             # API routes
├── components/          # Reusable React components
│   └── ui/             # Shadcn UI components
├── data/               # Static data and constants
├── lib/                # Utility functions and configurations
│   ├── inngest/       # Background job definitions
│   └── prisma.js      # Prisma client instance
├── prisma/             # Database schema and migrations
└── public/             # Static assets
```

## 🎨 Key Features Explained

### Mock Interview Practice
- AI generates 10 technical questions based on your industry and skills
- Multiple-choice format with detailed explanations
- Performance tracking and improvement suggestions
- Historical assessment data with progress charts

### Industry Insights
- Real-time salary ranges for various roles in your industry
- Market outlook and growth rate analysis
- Top in-demand skills and key industry trends
- Personalized skill recommendations

### Resume Builder
- Markdown-based resume editor
- ATS score calculation
- AI-powered feedback and suggestions
- PDF export functionality

### Cover Letter Generator
- Job-specific cover letter generation
- Company and role customization
- Save and manage multiple cover letters
- Professional formatting

## 🚢 Deployment

### Deploy to Vercel

1. Push your code to GitHub
2. Go to [vercel.com](https://vercel.com)
3. Import your repository
4. Add all environment variables from your `.env` file
5. Click **Deploy**

### Important Notes
- Make sure to add all environment variables in Vercel's dashboard
- The database should be accessible from Vercel's servers
- Clerk webhooks may need to be configured for production

## 🔧 Available Scripts

```bash
npm run dev          # Start development server
npm run build        # Build for production
npm start            # Start production server
npm run lint         # Run ESLint
npx prisma studio    # Open Prisma Studio (database GUI)
```



## 📝 License

This project is open source and available under the MIT License.


---

Made with ❤️ for career growth
