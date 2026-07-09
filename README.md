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
After importing `job-tracker-workflow.json`:
1. Reconnect the Google Sheets and Telegram credentials (these are not
   included in the export for security)
2. Update the `chatId` field in the "Send a text message" node with your
   own Telegram chat ID
3. Update the Google Sheets `documentId` to point to your own sheet

## Tech
n8n, RemoteOK API, Google Sheets, Telegram Bot API
