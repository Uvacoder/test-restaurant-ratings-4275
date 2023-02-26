## About

Whenever I try a new restaurant, I give it a rating across five dimensions (food, bev, service, comfort, vibe). Often times, I do this in the uber home with my husband and forget our rating the next day. Not anymore! This is a simple web app that allows a user to store their restaurant ratings in Supabase.

You can check out the app here: https://five-stars.vercel.app/

## Getting Started

Run `npm install`

Go to [Supabase](https://supabase.com), sign up or log in, and [create a new project](https://app.supabase.com/).

After your project is ready, create a table in your Supabase database using the [SQL Editor](https://app.supabase.com/project/_/sql) in the Dashboard. Use the following SQL statement to create a ratings table with some sample data.

`
  create table ratings (
  id bigint generated by default as identity primary key,
  inserted_at timestamp with time zone default timezone('utc'::text, now()) not null,
  date timestamp with time zone,
  restaurant text,
  food text,
  beverage text,
  service text,
  comfort text,
  vibe text
);`

Create a new file in the root directory called `.env` and add your [project URL and public API key](https://app.supabase.com/project/_/settings/api):

`NEXT_PUBLIC_SUPABASE_URL="https://<project>.supabase.co"
NEXT_PUBLIC_SUPABASE_ANON_KEY="<your-anon-key>"`

Run `npm run dev`

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.
