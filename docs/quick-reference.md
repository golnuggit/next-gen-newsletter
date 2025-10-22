# Quick Reference Guide

**Common edits you'll make every week - copy/paste ready.**

## Weekly Updates

### Change the Date/Issue Number

Find:
```html
Week of October 25, 2025 | Issue #001
```

Replace with:
```html
Week of [DATE], [YEAR] | Issue #[NUMBER]
```

---

## Text Formatting

### Make Text Bold

```html
<strong>This text will be bold</strong>
```

### Make Text Italic

```html
<em>This text will be italic</em>
```

### Both Bold and Italic

```html
<strong><em>Bold and italic</em></strong>
```

---

## Links

### Basic Link

```html
<a href="https://your-url.com" style="color: #0066cc; text-decoration: underline;">
    Link text here
</a>
```

### Link That Opens in New Tab

```html
<a href="https://your-url.com" target="_blank" style="color: #0066cc; text-decoration: underline;">
    Link text here
</a>
```

---

## Images

### Regular Image

```html
<img src="https://your-image-url.com/image.jpg"
     width="100%"
     style="max-width: 500px; border-radius: 8px; display: block; margin: 0 auto;">
```

### GenEmoji Avatar (Replace Yellow Box)

Delete the entire placeholder box and replace with:
```html
<div style="text-align: center; margin-bottom: 15px;">
    <img src="https://your-genemoji-url.com/image.png"
         width="100"
         height="100"
         style="border-radius: 50%;">
</div>
```

### Image with Link

```html
<a href="https://destination-url.com">
    <img src="https://image-url.com/image.jpg"
         width="100%"
         style="max-width: 500px; border-radius: 8px;">
</a>
```

---

## Color-Coded Boxes

### Info Box (Blue)

```html
<div style="background-color: #e7f5ff; border-left: 3px solid #00aaff; padding: 12px; border-radius: 4px;">
    Your info text here
</div>
```

### Success Box (Green)

```html
<div style="background-color: #d4edda; border-left: 3px solid #28a745; padding: 12px; border-radius: 4px;">
    Your success text here
</div>
```

### Warning Box (Yellow)

```html
<div style="background-color: #fff3cd; border-left: 3px solid #ffc107; padding: 12px; border-radius: 4px;">
    Your warning text here
</div>
```

### Important Box (Red)

```html
<div style="background-color: #f8d7da; border-left: 3px solid #dc3545; padding: 12px; border-radius: 4px;">
    Your important text here
</div>
```

---

## Lists

### Numbered List

```html
<ol style="margin: 0; padding-left: 20px; color: #333333; font-size: 15px; line-height: 1.8;">
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ol>
```

### Bullet List

```html
<ul style="margin: 0; padding-left: 20px; color: #333333; font-size: 15px; line-height: 1.8;">
    <li>First item</li>
    <li>Second item</li>
    <li>Third item</li>
</ul>
```

---

## Quotes & Callouts

### Quote Box

```html
<div style="background-color: #fff; border-left: 3px solid #6c757d; padding: 12px; font-style: italic; color: #666;">
    💬 "Your quote here"
</div>
```

### Tip Callout

```html
<div style="background-color: #f8f9fa; border-left: 3px solid #28a745; padding: 12px; border-radius: 4px;">
    <strong style="color: #28a745;">💡 Tip:</strong>
    <span style="color: #333333; font-size: 14px;">Your tip here</span>
</div>
```

---

## Section Headers

### Main Section Header (Blue Border)

```html
<h2 style="margin: 0 0 15px 0; color: #1a1a1a; font-size: 24px; border-left: 4px solid #00aaff; padding-left: 12px;">
    Your Section Title
</h2>
```

### Award Section Header (Gold Border)

```html
<h2 style="margin: 0 0 15px 0; color: #1a1a1a; font-size: 24px; border-left: 4px solid #ffc107; padding-left: 12px;">
    🪙 Perkins Coin Award
</h2>
```

