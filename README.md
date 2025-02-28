# Steam tags for Humble Bundle

This repository contains the full source code of the `Steam tags for Humble Bundle` extension for Google Chrome and Mozilla Fiferox, together with backend code handling communication with the Steamworks Web API.

## Download

- Chrome: https://chrome.google.com/webstore/detail/steam-tags-for-humble-bun/fcinjfniedmmfaalakcallcbjepfiabi
- Firefox: https://addons.mozilla.org/en-US/firefox/addon/steam-tags-for-humble-bundle/

## Description

Display "On wishlist" and "In library" tags next to games on various Humble Bundle pages based on your Steam account wishlist and library.

There are 2 ways of using this extension:

- Login to Steam website at https://store.steampowered.com/
- Enter your SteamId or CustomUrl in the extension settings

## Changelog

**v3.1:**

- Updated dependencies to fix new Chrome extension policy issue

**v3.0:**

- The website will remain responsive while the tags are loading
- Improved logging and error handling
- Switched to a new database

**v2.9:**

- Fixed humble site max-width being affected by this extension
- Fixed suggestion form

**v2.8:**

- Fixed popup display issue in Chrome caused by new update

**v2.7:**

- Fixed permissions check to not handle extra permission from previous version as a warning
- Improved cache handling so outdated cache from previous version won't break the extension

**v2.6:**

- Added missing permissions warning
- Fixed broken Firefox build
- Fixed other Firefox inconsistencies

**v2.5:**

- Tags that were found in your library/wishlist/ignore now link directly to steam store page of the game
- Merge both store and steamId info when available
- Properly update version number in About section

**v2.4:**

- Fixed wishlist for steam account login
- Handle coupons
- Fix some css issues on humble pages

**v2.3:**

- Added option to show a steam tag next to all items

**v2.2:**

- Fix mappings related bug that broke core functionality

**v2.1:**

- Fixed problem with steam store data returning empty cached value
- Fixed adding of tags to new items not present on first page load
- Added tags to store product detail page
- Added report missing tag form

**v2.0:**

- Migrated to manifest v3
- Replaced broken heroku backend with vercel edge functions
- Refactored to vite + typescript + react + tailwind
- Polished interface

**v1.5:**

- Updated to work on new `/membership` pages of humble choice
- Added option to log out and choose whether to log in with steam id or through store.steampowered.com

**v1.4:**

- Added indicator that user is logged in through store.steampowered.com
- Fixed error with loading library info by user steam id/url
- Fixed saved data info not updating in extension settings immediately after refresh

**v1.3:**

- Fixed a bug where cached ignored games would get reset
- Created a Firefox version of this extension
- Removed unnecessary `activeTab` permission

**v1.2:**

- DLCs will show up correctly (only if logged in on Steam website)
- Added `Ignored` tag that also lowers opacity of given item just like on Steam (only if logged in on Steam website)
- Game info is automatically retrieved after you change extension settings
- SteamId and CustomUrl input now also accepts the full profile url

**v1.1:**

- Added tags to `Library` and `Keys & Entitlements` pages
- Improved game name matching (to better match items with suffixes like `(Steam)` or `XYZ edition`))
- Added link to steam store with hover effect for tags
