# Quickstart & Verification

## Prerequisites
- Node.js 18+
- npm installed

## Setup
1. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application
1. Start the development server:
   ```bash
   npm run dev
   ```
2. Open http://localhost:3000 in your browser.

## Verification Steps

### 1. Global Dark Theme
- **Check**: The background should be very dark (`#0F1115`).
- **Check**: Text should be white (`#FFFFFF`).
- **Check**: No light mode flicker on refresh.

### 2. Layout Structure
- **Check**: "Anonymous Advice" logo (text) is visible at the top (Header).
- **Check**: Footer with "© 2026 Anonymous Advice..." is visible at the bottom.
- **Check**: Header is sticky (scroll down a long page to verify).
- **Check**: Footer is sticky to bottom on short pages (empty content).

### 3. Responsiveness
- **Check**: Resize window to mobile width. Header/Footer should fit.
- **Check**: Resize to desktop. Content should be readable.
