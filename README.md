# Next-Gen AI Newsletter

**A visually distinctive HTML email newsletter designed for lawyers who hate newsletters.**

## Why This Exists

This template was created for weekly AI innovation communication at a law firm. The goal: stand out in crowded inboxes, be fun to read, and work perfectly on both desktop email clients (especially Outlook) and mobile devices.

## Key Features

- **ASCII Art Section Dividers** - Retro visual style that actually works in email
- **Magazine-Style Layout** - Boxes and visual sections, not walls of text
- **Mobile-First Design** - Perfect on iPhone Mail, Outlook mobile, Android Mail
- **Outlook-Safe HTML** - Uses tables and inline CSS (the only reliable method)
- **GenEmoji Integration** - Spots for personalized cartoon avatars as section headers
- **Easy Editing** - Look for `[EDIT THIS]` markers - no coding needed

## Quick Start (For Non-Coders)

1. Open `templates/newsletter-template.html` in a text editor (or browser)
2. Find all `[EDIT THIS]` markers
3. Replace with your content
4. Replace `[IMAGE: description]` placeholders with your GenEmoji images
5. Send a test email to yourself
6. Check on your phone AND desktop email

## File Structure

```
next-gen-newsletter/
├── templates/              # Main newsletter template
│   └── newsletter-template.html
├── examples/              # Sample newsletters with real content
│   └── issue-001-launch.html
├── docs/                  # How-to guides
│   ├── editing-guide.md
│   └── testing-guide.md
└── assets/                # Helper files
    └── ascii-art.txt
```

## Testing Checklist

Before sending your newsletter, test on:
- [ ] Outlook desktop (Windows)
- [ ] Outlook 365 web
- [ ] iPhone Mail app
- [ ] Outlook iOS app
- [ ] Android Mail app
- [ ] Gmail web (bonus check)

## The Email HTML Secret

Email clients (especially Outlook) use 1999-era HTML rendering. Modern CSS doesn't work. This template uses:
- HTML tables for layout (yes, really)
- Inline CSS only (no external stylesheets)
- Email-safe fonts
- ASCII art (survives all email clients because it's just text)

## Credits

Built for lawyers by a lawyer with help from Claude. Because even partners can code with AI.

## First Issue Target

Friday, October 25, 2025
