# Facebook Reel Publish Verification

This amendment applies on top of the Publish and verify section of Social Publishing when the post is a Facebook Reel.

## Verify with the CLI timeline readback

- Verify a Facebook Reel only with the facebook-cli timeline fetch or post read commands, and treat a matching post in that readback as published.

- Treat an empty Reels tab as no evidence at all, since a published Reel can be absent there while present on the timeline.

- When a publish result is uncertain, run the timeline readback first and publish again only when the readback shows no matching post.

## Back every promised slot with a scheduled job

- List every time slot in the publish plan with the scheduled job that backs it before you promise the slot to the user.

- Treat a slot with no scheduled job as unscheduled, not as a backup, and say so plainly instead of listing it as a round that will run.

- Move items left over from a failed round only into a slot you have just confirmed is backed, and recheck the job list after any plan change.

## Fix a wrong caption by republishing

- Do not use Edit to fix a Reel caption. Delete the Reel and publish it again with the corrected caption, then verify the new copy with the timeline readback before reporting it live.

## Available connectors

- [Facebook](/opt/hatch/connectors/facebook_cli/CONNECTOR.md) for reading timelines and posts and for publishing personal Reels and Page Reels.

- Use muse.connector_search to find other connectors and muse.skill_search to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with Custom Connectors and MCPs, or build a custom connector.

## Alternatives for better results

- Wait for media processing to finish before the readback, so a Reel still processing is not mistaken for a failed publish.
