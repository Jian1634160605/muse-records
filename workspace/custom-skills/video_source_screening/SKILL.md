# Screen Video Sources Before Editing

Run this gate on every candidate clip before it enters the edit. It catches bad sources. The editing workflow's own acceptance check catches build errors. Both have to pass.

## Confirm the footage is yours to use

- Verify the account is company-owned or explicitly licensed for reuse before selecting any clip from a third-party account. Follower count and style similarity say nothing about ownership.

- Study structure only from a non-company account: shot order, hooks, text overlay placement. Never download, re-edit, or publish its footage.

- Confirm company library material is not marked no-publish before it enters the candidate set, and apply any required eye mosaic first.

- Keep the allowlist of usable source accounts in the project workspace notes and check every new candidate against it. Treat an account of unclear ownership as non-company until verified.

## Screen every candidate clip

- Check identity consistency: one finished video follows one person through one case. Reject the mix when two different faces appear unless you can confirm they are the same patient.

- Check frame integrity: open the first, middle, and last seconds of the clip plus every text overlay. Confirm no banner text is cut off at the frame edge and no frame is torn or frozen mid-motion.

- Check watermark residue: look for another creator's handle, logo, or platform watermark burned into the frame, including faint marks hiding under your own overlay. Reject clips you cannot clean without degrading the picture.

- Never let view count override a failed check. A high-view clip that fails screening stays a structure reference, never a source.

## Log rejections and report

- Record each rejected candidate in the prep log with its path and the reason, so the next round does not reselect it.

- Tell the user which high-view candidates were rejected and why, in one short list, before the edit begins.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Websites

- [Company material library](https://material-library-dashboard.zhouwenjun.meihehe.cn/) for pulling company-owned case footage. Carry the case path into the download endpoint and verify the case is not marked no-publish before use.

## Alternatives for better results

- Fall back to company-owned material or freshly shot footage when no candidate passes screening, instead of shipping a defective clip. Ask the user for the missing footage early rather than quietly lowering the bar.
