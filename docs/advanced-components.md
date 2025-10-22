# Advanced Email Components Reference

**Email-safe implementations of innovative design features for Outlook & mobile.**

---

## 1. Zig-Zag Cards (Left/Right Magazine Flow)

**What it does:** Alternating image-text layout that creates a magazine-style flow. Stacks gracefully on mobile.

### Left-Aligned Card (Image Left, Text Right)

```html
<!-- Zig-Zag Card - LEFT ALIGNED -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 20px auto;">
    <tr>
        <td style="padding: 0;">
            <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
                <tr>
                    <!-- Image Cell - Left -->
                    <td width="200" valign="top" style="padding: 0; vertical-align: top;">
                        <img src="https://via.placeholder.com/200x200" alt="GenEmoji: Dan with lightbulb" width="200" height="200" style="display: block; width: 200px; height: 200px; border-radius: 12px; object-fit: cover;">
                    </td>
                    <!-- Spacer -->
                    <td width="20" style="font-size: 0; line-height: 0;">&nbsp;</td>
                    <!-- Text Cell - Right -->
                    <td valign="top" style="padding: 15px 20px; background-color: #f8f9fa; border-radius: 12px; vertical-align: top;">
                        <h3 style="margin: 0 0 10px 0; font-size: 20px; color: #1a1a1a; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            💡 This Week's Innovation
                        </h3>
                        <p style="margin: 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            Built PC Grand Prix in 30 minutes with no coding experience. Just AI conversation.
                        </p>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
</table>
```

### Right-Aligned Card (Text Left, Image Right)

```html
<!-- Zig-Zag Card - RIGHT ALIGNED -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 20px auto;">
    <tr>
        <td style="padding: 0;">
            <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" dir="rtl">
                <tr>
                    <!-- Image Cell - Right (using dir="rtl" to reverse) -->
                    <td width="200" valign="top" style="padding: 0; vertical-align: top; direction: ltr;">
                        <img src="https://via.placeholder.com/200x200" alt="GenEmoji: Dan with trophy" width="200" height="200" style="display: block; width: 200px; height: 200px; border-radius: 12px; object-fit: cover;">
                    </td>
                    <!-- Spacer -->
                    <td width="20" style="font-size: 0; line-height: 0;">&nbsp;</td>
                    <!-- Text Cell - Left -->
                    <td valign="top" style="padding: 15px 20px; background-color: #fff3cd; border-radius: 12px; vertical-align: top; direction: ltr;">
                        <h3 style="margin: 0 0 10px 0; font-size: 20px; color: #1a1a1a; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            🏆 Perkins Coin Winner
                        </h3>
                        <p style="margin: 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            Sarah automated client intake using ChatGPT, saving 3 hours per case.
                        </p>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
</table>
```

**Mobile Behavior:** On narrow screens (<480px), cells stack with image on top. Use `<!--[if !mso]><!-->` for responsive media queries.

---

## 2. Cinemagraph Hero (Subtle Motion)

**What it does:** Animated GIF with subtle motion (blinking cursor, shimmering light). First frame = complete message.

```html
<!-- Cinemagraph Hero Card -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 640px; margin: 20px auto;">
    <tr>
        <td style="padding: 0; position: relative;">
            <!-- Background with VML for Outlook -->
            <!--[if mso]>
            <v:rect xmlns:v="urn:schemas-microsoft-com:vml" fill="true" stroke="false" style="width:640px;height:300px;">
            <v:fill type="frame" src="https://your-server.com/cinemagraph-first-frame.jpg" color="#1a1a1a" />
            <v:textbox inset="0,0,0,0">
            <![endif]-->
            <div style="background-image: url('https://your-server.com/cinemagraph-animated.gif'); background-size: cover; background-position: center; background-color: #1a1a1a; border-radius: 16px; overflow: hidden;">
                <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
                    <tr>
                        <td style="padding: 60px 40px; text-align: center;">
                            <h1 style="margin: 0 0 15px 0; font-size: 36px; color: #ffffff; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif; font-weight: 700; text-shadow: 0 2px 4px rgba(0,0,0,0.3);">
                                AI DIGEST
                            </h1>
                            <p style="margin: 0; font-size: 18px; color: #00ff00; font-family: 'Courier New', Courier, monospace; text-shadow: 0 2px 4px rgba(0,0,0,0.5);">
                                Week of October 25, 2025 ▌
                            </p>
                        </td>
                    </tr>
                </table>
            </div>
            <!--[if mso]>
            </v:textbox>
            </v:rect>
            <![endif]-->
        </td>
    </tr>
</table>
```

