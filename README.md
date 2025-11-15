# Responsive Email Signature Template

A modern, responsive email signature template in HTML designed for personal branding. Features include remote-hosted icons from Icons8 and GitHub, support for 11+ social platforms, and automatic scaling for desktop and mobile displays. The signature maintains even distribution across rows and adapts beautifully to any screen size.

![Email Signature Example](example.png)

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Customization](#customization)
- [Adding New Social Links](#adding-new-social-links)
- [Files Included](#files-included)
- [License](#license)

---

## Features

- ✅ **Two Versions**: Desktop (`signature.html`) and Mobile (`mobile_signature`) with device-specific messaging
- ✅ **11 Social Platforms**: YouTube, Twitch, TikTok, Kick, Mastodon, Bluesky, Threads, GitHub, Discord, Matrix
- ✅ **Remote Icons**: Uses Icons8 CDN for reliability and GitHub raw URLs for custom icons
- ✅ **Auto-scaling Layout**: Links wrap naturally at ~5 per row for optimal distribution
- ✅ **Responsive Design**: Media queries adjust sizing for mobile screens (≤480px)
- ✅ **Even Spacing**: Consistent margins and separators maintain visual balance
- ✅ **Profile Image**: Circular profile photo that scales from 80px to 60px on mobile

---

## Installation

1. Clone this repository or download the HTML files directly:
   ```bash
   git clone https://github.com/ChiefGyk3D/email_signature.git
   ```

2. Open either `signature.html` (desktop) or `mobile_signature` (mobile) in any code editor.

---

## Usage

### For Desktop Email Clients:
1. Open `signature.html` in a browser or code editor
2. Select all code (Ctrl+A / Cmd+A)
3. Copy the HTML code
4. Go to your email client's signature settings
5. Paste into the HTML signature editor
6. Save and test by sending yourself an email

### For Mobile Email Clients:
1. Use `mobile_signature` which includes "Sent from Mobile, apologies for any typos" message
2. Follow the same steps as desktop version

> **Note**: Some email clients (Gmail, Outlook) may strip certain CSS. Always test your signature after installation.

---

## Customization

### Profile Image
Replace the profile image URL with your own:
\`\`\`html
<img class="profile-img"
     src="https://your-cdn.com/your-avatar.png" 
     alt="Your Name" 
     style="border-radius: 50%; width: 80px; height: 80px; display: block; margin: 0 auto;" />
\`\`\`

### Personal Text
Update the greeting and name:
\`\`\`html
<p style="margin: 0; font-size: 1.2em; font-weight: bold; color: #000000;">
  Your Greeting,
</p>
<p style="margin: 0; font-size: 1em; color: #000000;">
  Your Name
</p>
\`\`\`

### Social Links
Update each link's \`href\` to point to your profiles:
\`\`\`html
<a href="https://youtube.com/@yourhandle" style="text-decoration: none; color: #000000;">
  <img src="https://img.icons8.com/color/20/000000/youtube-play.png" alt="YouTube Icon" width="20" height="20" /> YouTube
</a>
\`\`\`

### Bottom Links
Customize the two footer links:
\`\`\`html
<a href="https://your-link-site.com">More Ways to Connect</a>
<a href="https://your-mediakit.com">Collaboration Info</a>
\`\`\`

---

## Adding New Social Links

### Using Icons8 (Recommended)
1. Visit [Icons8](https://icons8.com) and search for your platform
2. Get the CDN URL in 20x20 size: \`https://img.icons8.com/color/20/platform-name.png\`
3. Add the new link following this pattern:
   \`\`\`html
   <span style="white-space: nowrap; display: inline-block; margin: 0 3px;">
     <a href="https://platform.com/yourprofile" style="text-decoration: none; color: #000000; display: inline-flex; align-items: center; vertical-align: middle;">
       <img src="https://img.icons8.com/color/20/platform.png" alt="Platform Icon" width="20" height="20" style="vertical-align: middle; margin-right: 3px;" /> Platform
     </a>
   </span>
   <span style="color: #ccc; margin: 0 2px;">|</span>
   \`\`\`

### Using Custom Icons
1. Add your 20x20 PNG icon to the \`icons/\` folder
2. Push to GitHub and get the raw URL: \`https://raw.githubusercontent.com/yourusername/email_signature/main/icons/youricon.png\`
3. Use the same HTML pattern as above with your custom URL

### Layout Notes
- Links automatically wrap at approximately 5 per row
- The 11th link will create a third row automatically
- No manual line breaks needed - the layout handles distribution

---

## Files Included

- \`signature.html\` - Desktop email signature
- \`mobile_signature\` - Mobile email signature with "Sent from Mobile" message
- \`icons/\` - Directory containing custom icons (kick.png, matrix.png, etc.)
- \`example.png\` - Screenshot showing the signature in action
- \`LICENSE\` - MIT License
- \`README.md\` - This file

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## Contributing

Feel free to fork this repository and submit pull requests to add features, improve compatibility, or include additional customization options.

Happy branding!
