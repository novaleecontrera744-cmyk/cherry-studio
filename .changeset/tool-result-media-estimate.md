---
'@cherrystudio/ai-core': patch
---

Count media carried inside tool results in the context estimate. `fromAISDK` and `fromModelMessages` now project each image or file in a tool-result `content` output (and in an inline provider-executed result) into `attachments`, so `estimateMessages` prices screenshots on native tool-image routes instead of treating them as free, and the `onBeforeCompress` budget guard no longer lets an over-budget screenshot history through.
