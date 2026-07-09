# Job Tracker (n8n)

An automated workflow that checks RemoteOK for new job listings matching
specific keywords, avoids duplicate notifications, and sends new matches
to Telegram.

## How it works
1. Schedule Trigger runs every 6 hours
2. Fetches listings from the RemoteOK public API
3. Filters listings by keyword (python, machine learning, ai, intern, data)
4. Checks a Google Sheet to skip jobs already seen
5. Logs new jobs to the sheet
6. Sends a Telegram notification for each new match

## Setup
1. Import `job-tracker-workflow.json` into your n8n instance
2. Add credentials for:
   - Google Sheets (OAuth)
   - Telegram (bot token from @BotFather)
3. Create a Google Sheet with a `job_id` column and link it in the
   Google Sheets nodes
4. Activate the workflow

## Tech
n8n, RemoteOK API, Google Sheets, Telegram Bot API
