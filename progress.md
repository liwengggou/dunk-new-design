## [2025-09-15 | 03:04 UTC]
**Task:** Remove unused Python files for static export.
**Summary:**
- Stopped the local Python HTTP server.
- Deleted server.py (dev static server with range support) and optimize_assets.py (one-off asset optimizer/manifest generator).
- Site is a static bundle (HTML/CSS/JS + assets). Runtime features do not depend on Python; only the fetch to assets/university_logos.json must be served by any static host.
**Next Steps:**
- Ensure hosting environment serves assets/ and supports client-side fetch of JSON from the same origin.
- If you need to regenerate the logos manifest in the future, recreate a similar script or restore optimize_assets.py from version control/backups.

