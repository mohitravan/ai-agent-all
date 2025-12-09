🧩 1. Gmail Auto-Reply Workflow (AI-Powered)
✅ Purpose

Automatically fetch unread Gmail messages, generate personalized replies using an AI Agent, store the conversation in Airtable, and mark each email as read.

🔧 Workflow Components

Schedule Trigger
Runs the workflow every X minutes to check for new emails.

Gmail – Get All Mails
Fetches unread emails from the user’s inbox.

Gmail – Get Mail Details
Extracts sender, subject, message body, and thread ID.

AI Agent (Google Gemini Chat Model)
Generates context-aware automatic email replies.
Inputs: subject + body
Outputs: reply message

Airtable – Create Record
Saves:

Sender email

Subject

AI-generated reply

Timestamp

Gmail – Mark as Read
Marks processed emails so they won’t be duplicated.

📤 Output

Auto-generated reply text

Airtable record

Clean inbox workflow
