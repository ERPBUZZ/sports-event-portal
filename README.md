# Sports Event Portal

A free-hostable sports event portal built with React + Vite + Supabase.

## Features
- Public school registration → admin approval
- Team registration for Kho-Kho / Kabaddi
- Coach + Team Manager
- Player name/class/age + optional photo
- Team list print / browser Save as PDF
- Player ID card print / PDF
- Kho-Kho and Kabaddi match tabs
- Live / Upcoming / Completed match status
- Admin score control (+/-)
- Automatic points table
- Rules section
- Mobile responsive UI
- Supabase database persistence
- Optional live score refresh

## 1. Install
```bash
npm install
```

## 2. Environment
Copy `.env.example` to `.env` and put your Supabase project URL and Publishable key.

## 3. Database
Run `supabase/schema.sql` in Supabase SQL Editor.

Then create your admin user in Supabase:
Authentication → Users → Add user.

After the user exists, run the INSERT statement at the bottom of `supabase/schema.sql` with that user's UUID.

## 4. Local run
```bash
npm run dev
```

## 5. Free deployment
Push this folder to GitHub and import it into Vercel.
Add:
- VITE_SUPABASE_URL
- VITE_SUPABASE_PUBLISHABLE_KEY

No service-role key belongs in the browser.

## Important
The SQL uses RLS. The public can submit schools and teams, but only admin users can approve schools and change match scores.
For a production event, review the public-registration policy before opening registration.
