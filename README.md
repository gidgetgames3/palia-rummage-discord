# Palia Rummage Pile Daily Discord Post (Template)

This repo posts daily Palia rummage pile maps (Kilima, Bahari, Elderwood) to a Discord channel via webhook.

## One-click setup
1) Click **Use this template** → create your own repo  
2) In Discord, create a webhook for the channel you want  
3) In your new GitHub repo, add the webhook as a secret:

### Add the required secret
Repo → **Settings** → **Secrets and variables** → **Actions** → **New repository secret**

- Name: `DISCORD_WEBHOOK_URL`
- Value: your Discord webhook URL

## Run it
- It runs automatically on schedule.
- You can also run manually:
  **Actions → Daily Palia Rummage Post → Run workflow**

## Notes
- GitHub schedules can be delayed by a few minutes sometimes.
- If scheduled runs ever stop, make a small commit (e.g., edit this README) to “wake” schedules.

## Troubleshooting
### “Missing DISCORD_WEBHOOK_URL secret”
You didn’t add the repository secret, or the name is wrong. It must be exactly:
`DISCORD_WEBHOOK_URL`

### No scheduled runs
- Confirm workflow file is on the default branch (`main`)
- Repo → Actions → ensure workflows are allowed
- Make a small commit to wake schedules

### It runs but doesn’t post in Discord
- Confirm your webhook URL is valid and the Discord channel still exists
