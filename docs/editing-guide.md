# Newsletter Editing Guide for Non-Coders

**You don't need to know how to code. Just find and replace.**

## Quick Start (5 Minutes)

1. **Open the template** - Right-click `templates/newsletter-template.html` and open with:
   - **Windows**: Notepad or Notepad++
   - **Mac**: TextEdit (Format → Make Plain Text first!)
   - **Any**: VS Code, Sublime Text, or any text editor

2. **Find `[EDIT THIS:`** - Use Find (Ctrl+F or Cmd+F) to jump to each editable section

3. **Replace the placeholder text** - Keep the HTML tags around it, just change the words

4. **Save and test** - Email it to yourself to see how it looks

---

## Step-by-Step: Your First Newsletter

### 1. Update the Header Info

**Find this:**
```
[EDIT THIS: Week of October 25, 2025 | Issue #001]
```

**Replace with:**
```
Week of October 25, 2025 | Issue #001
```

### 2. Write Your Opening

**Find this:**
```
[EDIT THIS: Your opening line]
```

**Replace with something like:**
```
Welcome to the first AI Digest!
```

**Then find:**
```
[EDIT THIS: 2-3 sentence intro. Keep it punchy...]
```

**Replace with:**
```
This week: I built a racing game in 30 minutes, we're launching the Perkins Coin award, and I've got a challenge that'll take you 5 minutes. Let's dive in.
```

### 3. Add Your Demo Content

**Find:**
```
[EDIT THIS: Demo Name]
```

**Replace with:**
```
PC Grand Prix
```

**Find:**
```
[EDIT THIS: Describe your demo. Example: "Meet <strong>PC Grand Prix</strong>..."]
```

**Replace with your description. Keep the `<strong>` tags around important words:**
```
Meet <strong>PC Grand Prix</strong> - a fully playable racing game I built in 30 minutes using Claude. No programming experience. Just conversation with AI.
```

**IMPORTANT:** See the `<strong>` tags? Those make text bold. Keep them!

### 4. Adding Images (Screenshots, GenEmojis)

**For regular screenshots, find:**
```
[INSERT SCREENSHOT HERE]
```

**Delete the placeholder box and add:**
```html
<img src="YOUR_IMAGE_URL_HERE" width="100%" style="max-width: 500px; border-radius: 8px; display: block; margin: 0 auto;">
```

**For GenEmoji avatars, find the yellow boxes with:**
```
[REPLACE WITH YOUR GENEMOJI: Dan holding lightbulb]
```

**Replace the entire yellow box with:**
```html
<img src="YOUR_GENEMOJI_URL" width="100" height="100" style="border-radius: 50%;">
```

### 5. Perkins Coin Winner Section

**Find:**
```
[EDIT THIS: Name]
```

**Replace with:**
```
Sarah Thompson
```

**Find the description and replace with what they did:**
```
Sarah automated client intake forms using ChatGPT Advanced Data Analysis, saving 3 hours per case. The 3D-printed Perkins Coin trophy is heading to her office via inter-office mail.
```

**Optional quote - find:**
```
[EDIT THIS: Optional quote from winner: "I didn't think I could do this myself..."]
```

**Replace with:**
```
"I didn't think I could do this myself, but with Claude's help it took 20 minutes." - Sarah
```

### 6. Weekly Challenge Section

**Find:**
```
[EDIT THIS: The challenge. Example: "Try the 'Put a Hat on Me' tool"]
```

**Replace with:**
```
Try the "Put a Hat on Me" tool
```

**Then add steps:**
```html
<li>Go to Google Gemini</li>
<li>Upload your headshot</li>
<li>Ask: "Put a silly hat on me"</li>
```

### 7. Sign-Off

**Find:**
```
[EDIT THIS: Your name]
```

**Replace with:**
```
Dan
```

**Find:**
```
[EDIT THIS: Your title - AI Implementation Partner]
```

**Replace with:**
```
AI Implementation Partner
```

---

## Understanding The Weird Code Stuff

### Don't Delete These!

**HTML Tags** - Things in angle brackets like `<strong>` or `</div>`:
- `<strong>` = bold text
- `<a href="URL">` = clickable link
- `<img src="URL">` = image
- `<br>` = line break

**Keep the tags, change what's between them.**

### Links

**Find:**
```html
<a href='#' style='color: #0066cc; text-decoration: underline;'>Play it here</a>
```

