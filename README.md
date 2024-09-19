# Quixel Auto Asset Claimer Script

## Description
This script automates the process of claiming all free assets on the Quixel website. It retrieves all available free assets using Quixel's API, checks for assets already owned by the user, and claims any unowned assets.

## How to Use

1. **Copy the Script:**
   Copy the script from the `run.js` file below.

2. **Login:**
   Login to your account at [Quixel](https://quixel.com).

3. **Navigate to Assets:**
   Go to [Quixel Megascans Collections](https://quixel.com/megascans/collections).

4. **Open DevTools:**
   Open your browser’s DevTools (F12 or right-click and select "Inspect"), then go to the "Console" tab.

5. **Paste the Script:**
   Paste the script into the console and press Enter.

6. **Confirm Execution:**
   A dialog should pop up confirming the execution. Click "OK."

7. **Wait:**
   Sit back and wait while the script claims the assets.

## Common Issues

### Getting "Forbidden" Error
- **Issue:** The page shows "Forbidden" error, even after refreshing.
- **Fix:** This might be due to hitting the API rate limit. Wait for 10-20 minutes, refresh the [Quixel website](https://quixel.com), and restart the script.

### Script Seems to be Paused/Hung
- **Issue:** The script might pause or hang due to excessive logging.
- **Fix:** Monitor the script. If it says "END PAGE X", note the page number and clear the console by clicking the "🚫" icon in DevTools. Restart the script after clearing the console.

### Getting the Error **UNABLE TO ADD ITEM**
- **Issue:** The script shows an error message like **UNABLE TO ADD ITEM**.
- **Fix:** If the error indicates that you already own the item at a higher or equal resolution, the item is already in your account.

### Getting the Error **Cannot Find Authentication Token**
- **Issue:** The script cannot find the authentication token.
- **Fix:** Clear your browser cookies, re-login to Quixel, and try adding an item manually. If successful, restart the script.

## Common Fixes

### Restart Script
1. Note the page number where the script encountered an issue.
2. Copy the `run.js` script.
3. Update `startPage = 0` on the first line to `startPage = [last successful page number]` (e.g., `startPage = 10`).
4. Run the updated script to continue from where it left off.

## Change Log

- **Initial Script Launch:** Initial version of the script to automate asset claiming.
- **Update:** Added functionality to clear logs to reduce hanging issues.
- **[CURRENT]**: Skips already acquired items, reduces logs, and provides more information after script completion to show purchased item count. You no longer need to specify the `startPage` unless restarting from a specific page.
