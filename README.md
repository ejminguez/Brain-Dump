# 🧠 BrainDump – What Did I Learn Today?

**BrainDump** is a minimalist fullstack app that lets you log one thing you learned every day, helping you track your growth and build learning momentum — one brain cell at a time.

## 🚀 Features

- ✍️ Log what you learned daily (with tags, difficulty, and optional mood)
- 📅 See your learning timeline and contribution calendar
- 📊 Visualize your learning streaks and topics
- 🔐 Supabase Auth for secure personal logs
- 🎨 Clean, aesthetic interface with subtle animations
- 🌶️ (Optional) Export to Markdown, GPT-generated monthly summaries, learning shame bell™

## 📸 Screenshots

*(Add screenshots here when you’re done, like the dashboard, heatmap, and log input)*

## 🧪 Tech Stack

| Layer         | Tool                |
|---------------|---------------------|
| Frontend      | React               |
| Styling       | Tailwind CSS        |
| State Mgmt    | Zustand             |
| Backend       | Supabase (Postgres + Auth) |
| Charts        | Chart.js / Recharts |
| Bonus Spice   | Day.js, GSAP, OpenAI API (optional) |

## 🗃️ Database Schema

```sql
-- Table: learning_logs

id UUID PRIMARY KEY,
user_id UUID REFERENCES auth.users(id),
content TEXT,
topic TEXT,
difficulty INTEGER, -- 1 to 5
mood TEXT,
created_at TIMESTAMP DEFAULT now()
