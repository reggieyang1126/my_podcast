# My Podcast RSS Feeds

A minimal GitHub repository for hosting custom podcast RSS feeds using Google Drive audio links. Perfect for personal podcasts, educational content, or niche topics.

## 🎯 Quick Start

1. **Fork this repository** or use it as a template
2. **Replace placeholders** in the RSS feeds with your content
3. **Upload your audio files** to Google Drive and get direct download links
4. **Enable GitHub Pages** to make your feeds publicly accessible
5. **Submit to podcast directories** using your RSS feed URLs

## 📁 Repository Structure

```
my_podcast/
├── feeds/
│   ├── health/
│   │   └── feed.xml          # Health & Wellness podcast
│   ├── finance/
│   │   └── feed.xml          # Personal Finance podcast
│   └── template.xml          # Template for creating new topics
└── README.md
```

## 🚀 Setting Up Your Podcast

### Step 1: Get Google Drive Direct Download Links

Google Drive sharing links won't work directly in RSS feeds. You need **direct download links**:

1. **Upload your MP3 file** to Google Drive
2. **Right-click** the file → **Get link**
3. **Change permissions** to "Anyone with the link can view"
4. **Copy the file ID** from the sharing URL:
   ```
   https://drive.google.com/file/d/1BxiMVs0XRA5nFMdKvBdBZjgmUUqptlWS/view
                                    ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
                                    This is your file ID
   ```
5. **Create the direct download URL**:
   ```
   https://drive.google.com/uc?export=download&id=YOUR_FILE_ID
   ```

### Step 2: Update RSS Feed Files

#### For Existing Topics (Health/Finance):
1. Open `feeds/health/feed.xml` or `feeds/finance/feed.xml`
2. Replace these placeholders:
   - `yourusername` → Your GitHub username
   - `your-email@example.com` → Your email address
   - `Your Name` → Your actual name
   - `YOUR_GOOGLE_DRIVE_FILE_ID_*` → Your Google Drive file IDs
   - Episode titles, descriptions, and dates

#### For New Topics:
1. **Create a new folder**: `feeds/your-topic-name/`
2. **Copy the template**: `cp feeds/template.xml feeds/your-topic-name/feed.xml`
3. **Edit the new feed** following the detailed comments in the template
4. **Replace all placeholders** marked with `YOUR_*`

### Step 3: Enable GitHub Pages

1. Go to your repository **Settings** → **Pages**
2. Set **Source** to "Deploy from a branch"
3. Choose **Branch**: `main` and **Folder**: `/ (root)`
4. Click **Save**

Your feeds will be available at:
- `https://reggieyang1126.github.io/my_podcast/feeds/health/feed.xml`
- `https://reggieyang1126.github.io/my_podcast/feeds/finance/feed.xml`

## 📱 Adding to Podcast Apps

### Apple Podcasts (iOS)
1. Open the **Podcasts** app
2. Tap **Library** → **Edit** → **Add Show by URL**
3. Enter your RSS feed URL: `https://reggieyang1126.github.io/my_podcast/feeds/health/feed.xml`
4. Tap **Subscribe**

### Spotify
1. Go to [Spotify for Podcasters](https://podcasters.spotify.com/)
2. Sign in and click **Get Started**
3. Enter your RSS feed URL
4. Follow the verification process

### Google Podcasts
1. Visit [Google Podcasts Manager](https://podcastsmanager.google.com/)
2. Click **Add Podcast**
3. Enter your RSS feed URL
4. Complete the verification

### Other Apps
Most podcast apps support adding shows by RSS URL:
- **Overcast**: Settings → Add URL
- **Pocket Casts**: Discover → Search → Enter URL
- **Castro**: Search → Add URL

## 🔧 Customization Tips

### RSS Feed Best Practices
- **Keep GUIDs unique** for each episode
- **Use proper date formats**: `Mon, 01 Jan 2024 09:00:00 +0000`
- **Include episode duration** in `MM:SS` or `HH:MM:SS` format
- **Add episode artwork** for better visual appeal
- **Write descriptive summaries** for better discoverability

### Audio File Recommendations
- **Format**: MP3 (most compatible)
- **Bitrate**: 128 kbps (good balance of quality/size)
- **Sample Rate**: 44.1 kHz
- **Channels**: Mono for speech, Stereo for music

### Google Drive Limits
- **Individual file limit**: 100 MB for direct download
- **Daily download limit**: ~750 MB per day for free accounts
- **For larger files**: Consider splitting into parts or using paid storage

## 🛠️ Troubleshooting

### Common Issues

**❌ "Feed not found" error**
- Check if GitHub Pages is enabled
- Verify the RSS feed URL is correct
- Ensure the XML file is valid (no syntax errors)

**❌ "Can't play audio" error**
- Verify Google Drive file permissions are set to "Anyone with the link"
- Check if the file ID in the RSS feed is correct
- Test the direct download URL in a browser

**❌ Episodes not updating**
- Update the `<lastBuildDate>` in your RSS feed
- Wait 24-48 hours for podcast apps to refresh
- Force refresh in your podcast app if available

### Testing Your Feed

1. **Validate RSS**: Use [Feed Validator](https://validator.w3.org/feed/)
2. **Test in browser**: Open your RSS URL directly
3. **Check audio links**: Click the Google Drive URLs to ensure they download

## 📚 RSS Feed Reference

### Required Elements
```xml
<channel>
  <title>Your Podcast Title</title>
  <description>Podcast description</description>
  <language>en-us</language>
  <item>
    <title>Episode Title</title>
    <description>Episode description</description>
    <enclosure url="..." length="..." type="audio/mpeg"/>
    <guid>unique-episode-id</guid>
    <pubDate>Date in RFC 2822 format</pubDate>
  </item>
</channel>
```

### iTunes Extensions
```xml
<itunes:author>Your Name</itunes:author>
<itunes:category text="Technology"/>
<itunes:image href="podcast-artwork-url"/>
<itunes:duration>MM:SS</itunes:duration>
<itunes:explicit>no</itunes:explicit>
```

## 🤝 Contributing

Found an issue or have a suggestion? Please:
1. Check existing issues first
2. Create a new issue with details
3. Submit a pull request if you have a fix

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 💡 Tips for Success

- **Consistent posting schedule** helps build audience
- **Quality audio** is more important than perfect content
- **Engage with your audience** through descriptions and social media
- **Cross-promote** your episodes on different platforms
- **Keep episodes focused** on your chosen topic

---

**Ready to start podcasting?** Fork this repo and start sharing your voice with the world! 🎙️
