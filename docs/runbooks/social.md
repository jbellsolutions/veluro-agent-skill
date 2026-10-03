# Social Media Manager and autopilot

**Route:** `/social` · [Open Veluro](https://veluro.ai/social)

**When:** Use to prepare and publish an approved social content calendar.

**Prerequisites:** Correct profiles/pages, brand assets, approved content and schedule/timezone.

## Agent procedure

1. Check each platform connection and current approval gates.
2. Create a manual post or generate a strategy/batch for review.
3. Inspect text, links, hashtags and finished image/video for each platform.
4. Save drafts or approve/schedule within the agreed publishing scope.
5. Verify provider publication and calendar state; reconcile before retrying failures.
6. Configure autopilot only with explicit content, frequency and spending limits.

## Success and recovery

Completion proof: Posts appear on the intended profile at the intended time with correct content.

Dragging a post can reschedule it. Autopilot can create and publish content; general Meta approval remains gated.

If loading or a request fails, inspect connection and quota state, then retry safe reads with bounded backoff. Reconcile existing object/job state before any repeated write. Preserve completed work and record the exact unresolved dependency. Consult the central verification register for the feature’s current evidence level.

## Observed controls and fields

2 captured screen states; 42 distinct controls/fields below. These are live UI observations, not a complete backend validation schema. A disabled state is the captured account state, not necessarily a universal restriction.

| Control / field | Locator | Type / role | Placeholder or options / constraints | Captured disabled |
|---|---|---|---|---|
| Autopilot | data-testid=autopilot-btn | BUTTON |  | False |
| Facebook Pages | data-testid=facebook-publish-btn | BUTTON |  | False |
| Instagram | data-testid=instagram-publish-btn | BUTTON |  | False |
| LinkedIn | data-testid=linkedin-publish-btn | BUTTON |  | False |
| TikTok | data-testid=tiktok-publish-btn | BUTTON |  | False |
| AI Week Queue | data-testid=generate-queue-btn | BUTTON |  | False |
| Create Post | data-testid=create-post-btn | BUTTON |  | False |
| Input / icon | data-testid=sm-website-input | INPUT | yourbusiness.com | False |
| Build my strategy | data-testid=sm-analyze-btn | BUTTON |  | False |
| Connect FB Page | data-testid=facebook-publish-btn | BUTTON |  | False |
| Connect Instagram | data-testid=instagram-publish-btn | BUTTON |  | False |
| Connect LinkedIn | data-testid=linkedin-publish-btn | BUTTON |  | False |
| Connect TikTok | data-testid=tiktok-publish-btn | BUTTON |  | False |
| Facebook | data-testid=platform-facebook | BUTTON |  | False |
| Instagram | data-testid=platform-instagram | BUTTON |  | False |
| LinkedIn | data-testid=platform-linkedin | BUTTON |  | False |
| TikTok | data-testid=platform-tiktok | BUTTON |  | False |
| Serious | data-testid=tone-serious | BUTTON |  | False |
| Educational | data-testid=tone-educational | BUTTON |  | False |
| Promotional | data-testid=tone-promotional | BUTTON |  | False |
| Edgy | data-testid=tone-edgy | BUTTON |  | False |
| Funny | data-testid=tone-funny | BUTTON |  | False |
| Inspirational | data-testid=tone-inspirational | BUTTON |  | False |
| Input / icon | data-testid=post-topic-input | text | e.g. New product launch, behind-the-scenes, industry tips... | False |
| AI Generate | data-testid=generate-content-btn | BUTTON |  | False |
| Generate from a website URL | data-testid=url-brief-open | button |  | False |
| Input / icon | data-testid=post-content-textarea | TEXTAREA | Write your post or let AI generate it... | False |
| Input / icon | data-testid=image-prompt-input | text | Describe the image you want... | False |
| Write prompt | data-testid=image-write-prompt-btn | button |  | False |
| Generate | data-testid=generate-image-btn | BUTTON |  | False |
| Pick Image | data-testid=post-pick-image-open | button |  | False |
| From Studio | data-testid=studio-picker-image-open | button |  | False |
| Input / icon | data-testid=video-prompt-input | text | Describe the video you want to create... | False |
| Write prompt | data-testid=video-write-prompt-btn | button |  | False |
| Generate | data-testid=generate-video-btn | BUTTON |  | False |
| Pick Video | data-testid=post-pick-video-open | button |  | False |
| From Studio | data-testid=studio-picker-video-open | button |  | False |
| Input / icon | data-testid=schedule-date | date |  | False |
| Input / icon | data-testid=schedule-time | time |  | False |
| Cancel | Use observed accessible label/placeholder | BUTTON |  | False |
| Save Draft | data-testid=save-draft-btn | BUTTON |  | False |
| Schedule Post | data-testid=schedule-post-btn | BUTTON |  | False |

## Related API call shapes

All paths below are relative to `/api`. These are **source observed**, except where the API guide records a test. Read the request shape and effect classification before use. Do not copy dynamic placeholders into a request.

| Method | Path template | Effect | Reference |
|---|---|---|---|
| GET | `/linkedin/posting/posts` | read candidate; inspect endpoint side effects | api-0356 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/linkedin/posting/publish` | delivery / publishing / provider or workflow change | api-0357 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/linkedin/posting/status` | read candidate; inspect endpoint side effects | api-0358 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/ai-caption` | generation / analysis; may consume credits or store output | api-0374 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/analytics` | read candidate; inspect endpoint side effects | api-0375 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/analytics/recommendations` | generation / analysis; may consume credits or store output | api-0376 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/connected` | read candidate; inspect endpoint side effects | api-0377 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/instagram/account` | read candidate; inspect endpoint side effects | api-0378 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/instagram/posts` | read candidate; inspect endpoint side effects | api-0379 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/instagram/publish` | delivery / publishing / provider or workflow change | api-0380 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/instagram/schedule` | create / edit / configuration; inspect before execution | api-0381 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/instagram/scheduled` | read candidate; inspect endpoint side effects | api-0382 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/meta/pages/instagram/scheduled/{parameter_1}` | delete / remove | api-0383 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PATCH | `/meta/pages/instagram/scheduled/{parameter_1}` | create / edit / configuration; inspect before execution | api-0384 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/profiles` | read candidate; inspect endpoint side effects | api-0385 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/profiles` | create / edit / configuration; inspect before execution | api-0386 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/publish` | delivery / publishing / provider or workflow change | api-0387 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/published` | read candidate; inspect endpoint side effects | api-0388 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/published/{parameter_1}/refresh` | delivery / publishing / provider or workflow change | api-0389 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/schedule` | create / edit / configuration; inspect before execution | api-0390 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/scheduled` | read candidate; inspect endpoint side effects | api-0391 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/meta/pages/scheduled/{parameter_1}` | delete / remove | api-0392 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PATCH | `/meta/pages/scheduled/{parameter_1}` | create / edit / configuration; inspect before execution | api-0393 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/subscribe-webhook` | create / edit / configuration; inspect before execution | api-0394 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/meta/pages/sync-leads` | delivery / publishing / provider or workflow change | api-0395 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/meta/pages/webhook-events` | read candidate; inspect endpoint side effects | api-0396 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social-manager/analyze` | generation / analysis; may consume credits or store output | api-0557 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social-manager/approve-schedule` | delivery / publishing / provider or workflow change | api-0558 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social-manager/best-times` | read candidate; inspect endpoint side effects | api-0559 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social-manager/generate-batch` | generation / analysis; may consume credits or store output | api-0560 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social-manager/jobs/{parameter_1}` | read candidate; inspect endpoint side effects | api-0561 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social-manager/learnings` | read candidate; inspect endpoint side effects | api-0562 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social-manager/plan` | read candidate; inspect endpoint side effects | api-0563 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social-stats/overview` | read candidate; inspect endpoint side effects | api-0564 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social/autopilot` | read candidate; inspect endpoint side effects | api-0565 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/social/autopilot` | create / edit / configuration; inspect before execution | api-0566 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social/platform-status` | read candidate; inspect endpoint side effects | api-0567 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social/posts` | read candidate; inspect endpoint side effects | api-0568 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social/posts` | create / edit / configuration; inspect before execution | api-0569 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social/posts/generate` | generation / analysis; may consume credits or store output | api-0570 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social/posts/generate-image` | generation / analysis; may consume credits or store output | api-0571 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social/posts/generate-video` | generation / analysis; may consume credits or store output | api-0572 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/social/posts/video-status/{parameter_1}` | read candidate; inspect endpoint side effects | api-0573 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/social/posts/{parameter_1}` | delete / remove | api-0574 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PUT | `/social/posts/{parameter_1}` | create / edit / configuration; inspect before execution | api-0575 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social/posts/{parameter_1}/approve` | delivery / publishing / provider or workflow change | api-0576 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social/posts/{parameter_1}/publish` | delivery / publishing / provider or workflow change | api-0577 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/social/queue/generate` | generation / analysis; may consume credits or store output | api-0578 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/tiktok/posting/creator-info` | read candidate; inspect endpoint side effects | api-0611 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/tiktok/posting/disconnect` | account / access / configuration change | api-0612 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/tiktok/posting/posts` | read candidate; inspect endpoint side effects | api-0613 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/tiktok/posting/publish` | delivery / publishing / provider or workflow change | api-0614 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/tiktok/posting/publish-photo` | delivery / publishing / provider or workflow change | api-0615 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/tiktok/posting/publish-status/{parameter_1}` | read candidate; inspect endpoint side effects | api-0616 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/tiktok/posting/schedule` | create / edit / configuration; inspect before execution | api-0617 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/tiktok/posting/scheduled` | read candidate; inspect endpoint side effects | api-0618 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| DELETE | `/tiktok/posting/scheduled/{parameter_1}` | delete / remove | api-0619 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| PATCH | `/tiktok/posting/scheduled/{parameter_1}` | create / edit / configuration; inspect before execution | api-0620 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| GET | `/tiktok/posting/status` | read candidate; inspect endpoint side effects | api-0621 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/tiktok/posting/suggest-caption` | generation / analysis; may consume credits or store output | api-0622 in [API catalog](../api/ENDPOINT_CATALOG.md) |
| POST | `/tiktok/posting/upload-draft` | generation / analysis; may consume credits or store output | api-0623 in [API catalog](../api/ENDPOINT_CATALOG.md) |

## Evidence references

- `ui-batch-05.json` — /social · 2026-09-08T17:04:11.520Z
- `dialogs-01.json` — Create Post · 2026-09-08T17:12:54.209Z

Source-call evidence: `evidence/api-source-calls.json`. Exact raw screen text and controls are retained in `evidence/screen-index.json`. UI label inventories do not validate generated outputs or external side effects.