**GIF Creation Tips:**
- First frame must contain complete message
- Keep under 1MB (optimize with ezgif.com or gifsicle)
- Subtle motion: blinking cursor (▌), shimmer effect, gentle pulse
- Export at 10-15 fps, loop infinitely
- Provide JPG first frame for Outlook 2007-2016 via VML

---

## 3. Scroll Illusion Flipbook

**What it does:** Tall vertical GIF creates illusion of movement during scroll (e.g., progress bar filling).

```html
<!-- Scroll Illusion Flipbook - Vertical Card -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 20px auto;">
    <tr>
        <td style="padding: 0;">
            <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
                <tr>
                    <!-- Narrow vertical strip with animated GIF -->
                    <td width="60" valign="top" style="padding: 0; vertical-align: top;">
                        <img src="https://your-server.com/progress-bar-filling.gif" alt="Progress indicator" width="60" height="400" style="display: block; width: 60px; height: 400px; border-radius: 8px;">
                    </td>
                    <!-- Spacer -->
                    <td width="20" style="font-size: 0; line-height: 0;">&nbsp;</td>
                    <!-- Main content beside the flipbook -->
                    <td valign="top" style="padding: 20px; background-color: #f8f9fa; border-radius: 12px; vertical-align: top;">
                        <h3 style="margin: 0 0 15px 0; font-size: 20px; color: #1a1a1a; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            Your Progress This Week
                        </h3>
                        <ul style="margin: 0; padding-left: 20px; font-size: 15px; line-height: 1.8; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            <li>Tried PC Grand Prix ✓</li>
                            <li>Put a hat on your headshot ✓</li>
                            <li>Submitted Perkins Coin nomination ✓</li>
                            <li>Shared with a colleague ✓</li>
                        </ul>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
</table>
```

**GIF Design:**
- Tall (400-600px), narrow (40-80px)
- Slow animation (5-10 seconds per loop)
- First frame = empty state (e.g., empty progress bar)
- Creates "filling up" illusion as user scrolls
- Alternative: Checkboxes appearing, arrows pointing down

---

## 4. Ribbon & Flag Accents

**What it does:** Angled ribbon labels ("NEW", "WIN", "TIP") with VML for Outlook.

```html
<!-- Card with "NEW" Ribbon - Top Right Corner -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 20px auto;">
    <tr>
        <td style="padding: 0; position: relative;">
            <div style="position: relative; background-color: #ffffff; border: 2px solid #dee2e6; border-radius: 12px; padding: 30px 20px; overflow: visible;">

                <!-- Ribbon - NEW (Top Right) -->
                <div style="position: absolute; top: 20px; right: -5px; background-color: #dc3545; color: #ffffff; padding: 6px 20px; font-size: 12px; font-weight: 700; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif; text-transform: uppercase; letter-spacing: 0.5px; box-shadow: 0 2px 4px rgba(0,0,0,0.2); border-radius: 4px 0 0 4px; z-index: 10;">
                    NEW
                    <div style="position: absolute; right: -0px; top: 100%; width: 0; height: 0; border-style: solid; border-width: 0 5px 5px 0; border-color: transparent #991f2c transparent transparent;"></div>
                </div>

                <!-- VML Fallback for Outlook -->
                <!--[if mso]>
                <v:shape xmlns:v="urn:schemas-microsoft-com:vml" style="position:absolute;top:20px;right:-5px;width:80px;height:28px;" fillcolor="#dc3545" strokecolor="#dc3545">
                    <v:textbox inset="0,6px,0,0">
                        <div style="color:#ffffff;font-size:12px;font-weight:bold;text-align:center;">NEW</div>
                    </v:textbox>
                </v:shape>
                <![endif]-->

                <!-- Card Content -->
                <h3 style="margin: 0 0 10px 0; font-size: 20px; color: #1a1a1a; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                    PC Grand Prix Launch
                </h3>
                <p style="margin: 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                    Our first AI-built game is live! Race around the track with the Perkins Coie logo.
                </p>
            </div>
        </td>
    </tr>
</table>
```

