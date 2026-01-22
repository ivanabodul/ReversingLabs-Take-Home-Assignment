# Z1000 changelog
## V8.1.0
January 2026
## New features
- Z1000 now tracks all analyzed email senders and assigns them a reputation score from 0–100 based on their email history. Higher scores with values near 100 indicate that the sender has a clean email history, and lower scores with values near 0 indicate that the sender's emails frequently contained malicious attachments. [Feature.ref.code]
- Added the `api/v1/sender_reputation/` endpoint that allows users to query email sender reputation scores. The API can query individual sender email addresses (for example, `user@example.com`) or all senders from a specific domain (for example, `https://example.com`). [Feature.ref.code]
## Bug fixes
- Fixed a memory leak in the email parsing module that caused increased RAM usage and required system restarts after processing approximately 50,000 emails. [Bug.ref.code]
- Resolved displaying false positives where legitimate encrypted ZIP files were incorrectly flagged as suspicious. [Bug.ref.code]
- Fixed a system crash caused by non-ASCII characters in attachment filenames (for example, `invoice_café.pdf`). [Bug.ref.code]
