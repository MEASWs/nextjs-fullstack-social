# My Fullstack Social App

A modern, full-stack social media web application built with Next.js, Prisma, PostgreSQL, Clerk Authentication, and Tailwind CSS.

## 🚀 Features

- **🔐 Secure Authentication:** Powered by [Clerk](https://clerk.dev/) for robust identity management.
- **📝 Create & Share Posts:** Users can share their thoughts and upload images.
- **💬 Interactive Comments:** Engage with others by commenting on posts.
- **❤️ Like System:** Like and unlike posts seamlessly.
- **👥 User Connections:** Follow and unfollow other users to see their content.
- **🔔 Notification System:** Stay updated when someone likes your post, comments, or follows you.
- **🎨 Modern UI:** Beautiful and fully responsive design utilizing [Tailwind CSS](https://tailwindcss.com/) and [Radix UI](https://www.radix-ui.com/).
- **🌗 Dark/Light Mode:** Full support for theming via `next-themes`.

## 🛠️ Tech Stack

- **Framework:** [Next.js 14](https://nextjs.org/) (App Router & Server Actions)
- **Frontend library:** [React 18](https://reactjs.org/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/), `clsx`, `tailwind-merge`
- **UI Components:** [Radix UI](https://www.radix-ui.com/), [Lucide React](https://lucide.dev/) (Icons)
- **Database ORM:** [Prisma](https://www.prisma.io/)
- **Database:** PostgreSQL
- **Authentication:** [Clerk](https://clerk.com/)

## ⚙️ Getting Started

Follow these instructions to set up the project locally on your machine.

### Prerequisites

- Node.js (v18 or higher recommended)
- PostgreSQL database (e.g., Supabase, Neon, or local PostgreSQL instance)
- A Clerk account

### Installation

1. **Clone the repository:**
   ```bash
   git clone <repository-url>
   cd my-fullstack-social
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Set up environment variables:**
   Create a `.env` file in the root directory and add the required keys:
   ```env
   # PostgreSQL Database URL
   DATABASE_URL="postgresql://user:password@host:port/database?schema=public"

   # Clerk Auth Keys
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=pk_test_...
   CLERK_SECRET_KEY=sk_test_...

   # Optional: Clerk URL Redirects (if needed)
   NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
   NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
   ```

4. **Initialize Database:**
   Generate the Prisma Client and push the schema to your database:
   ```bash
   npx prisma generate
   npx prisma db push
   ```

5. **Start the development server:**
   ```bash
   npm run dev
   ```

6. **Open your browser:**
   Navigate to [http://localhost:3000](http://localhost:3000) to see the app running.

## 🗄️ Database Schema Overview

The database uses Prisma and consists of the following core models:
- **`User`**: Profiles and Clerk authentication mapping.
- **`Post`**: User-generated content with optional images.
- **`Comment`**: Responses to specific posts.
- **`Like`**: Tracks the posts a user has liked.
- **`Follows`**: A self-relation managing the followers/following system.
- **`Notification`**: Activity alerts (`LIKE`, `COMMENT`, `FOLLOW`).

## 📜 License

This project is licensed under the MIT License.
