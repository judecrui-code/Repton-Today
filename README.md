# Repton Today — video site

Blue single-page video site for the Repton Today podcast. Everyone can watch; only the owner can log in to upload or delete.

- **Hosting:** GitHub Pages (this repo).
- **Backend:** Supabase project "Repton Today" — a `videos` table, a public `videos` storage bucket, and email/password auth.
- **Who can upload:** database and storage rules only allow the signed-in admin account (judecrui@reptontoday.app). Anyone else is rejected by the database itself, not just hidden in the page.
- **Login:** username `judecrui` + the password set on that account in Supabase (Authentication → Users).
- **Limits:** Supabase's free plan caps each uploaded file at 50 MB. You can also paste a link to a video hosted elsewhere (e.g. GitHub).
- The `publishable` key in `index.html` is meant to be public. Never put the `secret` key in this repo.
