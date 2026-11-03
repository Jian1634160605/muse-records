# Protect state files when writing them

## Back up before you write

- Copy the current state file to a backup copy before you change it.

- Keep the backup outside the live record so it cannot be mistaken for the live file.

- Keep the backup until the new version has been verified after the write.

## Write to a temporary file and rename

- Write the new content to a temporary file in the same directory as the live file.

- Replace the live file by renaming the temporary file over it instead of opening the live file for direct overwriting.

- Write only when no other round is writing the same file, and skip the round rather than writing over another writer.

## Verify after the write

- Read the live file back after the write and confirm it is not empty.

- Confirm the read back version parses as the expected structure and holds at least the entries it held before the write, apart from entries you meant to remove.

- Restore the backup at once when verification fails, and report the failed write with the prior version intact.

- Treat an unverified write as unwritten, and do not report its entries as saved.

## Fall back without losing the old version

- Stop using a write tool for that file after it refuses a write with an operation not permitted error.

- Switch to a different file tool such as `muse.edit` or `muse.write` for the next attempt, and still verify the result by reading it back.

- Stop the round when every available write tool has failed, and leave the backup and the prior live version in place for the next round.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Keep a dated copy of the last verified state file in a separate location, so a bad write can be restored even when the local backup is overwritten.

- Split a state file that keeps growing into smaller records by channel or action type, so each write touches less data and each verification stays quick.