**Ribbon Variations:**

```html
<!-- WIN Ribbon - Gold -->
<div style="position: absolute; top: 20px; right: -5px; background-color: #ffc107; color: #1a1a1a; padding: 6px 20px; font-size: 12px; font-weight: 700; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif; text-transform: uppercase; letter-spacing: 0.5px; box-shadow: 0 2px 4px rgba(0,0,0,0.2); border-radius: 4px 0 0 4px;">
    WIN 🏆
    <div style="position: absolute; right: 0; top: 100%; width: 0; height: 0; border-style: solid; border-width: 0 5px 5px 0; border-color: transparent #cc9a06 transparent transparent;"></div>
</div>

<!-- 60-SEC TIP Ribbon - Blue -->
<div style="position: absolute; top: 20px; left: -5px; background-color: #0066cc; color: #ffffff; padding: 6px 20px; font-size: 12px; font-weight: 700; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif; text-transform: uppercase; letter-spacing: 0.5px; box-shadow: 0 2px 4px rgba(0,0,0,0.2); border-radius: 0 4px 4px 0;">
    60-SEC TIP ⏱️
    <div style="position: absolute; left: 0; top: 100%; width: 0; height: 0; border-style: solid; border-width: 0 0 5px 5px; border-color: transparent transparent transparent #004d99;"></div>
</div>
```

**Note:** Ribbons use CSS triangles for "flag" effect. Outlook 2007-2016 renders VML fallback (simpler rectangle).

---

## 5. Edge-Band Cards (Bold Color Spines)

**What it does:** Vertical colored stripe on card edge, color-coded by section type.

```html
<!-- Edge-Band Card - Yellow Spine (Tips) -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 20px auto;">
    <tr>
        <td style="padding: 0;">
            <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="background-color: #ffffff; border-radius: 12px; overflow: hidden; box-shadow: 0 2px 8px rgba(0,0,0,0.1);">
                <tr>
                    <!-- Color Spine - Left Edge (8px wide) -->
                    <td width="8" style="background-color: #ffc107; padding: 0; width: 8px;">
                        <!-- Spine spacer -->
                    </td>
                    <!-- Card Content -->
                    <td style="padding: 25px 20px; background-color: #ffffff;">
                        <div style="color: #ffc107; font-size: 11px; font-weight: 700; text-transform: uppercase; letter-spacing: 1px; margin-bottom: 8px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            💡 Quick Tip
                        </div>
                        <h3 style="margin: 0 0 10px 0; font-size: 18px; color: #111111; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            Add "Make it conversational" to prompts
                        </h3>
                        <p style="margin: 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            When asking AI to write, add "Make it conversational, not corporate" at the end. The difference is shocking.
                        </p>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
</table>
```

**Color-Coding System:**