### Challenge Section Header (Red Border)

```html
<h2 style="margin: 0 0 15px 0; color: #1a1a1a; font-size: 24px; border-left: 4px solid #dc3545; padding-left: 12px;">
    Your Challenge Title
</h2>
```

---

## ASCII Dividers

### Solid Line

```html
<tr>
    <td style="padding: 0 20px;">
        <div style="font-family: 'Courier New', monospace; color: #00aaff; font-size: 11px; text-align: center; line-height: 1;">
            ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
        </div>
    </td>
</tr>
```

### Box Top

```html
<tr>
    <td style="padding: 0 20px;">
        <div style="font-family: 'Courier New', monospace; color: #00aaff; font-size: 11px; text-align: center; line-height: 1;">
            ╔════════════════════════════════════════════════════════════╗
        </div>
    </td>
</tr>
```

### Box Bottom

```html
<tr>
    <td style="padding: 0 20px;">
        <div style="font-family: 'Courier New', monospace; color: #00aaff; font-size: 11px; text-align: center; line-height: 1;">
            ╚════════════════════════════════════════════════════════════╝
        </div>
    </td>
</tr>
```

### Dashed Line

```html
<tr>
    <td style="padding: 0 20px;">
        <div style="font-family: 'Courier New', monospace; color: #6c757d; font-size: 11px; text-align: center; line-height: 1;">
            ┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈┈
        </div>
    </td>
</tr>
```

---

## Spacing & Breaks

### Line Break

```html
<br>
```

### Add Space Between Paragraphs

```html
<p style="margin: 0 0 15px 0; color: #333333; font-size: 15px; line-height: 1.6;">
    First paragraph
</p>
<p style="margin: 0 0 15px 0; color: #333333; font-size: 15px; line-height: 1.6;">
    Second paragraph
</p>
```

### Add Extra Vertical Space

```html
<div style="height: 20px;"></div>
```

---

## Common Color Codes

```
#1a1a1a - Dark gray (almost black)
#333333 - Medium dark gray (body text)
#666666 - Medium gray
#6c757d - Light gray
#f4f4f4 - Very light gray (background)

#00ff00 - Bright green (terminal text)
#00aaff - Bright blue (dividers)
#0066cc - Link blue

#28a745 - Success green
#ffc107 - Warning yellow
#dc3545 - Danger red
#17a2b8 - Info blue
#6f42c1 - Purple

#f8f9fa - Light background
#fffbf0 - Light yellow background
#f0f8ff - Light blue background
#fff5f5 - Light red background
#d4edda - Light green background
```

---

## Emojis for Sections

Copy/paste these:

```
💡 - Ideas/Insights
🏆 - Award/Winner
🪙 - Perkins Coin
🎯 - Challenge/Target
✨ - Innovation/Magic
📚 - Resources/Learning
🎮 - Games/Fun
🔧 - How-To/Tools
🚀 - Launch/New
🔥 - Hot/Trending
🎉 - Celebration
🤔 - Thinking/Question
❓ - Question
✓ - Check/Success
💬 - Quote/Chat
📧 - Email/Contact
```

---

## Weekly Workflow Checklist

### Monday
- [ ] Collect content ideas throughout week
- [ ] Ask for Perkins Coin nominations

### Thursday
- [ ] Open last week's newsletter HTML
- [ ] Save as new filename (e.g., `newsletter-2025-11-01.html`)
- [ ] Update date and issue number
- [ ] Replace all content sections with this week's content
- [ ] Update Perkins Coin winner
- [ ] Update challenge
- [ ] Update Quick Hits
- [ ] Upload new GenEmojis (if creating fresh ones)
- [ ] Spell check

### Friday Morning
- [ ] Send test email to yourself
- [ ] Check on Outlook desktop
- [ ] Check on iPhone
- [ ] Click all links
- [ ] Fix any issues
- [ ] Send to distribution list at 9-10am

---

## Save This File

Bookmark this page - you'll reference it every week!
