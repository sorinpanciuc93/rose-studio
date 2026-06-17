POSTUDIO — daily content-posting tracker for a small team
=========================================================

A phone-first dashboard to track how many Stories / Posts / Reels each
account posts per day against a daily goal, with a manager overview,
per-day history, and weekly/monthly reports.

LIVE URL:  https://sorinpanciuc93.github.io/Postudio/
REPO:      https://github.com/sorinpanciuc93/Postudio

It is already online and connected to Firebase, so it syncs live across
every phone — no setup needed to use it day to day.

==========================================================
A) LOGGING IN
==========================================================
  - Manager:  username  admin   + your manager code.
  - Team member: their username + their code (set by the manager).
    A team member only sees the accounts assigned to them.
  - Wrong username or code shows a single "Wrong username or code".
  - Log out with the red sign-out icon (top right).

==========================================================
B) MANAGING THE STUDIO (manager)
==========================================================
  Gear icon (top right) -> three tabs:
   - Accounts: add accounts, paste folder links (Drive / OneDrive),
     and set a daily goal per type. "Others" is a folder-only tile
     (no count) for storing documents.
   - Team: add people, give each a USERNAME and CODE, and tick which
     accounts they can see. ("admin" is reserved for the manager.)
   - Studio: change the manager code, see this device's status.

==========================================================
C) DAILY USE
==========================================================
  - Tap an account, then tap a category tile to open its folder.
    Post the content, then tap + to log it.
  - A completed goal turns the tile pastel green with a short
    celebration; the "Others" tile just opens its document folder.
  - The day strip + calendar let you view past days (read-only);
    only TODAY can be edited.

==========================================================
D) REPORTS
==========================================================
  - 📊 icon (top right) -> pick the accounts to include, choose a real
    calendar Week (Mon–Sun) or Month, then Generate.
  - Each day is green (goal met/surpassed) or red (missed); the header
    shows totals as posted/target (e.g. 2/14 stories).
  - Export with "Share image" (PNG) or "Share PDF" — both open the
    phone's native share sheet; files are named by period + accounts.

==========================================================
E) EDITING / DEPLOYING
==========================================================
  - Edit a file in the GitHub repo (pencil icon) -> Commit. GitHub
    Pages redeploys in ~1 minute. The app loads fresh on refresh.
  - Files: index.html (the whole app), firebase-config.js (keys),
    manifest.webmanifest, service-worker.js, icon-180/192/512.png.
  - Pages setting: Settings -> Pages -> Deploy from a branch ->
    Branch: main / (root).

==========================================================
F) FIREBASE (already configured)
==========================================================
  Backend project: rose-studio-6bd73 (internal id only — not shown to
  users; no need to rename). Firestore + Anonymous auth are enabled and
  the security rules allow read/write to any signed-in (anonymous) user.

  Security note: lightweight internal-tool security — the access codes
  are the practical gate, and anyone using the app can read/write the
  studio data. Fine for a small private team. Strict per-person
  permissions would need real user accounts (can be added later).

==========================================================
G) ADD TO HOME SCREEN (each phone)
==========================================================
  iPhone (Safari):  Share -> "Add to Home Screen".
  Android (Chrome): menu -> "Install app / Add to Home screen".
  Use the live URL above so the new name and icon show up.