```html
<!-- Tips = Yellow (#ffc107) -->
<td width="8" style="background-color: #ffc107; padding: 0;"></td>

<!-- Food for Thought = Blue (#0066cc) -->
<td width="8" style="background-color: #0066cc; padding: 0;"></td>

<!-- Wins/Awards = Gold (#f39c12) -->
<td width="8" style="background-color: #f39c12; padding: 0;"></td>

<!-- Challenges = Red (#dc3545) -->
<td width="8" style="background-color: #dc3545; padding: 0;"></td>

<!-- Resources = Green (#28a745) -->
<td width="8" style="background-color: #28a745; padding: 0;"></td>

<!-- Innovation = Purple (#6f42c1) -->
<td width="8" style="background-color: #6f42c1; padding: 0;"></td>
```

**Dark Mode Support:**

```html
<style>
@media (prefers-color-scheme: dark) {
    .edge-band-card { background-color: #1a1a1a !important; }
    .edge-band-content { color: #e0e0e0 !important; }
    .edge-band-heading { color: #ffffff !important; }
}
</style>

<!-- Apply classes: -->
<td style="padding: 25px 20px; background-color: #ffffff;" class="edge-band-card">
```

---

## 6. Tap-to-Reveal Tabs

**What it does:** Interactive tabs in WebKit (Apple Mail/iOS). Fallback shows TL;DR in Outlook/Gmail.

```html
<!-- Tap-to-Reveal Tabs Card -->

<!--[if !mso]><!-->
<!-- CSS for WebKit clients (Apple Mail, iOS) -->
<style>
.tab-content { display: none; }
#tab1:checked ~ .tab-panels #panel1,
#tab2:checked ~ .tab-panels #panel2,
#tab3:checked ~ .tab-panels #panel3 { display: block; }

.tab-label {
    display: inline-block;
    padding: 10px 20px;
    background-color: #e9ecef;
    color: #333333;
    font-size: 14px;
    font-weight: 600;
    border-radius: 8px 8px 0 0;
    cursor: pointer;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;
    margin-right: 5px;
}

#tab1:checked ~ .tab-nav label[for="tab1"],
#tab2:checked ~ .tab-nav label[for="tab2"],
#tab3:checked ~ .tab-nav label[for="tab3"] {
    background-color: #0066cc;
    color: #ffffff;
}

input[type="radio"] { position: absolute; opacity: 0; }
</style>
<!--<![endif]-->

<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 600px; margin: 20px auto;">
    <tr>
        <td style="padding: 0;">

            <!--[if !mso]><!-->
            <!-- Interactive version for WebKit -->
            <div>
                <input type="radio" name="tabs" id="tab1" checked>
                <input type="radio" name="tabs" id="tab2">
                <input type="radio" name="tabs" id="tab3">

                <div class="tab-nav" style="background-color: #f8f9fa; padding: 15px 15px 0 15px; border-radius: 12px 12px 0 0;">
                    <label for="tab1" class="tab-label">TL;DR</label>
                    <label for="tab2" class="tab-label">Why it matters</label>
                    <label for="tab3" class="tab-label">How to try</label>
                </div>

                <div class="tab-panels" style="background-color: #ffffff; border: 2px solid #e9ecef; border-top: none; border-radius: 0 0 12px 12px; padding: 20px;">
                    <div id="panel1" class="tab-content" style="display: block;">
                        <p style="margin: 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            <strong>TL;DR:</strong> Claude can now remember context across conversations with Projects. Upload firm docs once, reference forever.
                        </p>
                    </div>
                    <div id="panel2" class="tab-content">
                        <p style="margin: 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            <strong>Why it matters:</strong> No more re-uploading case files or re-explaining context. The AI remembers your work style, firm policies, and ongoing projects.
                        </p>
                    </div>
                    <div id="panel3" class="tab-content">
                        <p style="margin: 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                            <strong>How to try:</strong> Go to claude.ai → Click "Projects" → Upload your most-used documents → Start chatting. The AI references them automatically.
                        </p>
                    </div>
                </div>
            </div>
            <!--<![endif]-->

            <!--[if mso]>
            <!-- Fallback for Outlook: Show TL;DR only -->
            <div style="background-color: #ffffff; border: 2px solid #e9ecef; border-radius: 12px; padding: 20px;">
                <p style="margin: 0 0 10px 0; font-size: 15px; line-height: 1.6; color: #333333; font-family: Arial, sans-serif;">
                    <strong>TL;DR:</strong> Claude can now remember context across conversations with Projects. Upload firm docs once, reference forever.
                </p>
                <p style="margin: 0; font-size: 13px; color: #666666; font-family: Arial, sans-serif;">
                    <a href="[WEB-VERSION-URL]#full-article" style="color: #0066cc;">Read more: Why it matters & How to try</a>
                </p>
            </div>
            <![endif]-->

        </td>
    </tr>
</table>
```

