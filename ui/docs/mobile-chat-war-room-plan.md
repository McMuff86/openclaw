# Mobile Chat + War Room UX Improvement Plan

## Problem

On narrow screens the top navigation, chat chrome, split sidebar, and message/tool content can stack into the same visual space. The current mobile split-view behavior turns the War Room/sidebar into a fixed full-screen overlay, hiding chat and creating an overloaded layout.

## UX Direction

1. **One clear vertical flow on mobile**
   - Topbar owns its natural height instead of overlaying content.
   - Chat, notices, messages, and compose area stay in a single scroll-safe column.

2. **War Room/sidebar becomes a structured mobile panel**
   - Desktop keeps the horizontal resizable split.
   - Mobile uses a stacked panel below chat instead of a full-screen overlay.
   - The panel is still collapsible via the existing close action and can be vertically resized by the browser where supported.

3. **Reduce visual density**
   - Smaller mobile gaps, bubbles, avatars, tool cards, and status pills.
   - Tool/side content gets bounded heights and internal scrolling instead of pushing the whole UI apart.

4. **Keep controls reachable**
   - Composer remains sticky without covering content.
   - Chat/thread containers keep `min-height: 0` and safe viewport sizing.

## Acceptance Checks

- Mobile topbar no longer overlaps the chat content.
- Opening the War Room/sidebar on mobile does not hide the main chat.
- Desktop split view stays resizable through the divider.
- UI tests and Vite build pass.
