# Verify dedup state before an outward action

## Parse the whole dedup record before acting

- Read the full dedup record for the round before you post, comment, or message.

- Parse the record as structured data and confirm the target identifier is absent before you act.

- Compare the target by its platform identifier, not by its title or text alone, since similar titles can hide an earlier action.

## Check a large record by targeted lookup

- Use a targeted lookup only when a full read truncates or the record is too large to parse in one read, and keep the full parse rule for records you can read completely.

- Search the file for the target identifier wrapped in double quotes with a fixed-string search, so the search matches both a bare string entry and a structured entry that carries the same identifier.

- Treat a hit as proof the target was already acted on and skip the round without acting again.

- Treat a miss as permission to act only when the search ran over the whole file and the identifier format matches the entries in the file.

- Stop the round when the search itself fails or the file cannot be searched, and record the failed search and the skipped action for the next round.

- Record the search, the target identifier, and the hit or miss result before you act, so a later round can audit the check without rereading the whole record.

- After a verified outward action, append the new entry through a backup and a temporary file and a verified rename, so a failed append never truncates the live record.

## Stop when the record cannot be proven complete

- Stop the round when the record cannot be proven complete and a targeted lookup cannot prove the target is absent.

- Do not act on a partial list and do not guess that a missing entry means the target is new.

- Record the truncated read, the action you skipped, and the next check you will run, so a later round does not repeat the same guess.

- Re-read the record from the start in a fresh read before the next round, and act only after a complete parse or a clean targeted lookup succeeds.

## Verify a deletion before reporting it gone

- Check the live thread or timeline after a deletion attempt and confirm the item is absent before you report it removed.

- Treat a deletion tool success message as unproven until the live check confirms absence.

- Keep the duplicate visible in your report, with its identifier and the failed deletion attempts, until the live check confirms it is gone.

- Escalate to a manual browser check in the same round when repeated deletion attempts fail, instead of promising a later check with no owner or time.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Write the dedup entry immediately after a verified outward action, so the next round reads a record that already contains it.

- Keep a single dedup record per channel and action type, so two rounds cannot read different lists for the same target.