**How it works:**
- **WebKit/Apple Mail:** CSS checkbox hack enables tab switching
- **Outlook/Gmail:** Shows TL;DR with link to web version
- Graceful degradation ensures content is always accessible

---

## 7. Parallax-Style Split Card

**What it does:** Hero card split diagonally with solid color + background image.

```html
<!-- Parallax Split Card Hero -->
<table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%" style="max-width: 640px; margin: 20px auto;">
    <tr>
        <td style="padding: 0;">

            <!--[if mso]>
            <v:rect xmlns:v="urn:schemas-microsoft-com:vml" fill="true" stroke="false" style="width:640px;height:320px;">
            <v:fill type="frame" src="https://your-server.com/diagonal-split-bg.jpg" color="#1a1a1a" />
            <v:textbox inset="0,0,0,0">
            <![endif]-->

            <div style="background: linear-gradient(135deg, #1a1a1a 0%, #1a1a1a 50%, transparent 50%), url('https://your-server.com/diagonal-split-bg.jpg'); background-size: cover; background-position: center; background-color: #1a1a1a; border-radius: 16px; overflow: hidden; min-height: 320px; position: relative;">

                <table role="presentation" cellspacing="0" cellpadding="0" border="0" width="100%">
                    <tr>
                        <td width="50%" valign="middle" style="padding: 40px 30px; vertical-align: middle;">
                            <!-- Left Side - Solid Color with Text -->
                            <h1 style="margin: 0 0 15px 0; font-size: 32px; color: #ffffff; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif; font-weight: 700;">
                                AI Innovation<br>Starts Here
                            </h1>
                            <p style="margin: 0 0 20px 0; font-size: 16px; color: #00ff00; font-family: 'Courier New', Courier, monospace;">
                                Week of Oct 25, 2025
                            </p>
                            <a href="#" style="display: inline-block; padding: 12px 24px; background-color: #0066cc; color: #ffffff; text-decoration: none; border-radius: 6px; font-size: 14px; font-weight: 600; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Arial, sans-serif;">
                                Dive In →
                            </a>
                        </td>
                        <td width="50%" valign="middle" style="padding: 40px 30px; text-align: right; vertical-align: middle;">
                            <!-- Right Side - Image/GenEmoji -->
                            <img src="https://via.placeholder.com/200x200" alt="GenEmoji: Dan pointing forward" width="200" height="200" style="display: inline-block; width: 200px; height: 200px; border-radius: 50%; border: 4px solid #ffffff; box-shadow: 0 4px 12px rgba(0,0,0,0.3);">
                        </td>
                    </tr>
                </table>

            </div>

            <!--[if mso]>
            </v:textbox>
            </v:rect>
            <![endif]-->

        </td>
    </tr>
</table>
```

**Creating the Background Image:**

