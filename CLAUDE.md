# SkeetView

A lightweight, single-page web application to view Bluesky posts ("skeets") including quoted content, even when blocked by the original poster.

## Project Structure

```
skeetview/
├── index.html    # Complete application (HTML, CSS, JavaScript)
└── README.md     # User documentation
```

## Tech Stack

- **Pure vanilla JavaScript** - No frameworks or build tools required
- **HTML5/CSS3** - Responsive design with flexbox
- **Bluesky Public API** - REST API for fetching posts

## Key APIs Used

- `com.atproto.identity.resolveHandle` - Convert handles to DIDs
- `app.bsky.feed.getPostThread` - Fetch post threads
- `app.bsky.feed.getPosts` - Fetch individual posts by URI (for blocked quotes)

## Development

No build process needed. Simply open `index.html` in a browser or serve with any static file server.

```bash
# Example: serve locally with Python
python3 -m http.server 8000
```

## Core Functions

- `parseBlueskyUrl()` - Extract handle and post ID from Bluesky URLs
- `resolveHandle()` - Convert user handles to DIDs
- `getPostThread()` / `fetchPostByUri()` - Fetch posts from public API
- `fetchBlockedQuotes()` - Pre-fetch blocked/hidden quoted posts
- `processTextWithFacets()` - Convert text facets to clickable links
- `renderPost()` / `renderEmbed()` - Generate HTML for posts with embeds

## Testing

Open `index.html` in a browser and paste a Bluesky post URL to test. The app supports:
- Standard post URLs: `https://bsky.app/profile/user.bsky.social/post/abc123`
- URLs with query parameters for sharing: `?url=https://bsky.app/...`
