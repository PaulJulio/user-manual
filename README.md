# Personal User Manual

Welcome to my personal "User Manual". This project is a comprehensive guide on how to work with me, designed for my co-workers and anyone interested in our professional collaboration.

## 🔗 Live Site
You can view the full manual here: [https://PaulJulio.github.io/user-manual/](https://PaulJulio.github.io/user-manual/)

## 🎯 Goal
The goal of this project is to provide a clear reference site that explains my work style, preferences, and expectations. It serves as an introduction to me and a resource for building effective working relationships.

## 🛠️ Tech Stack
- **Content:** Markdown (optimized for AI-readability)
- **Static Site Generator:** [Jekyll 4.3](https://jekyllrb.com/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **Hosting:** [GitHub Pages](https://pages.github.com/)

---

## 💻 Local Development

To preview changes locally before pushing to GitHub, follow these instructions.

### 1. Prerequisites (Ubuntu on WSL)
Ensure your WSL environment is up to date and has the necessary build tools:

```bash
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev libssl-dev libreadline-dev libyaml-dev libffi-dev
```

### 2. Configure Ruby Environment
To avoid permission issues and using `sudo` for gems, set up a local gem directory in your `~/.bashrc`:

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### 3. Install Dependencies
Install Bundler (Ruby manager) and the project's specific gems and node modules:

```bash
gem install bundler
bundle install
npm install
```

### 4. Start the Development Server
This project uses a concurrent script to run both the Tailwind CSS compiler and the Jekyll server:

```bash
npm run dev
```

### 5. Preview the Site
Once the server is running, open your browser to:
**[http://localhost:4000/user-manual/](http://localhost:4000/user-manual/)**

> **WSL Note:** If `localhost` doesn't resolve in your Windows browser, try using `http://127.0.0.1:4000/user-manual/`.

---

## 📚 Sections Covered
1.  **Introduction & Scope:** My role as an EM, my mission-driven approach, and what you should (and shouldn't) come to me for.
2.  **Communication Style:** My "High-Signal" philosophy, Slack-first habits, and how to interpret my silence.
3.  **Feedback & Recognition:** My preference for "Hot Feedback," Radical Candor, and team-wide wins.
4.  **Working Rhythm:** How I integrate work and life, protect my focus, and use AI to stay at high leverage.
5.  **Decision-Making:** My "No surprises, no heroes" rule and how I evaluate risk:reward.
6.  **Strengths & Quirks:** My focus on emotional maturity, semantic precision, and professional pet peeves.
7.  **Troubleshooting:** My triage-based response to stress and how to resolve conflict or re-earn trust.
8.  **Personal Context:** How my background as a Marine and 9-1-1 dispatcher shapes my perspective today.

## 🙏 Thank You
Thank you for taking the time to look through this repository and my manual. I value transparency and collaboration, and I hope this resource makes our time working together more effective and enjoyable.

---
*Built with the assistance of Gemini CLI.*
