# Handover — HYROX Simulation Manager

**In plain terms:** this is the web page used to run HYROX Simulation events — assigning
volunteers and stations, running heats, and showing a live leaderboard on the TVs.

**Owner until 2026-09-29:** Lucas Rietsch (lucas@fitfactoryfitness.com).

## Do you need to touch any code?

**No** — this is a web page you open in a browser, like any website. Nobody running an event
needs to see or edit any code.

## How to actually use it

⚠️ **Action needed from Lucas before this section can be finished:** confirm the exact web
address (or bookmark) staff currently use to open this on event day, since it's not written
down anywhere in the project files. Add it here once confirmed:

> URL: _______________________________

Admin login (for anyone who needs to make changes, not just view) uses email + password
through the app itself — ask Lucas for the current admin login, or see "Setting up access"
below for how to create a new one.

## Setting up access (do this before 2026-09-29)

### 1. Firebase (stores all the event data — heats, participants, leaderboard)
1. Go to **console.firebase.google.com** and sign in with the Google account that should own
   this going forward (or get added to the existing one — ask Lucas which applies).
2. Open the project named **hyrox-sim-manager**.
3. Click the **gear icon** (top left, next to "Project Overview") → **Project settings**.
4. Click the **Users and permissions** tab.
5. Click **Add member**, enter the new owner's email, set role to **Owner**, click **Add member**.

This gives the new owner full control — billing, security settings, and the ability to
create/reset admin logins for the app itself.

### 2. Creating or resetting an admin login inside the app
The app has its own "change your password" screen once logged in. If nobody has the current
admin credentials, a new admin account can be created directly in the Firebase console:
Firebase console → your project → **Authentication** → **Users** tab → **Add user** (email +
password) — then that email/password logs into the app itself.

### 3. GitHub (where the code itself lives)
Done — this repository now lives at https://github.com/fitfactoryfitness/hyrox-sim-manager,
no longer tied to Lucas's personal account. You just need to be added as a member of the
`fitfactoryfitness` GitHub organization if you'll ever edit code yourself.

## Worth checking before treating this repo as fully public

Two old data exports (`hyrox-firestore-backup-2026-07-22*.json`) are sitting in this project's
files. They were spot-checked and looked empty of real participant info in the one sample
checked, but it's worth a quick look before giving broad access to this repository, in case
other events in those files do have real names/emails saved.
