# Next-Gen AI Newsletter

**A visually distinctive HTML email newsletter designed for lawyers who hate newsletters.**

## Why This Exists

This template was created for weekly AI innovation communication at a law firm. The goal: stand out in crowded inboxes, be fun to read, and work perfectly on both desktop email clients (especially Outlook) and mobile devices.

## Key Features

### Core Features
- **ASCII Art Section Dividers** - Retro visual style that actually works in email
- **Magazine-Style Layout** - Boxes and visual sections, not walls of text
- **Mobile-First Design** - Perfect on iPhone Mail, Outlook mobile, Android Mail
- **Outlook-Safe HTML** - Uses tables and inline CSS (the only reliable method)
- **GenEmoji Integration** - Spots for personalized cartoon avatars as section headers
- **Easy Editing** - Look for `[EDIT:]` markers - no coding needed

### Advanced Features (New!)
- **Zig-Zag Cards** - Alternating left/right image-text layout (magazine flow)
- **Cinemagraph Hero** - Subtle animated GIF header (blinking cursor, shimmer effects)
- **Scroll Flipbook** - Vertical GIF that creates motion illusion during scroll
- **Ribbon & Flag Accents** - "NEW", "WIN", "TIP" labels with VML fallbacks for Outlook
- **Edge-Band Cards** - Color-coded vertical spines for different content types
- **Tap-to-Reveal Tabs** - Interactive tabs in Apple Mail/iOS, graceful fallback elsewhere
- **Parallax Split Card** - Diagonal split hero with background image + solid color
- **Dark Mode Support** - Optimized for dark mode email clients

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
├── templates/                      # Newsletter templates
│   ├── newsletter-template.html           # Basic template (original)
│   └── newsletter-advanced-template.html  # Advanced features template (NEW!)
├── examples/                       # Sample newsletters with real content
│   └── issue-001-launch.html
├── docs/                          # How-to guides
│   ├── editing-guide.md               # Non-coder editing instructions
│   ├── testing-guide.md               # Cross-client testing guide
│   ├── quick-reference.md             # Copy/paste snippets
│   ├── advanced-components.md (NEW!)  # Advanced feature documentation
│   └── asset-creation-guide.md (NEW!) # GIF and image creation guide
└── assets/                        # Helper files
    └── ascii-art.txt
```

## Which Template Should You Use?

**Basic Template** (`newsletter-template.html`):
- Simpler, faster to edit
- No GIF assets required
- Works everywhere without progressive enhancement
- Good for getting started quickly

**Advanced Template** (`newsletter-advanced-template.html`):
- All 7 advanced features included
- Requires creating GIF assets
- More visually striking
- Better for standing out in crowded inboxes
- Recommended once you're comfortable with basics

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
