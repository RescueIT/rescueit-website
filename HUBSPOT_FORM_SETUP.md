# HubSpot Form Setup Instructions

## What Was Done
1. ✅ Fixed button alignment in header - both "AI Labs" and "Free Evaluation" now use `.btn.primary` class
2. ✅ Replaced static contact info with HubSpot form embed structure

## Next Steps

### Create HubSpot Contact Form

1. Log in to HubSpot (portal ID: 342808547)
2. Navigate to: **Marketing > Lead Capture > Forms**
3. Click **"Create Form"**
4. Choose **"Embedded form"**
5. Add the following fields:
   - **Name** (Single-line text, required)
   - **Email** (Email, required)
   - **Phone** (Phone number, optional)
   - **Company** (Single-line text, optional)
   - **Message** (Multi-line text, optional)
6. Configure form settings:
   - Name: "Website Contact Form"
   - Thank you message: "Thank you! We'll be in touch soon."
7. Click **"Publish"**
8. Copy the **Form ID** (will be shown in the embed code)

### Update the Website

Once you have the Form ID:

1. Open `/Users/mikeross/.openclaw/workspace/rescueit-font-variant/index.html`
2. Find line ~118: `formId: "REPLACE_WITH_FORM_ID",`
3. Replace `REPLACE_WITH_FORM_ID` with your actual form ID
4. Save and push to GitHub

Example:
```javascript
formId: "abc123-def456-ghi789", // Your actual form ID
```

## Alternative: Use HubSpot Meeting Scheduler

If you prefer to use HubSpot's meeting scheduler instead of a contact form:

1. Go to **Settings > Marketing > Forms & Landing Pages > Meetings**
2. Create or copy the meeting link
3. Replace the form embed code with the meeting embed code in index.html

## Testing

After updating the form ID:
1. Visit the website
2. Navigate to the Contact section
3. Fill out and submit the form
4. Check HubSpot Contacts to verify the submission appears
