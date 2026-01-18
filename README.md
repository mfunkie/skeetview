# SkeetView

A simple web app to view Bluesky posts including quoted content, even if you're blocked by the poster.

## Why?

Sometimes people quote posts and then block the original poster, making the quoted content invisible to them. SkeetView uses the public Bluesky API to display the full post content including any quotes.

## Usage

1. Open `index.html` in a browser
2. Paste a Bluesky post URL (e.g., `https://bsky.app/profile/user.bsky.social/post/abc123`)
3. Click "View" to see the post and any quoted content

You can also pass a URL as a query parameter: `index.html?url=https://bsky.app/profile/...`

## Features

- Displays post text with proper formatting
- Shows images and external link previews
- Renders quoted posts inline
- Shows engagement stats (replies, reposts, likes)
- Works without authentication using the public API
