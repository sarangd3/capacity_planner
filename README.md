# Resource Capacity Planner

Static web app (single `index.html`) backed by Supabase. Sign-in required.

## Deploy on GitHub Pages
1. Create a GitHub repo, add `index.html` (and this README) to the root, commit.
2. Repo -> Settings -> Pages -> Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. Open the URL GitHub shows (https://<user>.github.io/<repo>/).

## Supabase setup (one time)
1. Dashboard -> Authentication -> Sign In / Providers (or "Settings"): turn OFF "Allow new users to sign up".
2. Authentication -> Users -> Add user -> Create new user. Enter email + password, tick auto-confirm. Repeat for each person.
3. (Optional) Authentication -> URL Configuration: set Site URL to your GitHub Pages URL.

The tables `rp_tasks` and `rp_leaves` only allow signed-in users (row level security).
The key in index.html is the public "publishable" key; it is safe to publish. Never put the service_role key in this file.
