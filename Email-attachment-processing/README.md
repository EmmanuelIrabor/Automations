# Email Attachment Processing & Archiving

An n8n automation that monitors Gmail for incoming emails, extracts their attachments, compresses them, and stores the resulting file for later use or archiving.

The project was built as a small example of how common file-handling tasks can be automated with n8n, Docker, Gmail, and Google Drive.

## What it does

The workflow currently follows this path:

Gmail  
→ Get the latest email  
→ Extract attachments  
→ Compress attachments  
→ Store the result in Google Drive

The idea is simple: instead of manually downloading files from an email, organizing them, compressing them, and uploading them somewhere else, the workflow handles the repetitive parts automatically.

## Workflow

```text
┌──────────────┐
│     Gmail    │
│ New / latest │
│    email     │
└──────┬───────┘
       │
       ▼
┌──────────────────┐
│ Get email data   │
│ + attachments    │
└──────┬───────────┘
       │
       ▼
┌──────────────────┐
│ Compress files   │
└──────┬───────────┘
       │
       ▼
┌──────────────────┐
│   Google Drive   │
│     Storage      │
└──────────────────┘
