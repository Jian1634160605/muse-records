# Triage a stuck X posting client before retrying

## Recognise an init failure

- Treat a failure that happens while the posting client starts up as a client init failure.

- Record the exact error text and the exit code for every failed attempt.

- Treat an init failure as different from a platform limit unless the error itself names a platform limit code.

- Check the timeline before you judge a round so you know whether the latest post actually changed.

## Stop blind retries after a short run

- Stop scheduled retries after three consecutive failures with the identical init error.

- Hold the queued items in their original order while the client is stuck.

- Create no duplicate draft for a queued item while its first attempt is still held.

- Resume retries only after a diagnosed change has been made and a read only check has passed.

## Diagnose the init inputs one at a time

- Test the proxy line directly against a public site before you blame the proxy line.

- Check the client session and credential state without printing any credential value.

- Compare the last successful post with the first failed post to find what changed in between.

- Change one input at a time and retest with a read only timeline check before you post again.

## Verify the result and report an open block

- Confirm a post only when the timeline shows a new post with a new post id and a changed post count.

- Report a still open init failure in the main chat and in the designated urgent channel in the same turn you stop retries.

- Name the platform and the task in the report.

- State the exact init error and whether the user must act or you are handling the diagnosis.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Ask the user whether a manual post is acceptable while the client is down and record any manual post id so the client does not duplicate it on recovery.

- Pause the retry cadence while the init failure is open instead of letting failed retry jobs pile up.
