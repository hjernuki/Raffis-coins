# Raffi's Authentic Coins — Website

Elegant, user-friendly coin sales landing page and inventory system.

## Features
- Public storefront with categories: Gold, Silver, Copper, Other
- Quantity tracking on both admin (accounting) and public retail side
- Admin: set quantity when adding, edit quantity in the table, totals account for quantity
- Public: shows available quantity, Buy Now / Offer includes quantity selector (capped at available)
- Buy Now and Make an Offer buttons (sends formatted email alert to hjernuki@gmail.com)
- Payment mentions: PayPal, Apple Pay, Venmo
- Phone: 480-688-1100
- **Photo-first Add Coin flow**
  - Take a picture (or upload) of the coin
  - Prompt: enter into retail?
  - Prompt: put into inventory?
  - If entering into retail: prompt for AI description (with instructions to get one from Grok and paste it)
- **Average Sold Price Research**
  - New "Avg Sold" column in inventory
  - Click **Lookup** to open eBay sold listings (last ~90 days) for that coin title
  - Enter the average you observe; it is saved and shown next to your retail/purchase prices
  - Also available when adding or editing a coin
  - Helps compare your pricing to recent market sold prices
- Admin page for inventory management:
  - Upload front & back photos (auto-resized for storage)
  - Enter title, description, purchase price (internal), retail price
  - Tracks profit
  - Export/Import JSON backup of entire inventory **and sales**
- Images stored as compressed base64 in localStorage

## How to Use
1. Open `index.html` in any modern browser (or host the folder on any web host) for the public storefront.
2. For adding coins and recording sales, open `admin.html`.
3. Click **📸 Add Coin from Photo** — take or upload a photo, then follow the prompts for retail / inventory / AI description.
4. To record a sale: click the **Sell** button on a coin, fill in the details, and confirm. Quantity is reduced automatically.
5. Switch to the **Sales History** tab to review all recorded sales.
6. Inventory and sales are stored in the browser's localStorage (persists on the same device/browser).
7. Use the Export button regularly to save a JSON backup of your inventory **and sales**.
8. To generate AI descriptions: when prompted, upload the coin photo to Grok and ask for a professional numismatic description, then paste it into the field.

## Important — Saving Your Work
- Always use the Export All Data button in Admin to download a JSON backup.
- Keep the two HTML files together in the same folder.
- This version is self-contained and does not rely on external servers for the shop itself.
- For email alerts: forms open the user's email client pre-filled so you receive the request at HJErnuki@gmail.com.
- Note: localStorage has size limits. Export regularly and avoid extremely large photo collections. Images are automatically resized.
- Deleting a sale record does **not** restore inventory quantity (you can manually edit quantity if needed).

## Hosting Suggestion
Upload the folder to any static host (Netlify, GitHub Pages, your own server, etc.) for a public URL. The admin page has no password by default — consider adding one or keeping the admin URL private if hosting publicly.

Created for Raffi's Authentic Coins.
