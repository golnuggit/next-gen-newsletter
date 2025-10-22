# Newsletter Testing Guide

**Before you send to the whole firm, test on real devices and email clients.**

## Why Testing Matters

Email HTML is notoriously unpredictable. What looks perfect in Gmail might break in Outlook. What works on desktop might stack weird on mobile. You MUST test before sending.

## Quick Testing Checklist

- [ ] Outlook Desktop (Windows) - if you have access
- [ ] Outlook 365 Web - [outlook.office.com](https://outlook.office.com)
- [ ] iPhone Mail App - forward to your iPhone
- [ ] Outlook iOS App - if you use it
- [ ] Android Mail - if possible (ask a colleague)
- [ ] Gmail Web - bonus check
- [ ] All links work
- [ ] All images load
- [ ] Reads well on phone (vertical scroll)

---

## Method 1: Send Test Email to Yourself

### In Outlook Desktop

**Windows:**
1. Open Outlook
2. New Email
3. Click in the body
4. Go to Insert → Attach File
5. Browse to your `.html` file
6. Right-click the attached file → "Open"
7. Copy all the content that opens
8. Paste into email body
9. Send to yourself

**Mac:**
1. Open your `.html` file in a text editor
2. Select All (Cmd+A) → Copy (Cmd+C)
3. New Email in Outlook
4. Paste (Cmd+V)
5. Send to yourself

### In Gmail Web

1. Compose new email
2. Open your `.html` file in browser
3. Select all → Copy
4. Paste into Gmail compose window
5. Send to yourself

---

## Method 2: Use Email Testing Services (Recommended)

### Litmus (Free Trial)

1. Go to [litmus.com/email-testing](https://litmus.com/email-testing)
2. Sign up for free trial (no credit card for 7 days)
3. Create new test
4. Paste your entire HTML code
5. Click "Test email"
6. See previews across 90+ email clients instantly

**What you get:**
- Outlook 2016/2019/365 previews
- iPhone Mail previews (multiple iOS versions)
- Android Mail previews
- Gmail, Yahoo, Apple Mail
- Side-by-side comparisons

**Worth it?** YES for your first newsletter. Cancel after launch if you want.

### Email on Acid (Alternative)

Similar to Litmus: [emailonacid.com](https://emailonacid.com)
- Free trial available
- Same multi-client testing
- Good for one-time verification

---

## Method 3: Manual Device Testing

### iPhone Testing

1. Send test email to yourself
2. Open on iPhone in native Mail app
3. Check:
   - [ ] Sections stack vertically
   - [ ] Text is readable (not too small)
   - [ ] Images load
   - [ ] Links are tappable (not too close together)
   - [ ] ASCII art displays correctly
   - [ ] Colors show up
   - [ ] Easy to scroll past sections

### Android Testing

1. Send test to yourself or colleague with Android
2. Open in Gmail app or native Mail app
3. Check same items as iPhone

### Desktop Testing

1. Send test email
2. Open in Outlook desktop
3. Open in Outlook 365 web
4. Check:
   - [ ] Layout is centered (not left-aligned)
   - [ ] Images show (not blocked)
   - [ ] Width looks reasonable (should max at 600px)
   - [ ] Links work
   - [ ] Sections are visually distinct

---

## What To Look For

### Layout Issues

**Good:** Sections are visually separated, clear hierarchy, easy to scan

**Bad:** Everything runs together, hard to tell where sections start/end

**Fix:** Add more padding in style attributes (increase `padding: 20px` numbers)

### Image Issues

**Good:** All images load, appropriate size, not pixelated

**Bad:** Broken image icons, images too large/small, not loading

**Fix:**
- Check image URLs work in browser
- Use public URLs (Imgur, firm server)
- Add `width="100%"` and `style="max-width: 500px;"` to images

### Mobile Issues

**Good:** Sections stack vertically, text readable, links easy to tap

**Bad:** Text too small, sections side-by-side (shouldn't happen with tables), links too close

**Fix:**
- This template uses tables which force vertical stacking
- If text is small, increase font-size in style attributes
- Ensure links have padding between them

### ASCII Art Issues

**Good:** Lines align properly, characters display correctly

**Bad:** Characters misaligned, some symbols missing, looks jagged

**Fix:**
- Use `font-family: 'Courier New', Courier, monospace;`
- Ensure `line-height: 1;` or `line-height: 1.2;`
- Test with simpler ASCII if complex art breaks

### Color Issues

**Good:** Background colors show, text is readable against backgrounds

**Bad:** All white background (Outlook blocks some background colors)

**Fix:**
- Use borders instead of backgrounds for critical sections
- Test different color combinations
- Ensure text color contrasts with background

### Link Issues

**Good:** All links are blue/underlined and clickable

**Bad:** Links don't work, not obviously clickable

**Fix:**
- Check href URLs are correct
- Ensure style includes `color: #0066cc; text-decoration: underline;`
- Test each link by clicking

---

## Specific Email Client Quirks

### Outlook Desktop (Windows)

**Known issues:**
- Uses Microsoft Word rendering engine (yes, really)
- Blocks some background colors
- Strips out some CSS
- May not show web fonts

**What works:**
- HTML tables (that's why we use them)
- Inline CSS
- Basic colors
- Simple layouts

**Test specifically:**
- [ ] Tables render correctly
- [ ] Colors show (or fallback gracefully)
- [ ] Images load (may need to "Download pictures")

### Outlook 365 Web

**Known issues:**
- Better than desktop, but still quirky
- May rewrite some CSS

**What works:**
- Most things desktop Outlook supports
- Better color support

### iPhone Mail App

**Known issues:**
- Auto-zooms if text is too small
- May reformat very wide content

**What works:**
- Responsive design
- Images scale nicely
- Good color support

**Test specifically:**
- [ ] Font size readable without zooming
- [ ] Tap targets large enough for fingers
- [ ] Horizontal scrolling not needed

### Gmail

**Known issues:**
- Strips out <style> tags (we don't use them)
- Sometimes caches aggressively

**What works:**
- Inline CSS (what we use)
- Images
- Links

**Test specifically:**
- [ ] Images load (Gmail sometimes blocks by default)
- [ ] Layout looks clean

---

## Testing Your First Newsletter: Step-by-Step

### Day 1: Desktop Test
1. Send to yourself
2. Open in Outlook desktop
3. Open in Outlook 365 web
4. Check layout, images, links

### Day 2: Mobile Test
1. Forward to your iPhone
2. Check readability and layout
3. Ask colleague with Android to check

### Day 3: Fix Issues
1. Note any problems from Day 1-2
2. Make adjustments to HTML
3. Re-test

### Day 4: Final Check
1. Send one more test to yourself
2. Open on both desktop and phone
3. Click every link
4. Proofread one more time
5. If all good → schedule send for Friday

---

## Common Issues & Solutions

### Issue: Images Not Loading in Outlook

**Cause:** Outlook blocks external images by default

**Solution:** Recipients need to click "Download pictures" - this is normal. You can add a note at top: "Not seeing images? Click 'Download pictures' above."

**Prevention:** Upload images to trusted domain (firm server better than Imgur)

### Issue: Text Too Small on Mobile

**Cause:** Font size too small for phone screens

**Solution:** Increase font-size to at least 14px for body text, 16px for important text

### Issue: ASCII Art Misaligned

**Cause:** Wrong font or line-height

**Solution:**
```html
<pre style="font-family: 'Courier New', monospace; line-height: 1;">
YOUR ASCII ART
</pre>
```

### Issue: Links Not Clickable

**Cause:** Missing href or wrong syntax

**Solution:** Ensure format is:
```html
<a href="https://full-url.com" style="color: #0066cc;">Link text</a>
```

### Issue: Layout Broken in Outlook

**Cause:** CSS that Outlook doesn't support

**Solution:** Stick to tables and inline CSS (already done in template)

### Issue: Newsletter Too Wide on Desktop

**Cause:** Missing max-width

**Solution:** Table should have `style="max-width: 600px;"`

---

## Quick Fixes Before Sending

### If You're Short on Time

**Minimum viable testing:**
1. Send to yourself in Outlook
2. Forward to your iPhone
3. Check both - if they look good, you're probably safe

**What you can skip:**
- Android testing (if no one available)
- Gmail testing (nice to have, not critical for internal firm email)
- Multiple iOS versions

**What you CANNOT skip:**
- Outlook desktop test (most lawyers use this)
- iPhone test (many lawyers check email on phone)
- Link testing (broken links = bad look)
- Spell check

---

## Pre-Send Final Checklist

Print this and check off before hitting send:

### Content
- [ ] All `[EDIT THIS]` markers removed
- [ ] Your name and title correct
- [ ] Date/issue number correct
- [ ] Spell-checked
- [ ] Legal disclaimer (if required)

### Technical
- [ ] All links work
- [ ] All images load
- [ ] Email subject line written
- [ ] Tested in Outlook desktop
- [ ] Tested on iPhone
- [ ] ASCII art displays correctly

### Recipients
- [ ] Correct distribution list
- [ ] BCC considered (if sensitive)
- [ ] Scheduled for Friday morning (9-10am best)

---

## When Things Go Wrong

### You Sent It and Found a Typo

**Don't panic.** Send a quick follow-up:
"Correction: [fix the error]. That's what I get for writing the first newsletter about AI without AI proofreading it. 🤦"

People will appreciate the humanity.

### Links Don't Work

**Send immediate follow-up:**
"The link to [thing] isn't working. Here's the correct link: [URL]. Sorry for the confusion!"

### Images Don't Load for Anyone

**Don't recall the email.** Send follow-up:
"If images aren't loading, click 'Download pictures' at the top of the email. (Outlook blocks external images by default.)"

### Layout Completely Broken

**If it's unreadable:** Send plain text summary as follow-up, promise to fix for next week

**If it's just ugly:** Let it go. You'll fix it next week. First issue imperfection is forgiven.

---

## Tools & Resources

### Testing Services
- [Litmus](https://litmus.com) - Email testing across all clients
- [Email on Acid](https://emailonacid.com) - Alternative to Litmus
- [Can I Email](https://www.caniemail.com) - Check CSS support in email clients

### Validation
- [W3C HTML Validator](https://validator.w3.org) - Check HTML validity
- [Broken Link Checker](https://www.brokenlinkcheck.com) - Test all links

### Image Hosting
- [Imgur](https://imgur.com) - Free, easy, reliable
- Your firm's internal server - Best for security

---

## Remember

**Perfect is the enemy of shipped.**

Your first newsletter doesn't need to be flawless. It needs to:
1. Be readable
2. Have working links
3. Look intentional (not broken)
4. Get sent

Test enough to be confident, then hit send. You'll improve each week.

**The lawyers who need to read this are waiting. Don't let perfectionism delay launch.**