**Change the `#` to your URL:**
```html
<a href='https://your-game-url.com' style='color: #0066cc; text-decoration: underline;'>Play it here</a>
```

### Colors

If you want to change a section's color, look for `background-color: #XXXXXX` and replace with:
- `#f8f9fa` = light gray
- `#fffbf0` = light yellow
- `#f0f8ff` = light blue
- `#fff5f5` = light red
- `#d4edda` = light green

### Style Guide

**DO:**
- Keep it punchy (2-3 sentences max per section)
- Use bold (`<strong>`) for important names/terms
- Include links for everything
- Write like you're talking to a friend

**DON'T:**
- Write long paragraphs (lawyers won't read them)
- Use jargon or buzzwords
- Be preachy about AI
- Make it look like every other corporate email

---

## Getting Images Into Email

### Option 1: Upload to Imgur (Easiest)

1. Go to [imgur.com](https://imgur.com)
2. Click "New post"
3. Upload your image
4. Right-click the image → "Copy image address"
5. Paste that URL into your `src="HERE"`

### Option 2: Attach to Email (Less Reliable)

Some email clients block attachments. Use Option 1 for important images.

### Option 3: Use Your Firm's Server

If your IT department has an internal image server, upload there and use that URL.

---

## Before You Send: Checklist

- [ ] All `[EDIT THIS:]` markers removed or replaced
- [ ] Links tested (click each one)
- [ ] Images showing up (not broken)
- [ ] Your name and title correct
- [ ] GenEmoji avatars in place (or placeholders removed)
- [ ] Spell check (copy into Word if needed)
- [ ] Sent test email to yourself
- [ ] Checked on phone
- [ ] Checked in Outlook desktop

---

## Testing Your Newsletter

### Send a Test Email

**In Outlook:**
1. New Email
2. Paste the entire HTML into the body
   - **Windows**: Might need to Insert → Attach File → select the .html file
   - **Mac**: Copy all HTML code → paste into email
3. Send to yourself

**Better method - use a service:**
1. Copy all your HTML
2. Go to [litmus.com](https://litmus.com/email-testing) (free trial)
3. Paste HTML and see previews across all email clients

### What To Check

- **Desktop Outlook**: Does it look broken? Tables should prevent this.
- **iPhone Mail**: Can you read everything? Should stack vertically.
- **Gmail**: Colors and images showing?
- **Links**: Click every single one

---

## Common Issues & Fixes

### Images Not Showing

**Problem:** Broken image icon
**Fix:** Check your image URL - copy it into a browser to verify it works

### Text Running Together

**Problem:** No spacing between sections
**Fix:** Look for `padding` in the style - increase the numbers (e.g., `padding: 20px;` → `padding: 30px;`)

### Everything Left-Aligned

**Problem:** Newsletter looks off-center on desktop
**Fix:** This is normal - email HTML is limited. It'll still look fine.

### Colors Look Wrong

**Problem:** Background colors not showing in Outlook
**Fix:** Some Outlook versions block background colors. Use borders instead.

### GenEmoji Placeholder Still Showing

**Problem:** Yellow box with emoji still visible
**Fix:** You need to replace the ENTIRE `<div>` block with your `<img>` tag (see Section 4 above)

---

## Quick Reference: Common Edits

### Bold Text
```html
<strong>This will be bold</strong>
```

### Add a Link
```html
<a href="https://your-url.com" style="color: #0066cc;">Click here</a>
```

### Add an Image
```html
<img src="https://your-image-url.com/image.jpg" width="500" style="max-width: 100%;">
```

### Line Break
```html
First line<br>Second line
```

### New Paragraph
```html
<p style="margin: 0 0 15px 0; color: #333333;">Your paragraph here</p>
```

---

## Getting Help

1. **Can't find something?** Use Ctrl+F (or Cmd+F) to search
2. **Broke something?** Just re-download the template from GitHub
3. **Need to change the layout?** That's advanced - ask for help

## Pro Tips

1. **Save versions** - Save as `newsletter-2025-10-25.html` each week
2. **Keep a content doc** - Write your content in Word first, then paste into HTML
3. **Reuse what works** - Copy sections from previous successful issues
4. **Don't overthink it** - Lawyers want quick, scannable, useful. Simple wins.

---

## You've Got This

Remember: You're not trying to be a developer. You're just replacing placeholder text. If you can use Find & Replace in Word, you can do this.

**First newsletter jitters are normal. Ship it anyway.**
