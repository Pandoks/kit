---
'@sveltejs/kit': patch
---

fix: persist preload data cache for prerendered routes

`preloadData()` now supports preloading multiple routes simultaneously (closes #12122) and preserves cached data for routes declaring `prerender = true` across client-side navigations. Prerendered `__data.json` is immutable per build, so refreshing it was strictly wasteful. Non-prerendered routes continue to refresh after a navigation consumes their cache entry. Invalidation via `invalidate()` / `invalidateAll()` continues to clear the cache as before.
