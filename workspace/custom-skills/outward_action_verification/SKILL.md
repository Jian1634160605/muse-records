# Verify before an outward action

## Check dedup state before acting

- Read the full dedup record for the round before you post, comment, or message.

- Parse the record as structured data and confirm the target identifier is absent before you act.

- Compare the target by its platform identifier, not by its title or text alone, since similar titles can hide an earlier action.

- Use a targeted lookup only when a full read truncates or the record is too large to parse in one read, and keep the full parse rule for records you can read completely.

- Search the file for the target identifier wrapped in double quotes with a fixed-string search, so the search matches both a bare string entry and a structured entry that carries the same identifier.

- Treat a hit as proof the target was already acted on and skip the round without acting again.

- Treat a miss as permission to act only when the search ran over the whole file and the identifier format matches the entries in the file.

- Stop the round when the search itself fails or the file cannot be searched, and record the failed search and the skipped action for the next round.

- Record the search, the target identifier, and the hit or miss result before you act, so a later round can audit the check without rereading the whole record.

- After a verified outward action, append the new entry through a backup and a temporary file and a verified rename, so a failed append never truncates the live record.

## Check self-cite ownership and the banned list

- Search your own post record for the exact identifier of the post you want to cite before you write the comment or post.

- Read the author field on the matching record and confirm it names your own account.

- Treat a missing record as unproven ownership and do not cite the post as your own.

- Treat a record whose author names another account as a wrong cite and do not use its link.

- Use a targeted quoted identifier search when the record is too large to read in full, and stop when the search cannot prove the author.

- Search your banned cite list for the exact identifier before you use any self-cite link.

- Skip the link when the identifier appears on the banned list, even when the post looks like your own content.

- Add the identifier to the banned list at once when a later check proves a cite was wrong, so the next round does not repeat it.

- Pick a different verified own post when the first choice is banned or unproven, and cite nothing when no verified own post fits.

- Record the cited identifier, the author you found, and the banned list result before you act, so a later round can audit the check without rereading the whole record.

- Send the comment or post only after the ownership check and the banned list check both pass.

- Count misattributed cites in the daily report by the cited identifier and the true author, so a repeated wrong cite is visible as one pattern and not as separate accidents.

## Check same-author frequency before commenting

- Before commenting, check the dedup record for earlier comments on the same author today.

- Treat one comment per author per day as the limit and skip the round when that author already has a comment today.

- Run the frequency check before you post the comment, never after it, and stop the round when the check script errors instead of posting without it.

- Read any ledger note on the target, such as a note that says do not comment again, and treat that note as a skip.

- Record the frequency result with the author and the earlier comment identifiers before you act.

## Stop when the record cannot be proven complete

- Stop the round when the record cannot be proven complete and a targeted lookup cannot prove the target is absent.

- Do not act on a partial list and do not guess that a missing entry means the target is new.

- Fetch every page of a paginated list before you report a count change or a missing item, and never report a loss from a first page alone.

- Record the truncated read, the action you skipped, and the next check you will run, so a later round does not repeat the same guess.

- Re-read the record from the start in a fresh read before the next round, and act only after a complete parse or a clean targeted lookup succeeds.

## Verify a deletion before reporting it gone

- Check the live thread or timeline after a deletion attempt and confirm the item is absent before you report it removed.

- Treat a deletion tool success message as unproven until the live check confirms absence.

- Keep the duplicate visible in your report, with its identifier and the failed deletion attempts, until the live check confirms it is gone.

- Keep a wrong cite in your report with its identifier until a live check proves it is gone, and do not report it as fixed before that check.

- Escalate to a manual browser check in the same round when repeated deletion attempts fail, instead of promising a later check with no owner or time.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Write the comment without a self-cite link when no own post is verified, so the comment still adds value without risking a wrong attribution.

- Write the dedup entry immediately after a verified outward action, so the next round reads a record that already contains it.

- Keep a single dedup record per channel and action type, so two rounds cannot read different lists for the same target.
