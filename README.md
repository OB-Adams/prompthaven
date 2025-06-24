# Prompt Haven 🚀

Prompt Haven is an open-source AI prompting platform built with **Next.js**, **Tailwind CSS**, and **MongoDB**. It empowers users to create, discover, and share creative AI prompts, fostering a vibrant community for AI-driven content creation. With secure Google OAuth authentication via **NextAuth.js**, Prompt Haven offers a seamless and scalable experience.

---

## ✨ Features

- **Secure Authentication**: Sign in with Google OAuth using NextAuth.js.
- **Prompt Management**: Create, edit, view, and share AI prompts stored in MongoDB.
- **Responsive UI**: Sleek, mobile-friendly design with Tailwind CSS.
- **Scalable Backend**: Next.js API routes for efficient server-side logic.
- **Community-Driven**: Discover and collaborate on prompts with other users.

---

## 🛠️ Tech Stack

- **Frontend**: Next.js, Tailwind CSS  
- **Backend**: Next.js API Routes, MongoDB  
- **Authentication**: NextAuth.js (Google OAuth)  
- **Deployment**: Vercel (recommended)  
- **Database**: MongoDB Atlas or local MongoDB  

---

## 📦 Installation

### Prerequisites

- Node.js: v16 or higher  
- MongoDB: Local instance or MongoDB Atlas  
- Google OAuth: Client ID and Secret from Google Cloud Console  

### Steps

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/ob-Adams/prompthaven.git
   cd prompthaven
   ```

2. **Install Dependencies**:
   ```bash
   npm install
   ```

3. **Configure Environment Variables**:  
   Create a `.env` file in the root directory with the following:

   ```env
   GOOGLE_ID=your-google-client-id
   GOOGLE_CLIENT_SECRET=your-google-client-secret
   MONGODB_URI=your-mongodb-connection-string
   NEXTAUTH_SECRET=your-secure-random-secret
   NEXTAUTH_URL=http://localhost:3000
   ```

   - Generate a secure `NEXTAUTH_SECRET`:
     ```bash
     openssl rand -base64 32
     ```

   - Get Google OAuth credentials from the [Google Cloud Console](https://console.cloud.google.com/).

   - Use a connection string from [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) or your local setup.

4. **Run the Development Server**:
   ```bash
   npm run dev
   ```

   Open [http://localhost:3000](http://localhost:3000) to view the app.

---

## 🚀 Deployment

1. **Push to GitHub**:
   ```bash
   git push origin main
   ```

2. **Deploy to Vercel**:
   - Import your repository into [Vercel](https://vercel.com/).
   - Add the following environment variables in Vercel’s dashboard:
     - `GOOGLE_ID`
     - `GOOGLE_CLIENT_SECRET`
     - `MONGODB_URI`
     - `NEXTAUTH_SECRET`
     - `NEXTAUTH_URL` (e.g., `https://prompthaven-rust.vercel.app`)
   - Deploy and access your production URL.

3. **Verify Environment**:
   - Ensure `NODE_ENV=production` is set.
   - Test authentication and API endpoints in production.

---

## 🧪 API Validation

To ensure Prompt Haven’s APIs (e.g., `/api/auth/[...nextauth]`, `/api/users`) are robust:

- **Tools**: Postman, cURL, or Insomnia  
- **Endpoints**:
  - `GET/POST /api/auth/[...nextauth]`: Google OAuth sign-in
  - `GET/POST /api/users`: User data management  

### Validation Tasks

- **Functionality**: Test valid/invalid requests, status codes (200, 401, 403)
- **Security**: Verify OAuth, test unauthorized access, check for injection risks
- **Performance**: Measure response times (<200ms) and load handling (10–50 users)
- **Reliability**: Ensure data consistency and idempotency for user operations

### Example Test with cURL

```bash
curl -X POST https://prompthaven-rust.vercel.app/api/auth/[...nextauth] \
  -H "Authorization: Bearer your-token"
```

---

## 🤝 Contributing

We welcome contributions! To contribute:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature"
   ```
4. Push to your branch:
   ```bash
   git push origin feature/your-feature
   ```
5. Open a pull request.

Please follow our Code of Conduct and ensure all tests pass before submitting.

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 📬 Contact

For questions, feedback, or issues:

- Open an issue on [GitHub](https://github.com/ob-Adams/prompthaven/issues)
- Email: obobadams@gmail.com

---

⭐ **Star this repo if you find Prompt Haven useful!** ⭐