1. **Photoshop/Figma:**
   - Canvas: 640x320px
   - Draw diagonal line from top-right to bottom-left
   - Left half: Solid color (#1a1a1a)
   - Right half: Your image/gradient

2. **CSS Fallback:**
   ```css
   background: linear-gradient(135deg, #1a1a1a 0%, #1a1a1a 50%, transparent 50%),
               url('image.jpg');
   ```

3. **VML for Outlook:**
   - Use `<v:fill>` with background image
   - Text remains readable with `<v:textbox>`

---

## General Implementation Tips

### Mobile Responsiveness

Add this media query block in `<head>`:

```html
<style>
@media only screen and (max-width: 480px) {
    /* Stack zig-zag cards */
    .stack-mobile {
        display: block !important;
        width: 100% !important;
        max-width: 100% !important;
    }

    /* Full-width images */
    .mobile-full {
        width: 100% !important;
        height: auto !important;
    }

    /* Hide on mobile */
    .hide-mobile {
        display: none !important;
    }
}
</style>
```

### Dark Mode Safety

```html
<style>
@media (prefers-color-scheme: dark) {
    .dark-bg { background-color: #1a1a1a !important; }
    .dark-text { color: #e0e0e0 !important; }
    .dark-heading { color: #ffffff !important; }
    .dark-border { border-color: #333333 !important; }
}

/* Outlook dark mode overrides */
[data-ogsc] .dark-bg { background-color: #1a1a1a !important; }
[data-ogsc] .dark-text { color: #e0e0e0 !important; }
</style>
```

### VML Namespace Declaration

Add to `<head>` for Outlook VML support:

```html
<!--[if mso]>
<xml>
    <o:OfficeDocumentSettings>
        <o:AllowPNG/>
        <o:PixelsPerInch>96</o:PixelsPerInch>
    </o:OfficeDocumentSettings>
</xml>
<![endif]-->
```

And in `<html>` tag:

```html
<html lang="en" xmlns="http://www.w3.org/1999/xhtml" xmlns:v="urn:schemas-microsoft-com:vml" xmlns:o="urn:schemas-microsoft-com:office:office">
```

---

## Asset Creation Checklist

### For Cinemagraphs & Flipbooks:
- [ ] Create GIF with first frame containing complete message
- [ ] Optimize to <1MB (use ezgif.com)
- [ ] Export matching JPG first frame for Outlook VML
- [ ] Test in email clients (Litmus/Email on Acid)

### For Ribbons & Flags:
- [ ] Design ribbon graphics (can use CSS shapes)
- [ ] Create VML fallback rectangles for Outlook
- [ ] Test positioning across clients

### For Split Card Backgrounds:
- [ ] Create 640x320px diagonal split image
- [ ] Export at 2x resolution (1280x640px) for Retina
- [ ] Optimize for web (<200KB)
- [ ] Test VML rendering in Outlook

---

## Testing Matrix

| Feature | Outlook Desktop | Outlook 365 | Apple Mail | iOS Mail | Gmail | Android |
|---------|----------------|-------------|------------|----------|-------|---------|
| Zig-Zag Cards | ✓ (stacks) | ✓ | ✓ | ✓ (stacks) | ✓ | ✓ (stacks) |
| Cinemagraph | First frame only | ✓ Animated | ✓ Animated | ✓ Animated | ✓ Animated | ✓ Animated |
| Flipbook GIF | First frame only | ✓ Animated | ✓ Animated | ✓ Animated | ✓ Animated | ✓ Animated |
| Ribbons | VML fallback | ✓ CSS | ✓ CSS | ✓ CSS | ✓ CSS | ✓ CSS |
| Edge-Bands | ✓ | ✓ | ✓ | ✓ | ✓ | ✓ |
| Tabs | Shows TL;DR | Shows TL;DR | ✓ Interactive | ✓ Interactive | Shows TL;DR | Shows TL;DR |
| Split Card | VML bg | ✓ CSS bg | ✓ CSS bg | ✓ CSS bg | ✓ CSS bg | ✓ CSS bg |

---

## Quick Copy/Paste Templates

**Need a quick component?** See `templates/components-library.html` for ready-to-use examples with placeholder content.

**Customizing colors?** All color values are inline - just Find & Replace hex codes.

**Adding your content?** Look for `[EDIT:]` markers in each component.
