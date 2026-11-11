# Client Principles

All clients (web, iOS, Android) follow the same rules:

1. Call only the backend API.
2. Never hard-code framework, level, or AI behavior.
3. Render the structured study units returned by the backend.
4. Use shared UI strings from the backend (`GET /v1/ui-strings`) for any label that must match across platforms.
5. Support the four language modes by displaying the fields the backend already prepared.

Source of truth: [torah-study-shared](https://github.com/jaywoith/torah-study-shared)  
Runtime: [torah-study-backend](https://github.com/jaywoith/torah-study-backend)  
Best practice split: [shared-vs-local](https://github.com/jaywoith/torah-study-shared/blob/main/docs/shared-vs-local.md)
