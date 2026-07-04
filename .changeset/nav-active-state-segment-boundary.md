---
"blume": patch
---

Fix navigation active states matching on raw string prefixes instead of path segments. With tabs at `/api` and `/api-reference`, visiting `/api-reference` highlighted both — `route.startsWith(tab.path)` treated the sibling section as a child. The header tab bar, the mobile drawers in `RootLayout` and `PageLayout`, and the nav selector's active item now all match only at segment boundaries (the section root itself or routes nested beneath it).
