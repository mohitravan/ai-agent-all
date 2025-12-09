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


🧩 2. HeyGen Video Generation Automation
✅ Purpose

Create an automated pipeline that:

Uploads a user-provided asset

Calls HeyGen API to create an AI avatar video

Polls until the video is ready

Downloads the final video automatically

🔧 Workflow Components

On Form Submission Trigger
Starts when a user uploads text/image/video via a form.

Upload Asset (HeyGen API)
Uploads the input file using:
POST https://upload.heygen.com/...

Wait Node
Ensures asset upload is completed.

Create Video (HeyGen API)
Calls:
POST https://api.heygen.com/v1/video.create

Wait Node
Allows processing time.

Get Video (HeyGen API)
Polls the job status with:
GET https://api.heygen.com/v1/video.get

Wait (Optional)
Re-poll until status = completed

Download Video
Downloads the final MP4 file.

📤 Output

Fully generated AI avatar video

Automatic download to local/system

Seamless end-to-end asset → video pipeline

🧩 3. AI Chat-to-Database Workflow (Structured Output)
✅ Purpose

Convert incoming chat messages into structured data using an AI Agent and save the parsed output into Airtable.

🔧 Workflow Components

When Chat Message Received
Trigger whenever a user sends a message.

AI Agent (OpenAI Chat Model)
Processes user input and generates structured JSON output.

Structured Output Parser
Ensures the AI response strictly follows a JSON format like:

{
  "name": "",
  "email": "",
  "message": "",
  "intent": "",
  "priority": ""
}


Airtable – Create Record
Saves the parsed fields into a database.

📤 Output

Perfectly structured data

Airtable CRM logs

Clean and consistent chat → database automation

Gmail – Mark as Read
Marks processed emails so they won’t be duplicated.

📤 Output

Auto-generated reply text

Airtable record

Clean inbox workflow
