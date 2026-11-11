# Torah Study iOS Client

Native iOS client for the multi-platform Torah independent study app.

## Role

- Pure consumer of the [torah-study-backend](https://github.com/jaywoith/torah-study-backend) API
- Renders daily study, Siddur path, specialized paths, and AI Rabbi Coach
- Uses shared UI strings from the backend for consistent labels
- Contains **no** framework logic, generation rules, or AI prompts

## Related Repositories

| Repo | Purpose |
|------|---------|
| [torah-study-shared](https://github.com/jaywoith/torah-study-shared) | Shared packages + UI strings (source of truth) |
| [torah-study-backend](https://github.com/jaywoith/torah-study-backend) | Backend API (this client talks only to it) |
| [torah-study-web](https://github.com/jaywoith/torah-study-web) | Web client |
| [torah-study-android](https://github.com/jaywoith/torah-study-android) | Android client |

## Drift Prevention

This client never embeds rules or hard-codes shared labels. It only calls backend endpoints and displays the prepared Hebrew, transliteration, English, commentary, kavannah prompts, and UI strings. Changes to content, AI behavior, or shared copy are made in the shared packages and backend.

## Next Steps

- Create Xcode project (SwiftUI recommended)
- Implement networking layer against backend API
- Fetch and cache `/v1/ui-strings`
- Screens for daily study, Siddur path, and Coach
- Support mixed language mode (pointed Hebrew + transliteration + English)

See [shared-vs-local best practice](https://github.com/jaywoith/torah-study-shared/blob/main/docs/shared-vs-local.md).
