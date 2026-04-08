# Release notes — 0.0.39

Release date: 25-Mar-2026 

## English
- History swipe-to-delete is now more reliable, so entries remove consistently after a full swipe.
- Library loading errors are clearer and more specific, with localized messages for common network and server problems.
- Improved screen reader support across playback controls, search, menus, artwork, bookmarks, and track selection.
- More of the interface is now translated, with clearer wording in playback, sleep timer, search, folder details, and delete feedback.
- Scrolling is smoother and lists feel more responsive, especially while download progress is updating.
- Improved cover image handling for the Akniga source for more reliable artwork loading.

### Behavior changes
- Swiping a History item far enough now deletes it immediately instead of sometimes snapping back.
- Library errors now show specific causes like timeout, forbidden access, page not found, DNS, SSL/TLS, and general network failures.
- Akniga artwork now uses the source’s original cover URLs, which may slightly change how some covers appear but should reduce broken artwork.

### BREAKING CHANGES
- None

### Risks / What to test
- Swipe-delete several History items and confirm they disappear consistently after the threshold is passed.
- Verify library error screens for offline mode, timeout, forbidden or missing pages, and retry flow.
- Check TalkBack or another screen reader on player controls, search, track picker, bookmarks, and menu buttons.
- Browse Akniga listings and book pages to confirm cover art loads correctly.
- Scroll large library and history lists during active downloads and confirm smooth progress updates.

