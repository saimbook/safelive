
# SAFE TV App (Netlify + Neon DB)

## 📦 Structure
- Serverless functions hosted on Netlify
- PostgreSQL Database hosted on Neon
- Dynamic HTML frontend loads live TV channels

## 🚀 Deployment Guide

### 1. Create a Neon DB
- Create a table:
```sql
CREATE TABLE channels (
    id SERIAL PRIMARY KEY,
    name_bn TEXT NOT NULL,
    name_en TEXT NOT NULL,
    stream_url TEXT NOT NULL,
    logo_url TEXT
);
```

- Insert sample data using Neon Console or SQL script.

### 2. Upload this project to GitHub and connect to Netlify

### 3. Add environment variable in Netlify:
- `DATABASE_URL`: your Neon connection string

### 4. Done! Your site will now load channel list dynamically.
