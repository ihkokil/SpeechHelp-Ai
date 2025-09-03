<div align="center">
  <img src="https://yotrueuqjxmgcwlbbyps.supabase.co/storage/v1/object/public/images//SpeechHelp_Logo.svg" alt="SpeechHelp AI Logo" width="250"/>
  <br />
  <h1>SpeechHelp.ai</h1>
  <p><strong>Your personal AI-powered speech writing assistant.</strong></p>
  <p>
    <a href="https://speechhelp.ai/" target="_blank">
      <img src="https://img.shields.io/badge/Live_Demo-4CAF50?style=for-the-badge&logo=react&logoColor=white" alt="Live Demo"/>
    </a>
  </p>
</div>

---

**SpeechHelp.ai** is a sophisticated web application that leverages advanced AI to help users generate high-quality, personalized speeches for any occasion. From wedding toasts to corporate keynotes, the platform provides an intuitive, guided experience to craft memorable and impactful speeches effortlessly.

This project is a full-stack application built with a modern technology stack, featuring a React frontend and a comprehensive Supabase backend that handles the database, authentication, file storage, and serverless edge functions.

---

### ✨ Core Features

* **🤖 AI-Powered Generation**: Utilizes the OpenAI API to generate unique speeches tailored to the user's specific occasion, tone, and key talking points.
* **👤 User Dashboard**: A secure, personal workspace for users to create, edit, manage, and archive their speeches.
* **💳 Stripe Subscription Management**: Seamless and secure integration with Stripe for handling user subscriptions, payment methods, and billing cycles.
* **🔐 Secure Authentication & 2FA**: A complete authentication system including user registration, login, password reset, and Two-Factor Authentication (2FA) for enhanced security.
* **👑 Full-Featured Admin Panel**: An extensive dashboard for administrators to manage users, monitor all generated speeches, and configure system settings.
* **🌍 Multi-Language Support**: Built with internationalization (i18n) to support a global user base.
* **📱 Responsive & Modern UI**: A polished and intuitive user interface built with Tailwind CSS and Shadcn/UI, ensuring a flawless experience on any device.

_Add a screenshot or GIF of the application dashboard here._
![SpeechHelp.ai Dashboard Screenshot](https://speechhelp.ai/og-image.png)

---

### 🛠️ Technology Stack

<p align="center">
  <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React"/>
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript"/>
  <img src="https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite"/>
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS"/>
  <br />
  <img src="https://img.shields.io/badge/Supabase-3FCF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase"/>
  <img src="https://img.shields.io/badge/Stripe-626CD9?style=for-the-badge&logo=stripe&logoColor=white" alt="Stripe"/>
  <img src="https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white" alt="OpenAI"/>
</p>

| Category      | Technology                                                                                                  |
| ------------- | ----------------------------------------------------------------------------------------------------------- |
| **Frontend** | `React`, `Vite`, `TypeScript`, `Tailwind CSS`, `Shadcn/UI`                                                    |
| **Backend** | `Supabase` (PostgreSQL Database, Auth, Storage, Edge Functions)                                             |
| **Payments** | `Stripe`                                                                                                    |
| **AI** | `OpenAI API`                                                                                                |

---

### 🚀 Local Development Setup

Follow these instructions to get the project running on your local machine for development.

#### **Prerequisites**

* Node.js (v18.x or later)
* npm (or your preferred package manager like pnpm/bun)
* Supabase CLI ([Official Installation Guide](https://supabase.com/docs/guides/cli/getting-started))

#### **Step-by-Step Guide**

1.  **Clone the Repository**
    ```sh
    git clone [https://github.com/your-username/speech-helper-ai.git](https://github.com/your-username/speech-helper-ai.git)
    cd speech-helper-ai
    ```

2.  **Install Project Dependencies**
    ```sh
    npm install
    ```

3.  **Initialize Local Supabase Instance**
    * Log in to the Supabase CLI (only needs to be done once).
        ```sh
        supabase login
        ```
    * Start all the local Supabase services. This will generate your local API keys.
        ```sh
        supabase start
        ```
    * **Important:** Copy the `API URL` and `anon key` from the terminal output.

4.  **Configure Environment Variables**
    * Create a `.env` file by copying the sample file.
        ```sh
        cp sample.env .env
        ```
    * Open the `.env` file and populate it with the keys from the previous step and your personal API keys for OpenAI and Stripe.
        ```env
        VITE_SUPABASE_URL=YOUR_LOCAL_SUPABASE_URL_HERE
        VITE_SUPABASE_ANON_KEY=YOUR_LOCAL_ANON_KEY_HERE
        OPENAI_API_KEY=sk-...
        STRIPE_SECRET_KEY=sk_test_...
        STRIPE_WEBHOOK_SECRET=whsec_...
        ```
    * Set these variables as secrets for your local Supabase Edge Functions to use.
        ```sh
        supabase secrets set --env-file ./.env
        ```

5.  **Apply Database Migrations**
    * This command will reset the local database and apply the schema from your migrations folder.
        ```sh
        supabase db reset
        ```

6.  **Run the Application**
    * **Terminal 1: Start the Backend Functions**
        This command serves your Supabase Edge Functions locally.
        ```sh
        supabase functions serve
        ```
    * **Terminal 2: Start the Frontend Application**
        This command starts the Vite development server.
        ```sh
        npm run dev
        ```

The application should now be accessible at `http://localhost:5173`.

---

### 👤 Author

**Md. Iqbal Haider Khan**

* **GitHub**: [@ihkokil](https://github.com/ihkokil)
* **LinkedIn**: [in/ihkokil](https://www.linkedin.com/in/ihkokil/)

---

### 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more information.