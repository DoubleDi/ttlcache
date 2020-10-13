# 2.1.0 (October 2020)

## API changes

* `SetCacheSizeLimit(limit int)` a call  was contributed to set a cache limit. #35

# 2.0.0 (July 2020)

## Fixes #29, #30, #31

## Behavioural changes

* `Remove(key)` now also calls the expiration callback when it's set
* `Count()` returns zero when the cache is closed

## API changes

* `SetLoaderFunction` allows you to provide a function to retrieve data on missing cache keys.
* Operations that affect item behaviour such as `Close`, `Set`, `SetWithTTL`, `Get`, `Remove`, `Purge` now return an error with standard errors `ErrClosed` an `ErrNotFound` instead of a bool or nothing
* `SkipTTLExtensionOnHit` replaces `SkipTtlExtensionOnHit` to satisfy golint
* The callback types are now exported
