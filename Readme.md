# :globe_with_meridians: Prism: Parallel Social Posting

Prism is a lightweight, self-hosted web application designed to help you reclaim your time. It provides a single, unified interface to broadcast your thoughts across multiple decentralized social media platforms simultaneously. 

Currently, Prism supports simultaneous posting to **Bluesky** and **Mastodon**.

---
Backend: Python + Fastapi + Uvicorn

Frontend: HTML + CSS

Note: Frontend is the part that is AI-generated.
---

---

## Getting Started

### 1. Prerequisites
- [Docker](https://docs.docker.com/get-docker/) installed on your machine.
- [Docker Compose](https://docs.docker.com/compose/install/) installed.

### 2. Obtain Your Credentials

#### **For Mastodon:**
1. Log in to your Mastodon instance (e.g., [mastodon.social](https://mastodon.social)).
2. Navigate to **Preferences > Development > New Application**.
3. Give your app a name (e.g., "Prism") and ensure it has `write` permissions.
4. Once saved, click on the application name to find your credentials:
   - **Client Key** (This is your `MASTODON_CLIENT_ID`)
   - **Client Secret**
   - **Your Access Token**

#### **For Bluesky:**
1. You will need your handle (e.g., `user.bsky.social`).
2. It is highly recommended to use an **App Password** rather than your main password. Go to **Settings > App Passwords** on Bluesky to generate one.

---

### 3. Setup the Environment

Create a new folder on your host machine and create a file named `.env` inside it. Copy the following template and fill in your details:

```env
# Mastodon Configuration
MASTODON_CLIENT_ID=your_client_id_here
MASTODON_CLIENT_SECRET=your_client_secret_here
MASTODON_ACCESS_TOKEN=your_access_token_here
MASTODON_API_BASE_URL=[https://mastodon.social](https://mastodon.social)

# Bluesky Configuration
BLUESKY_HANDLE=yourname.bsky.social
BLUESKY_PASSWORD=your-app-password-here

# Application Port (Internal)
PORT=9000
```

### 4. Starting up the App
The compose.yaml file contains the docker configuration. By default, the app will be available on port 8000. You can change it as you will.
```
docker compose up -d
```
Now you app should be running on [http://localhost:8000](http://localhost:8000)

## 🤝 Contact & Support

Questions? Feedback? Reach out on the platforms:
Bluesky: [@cmodi306](@cmodi306.bsky.social)
Mastodon: [@cmodi3006](@cmodi3006@mastodon.social)