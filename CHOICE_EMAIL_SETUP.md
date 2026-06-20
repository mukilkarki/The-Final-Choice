# Send Final Choice Answers to Your Gmail

This game is a static single-file HTML game, so it cannot send email by itself without a small free form service. The included code is ready for **FormSubmit**, a free service that can forward each player choice to your Gmail inbox.

## What gets emailed

When a player clicks **YES** or **NO**, the game sends:

- Game name: `The Final Choice`
- Choice label: `YES — Together We Rise` or `NO — A Promise Without Conditions`
- Raw choice: `yes` or `no`
- Timestamp
- Page URL
- Browser user-agent

## Setup steps

1. Open `index.html`.
2. Find this line near the top of the script:

   ```js
   const CHOICE_EMAIL_ENDPOINT = 'https://formsubmit.co/ajax/YOUR_GMAIL_ADDRESS';
   ```

3. Replace `YOUR_GMAIL_ADDRESS` with your real Gmail address.

   Example:

   ```js
   const CHOICE_EMAIL_ENDPOINT = 'https://formsubmit.co/ajax/yourname@gmail.com';
   ```

4. Save and publish the game.
5. Open the game in a browser and choose either **YES** or **NO** once.
6. FormSubmit will send an activation email to your Gmail inbox.
7. Open that activation email and click the confirmation link.
8. After confirmation, future player choices will arrive in your Gmail.

## Important notes

- The music and game will still work even if email is not configured.
- If the placeholder `YOUR_GMAIL_ADDRESS` is still in `index.html`, the game will not attempt to send anything.
- Browser ad blockers or privacy extensions may block third-party form requests. If that happens, test in a clean browser profile.
- Do not commit a private Gmail address if you are publishing the repository publicly and do not want that address visible.

## Free source used

- FormSubmit: <https://formsubmit.co/>

No backend server, paid plan, framework, or database is required.
