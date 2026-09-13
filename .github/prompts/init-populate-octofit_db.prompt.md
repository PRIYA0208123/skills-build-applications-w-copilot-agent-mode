---
mode: 'agent'
model: GPT-5.5
description: 'Configure MongoDB and seed octofit_db for the Octofit multi-tier application'
---

Configure and seed the data tier for `octofit-tracker/backend`. Inspect the existing
backend structure first, preserve its conventions, and implement the changes rather
than only describing them.

Requirements:

1. Use MongoDB with Mongoose.
2. Use connection string for local MongoDB on port `27017` and database `octofit_db`.
3. Create Mongoose models for users, teams, activities, leaderboard, and workouts.
4. Add a seed script at `src/scripts/seed.ts`.
5. Include this help/description text in the seed script comments or logs:
   `Seed the octofit_db database with test data`.
6. Insert realistic sample data for all collections.
7. Ensure the seed operation is safe to rerun (clear or upsert the intended seed data,
   maintain references between related documents, and close the database connection).
8. Expose or use the backend's existing API routes to verify that each collection's
   seeded data is returned in API responses; add only the minimal routes needed if
   they do not already exist.
9. Run the seed script and relevant tests or API checks, and report any required
   startup commands or environment variables.
10. Commit and push your backend changes.
