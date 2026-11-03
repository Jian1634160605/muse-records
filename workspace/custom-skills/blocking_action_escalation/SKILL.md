# Report blocking problems at once

## Recognize a blocking event

- Treat an approval request, a login or verification challenge, a platform limit, and any failure that stops a scheduled task as a blocking event.

- Treat a short wait threshold for user action as the trigger itself. Notify when the threshold passes without action and never wait for the job to time out or for the next report round.

- Treat a timed out browser or tool task as unverified, not as sent or done. Report the timeout as the problem and keep the work unconfirmed until a server side or tool side check proves it.

## Notify at once in both channels

- Report the blocking event in the main chat at once, in the same turn that you detect it.

- Send the same report through the out-of-band channel the user has designated for urgent help, in the same turn. Do not choose a new channel and do not wait for the user to notice the main chat.

- Repeat the report only if the block is still open at the next scheduled round and the user has not yet acted. Do not batch open blocks into a daily summary.

## Say the four facts

- Name the platform or service that blocked the work.

- Name the account or task that hit the block.

- State what happened in plain language and what evidence shows it.

- State clearly whether the user must act and exactly what action you need, or state that no user action is needed and you are handling it.

## Propagate the rule to every task

- When you learn a new escalation rule or threshold, copy it into every active task body that can hit the same kind of block in the same turn.

- Check scheduled tasks, background workers, and hunter style tasks, not only the task where the rule first appeared.

- Re-read the updated task body before the next run to confirm the rule is present in each place that needs it.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- If the designated out-of-band channel is unavailable, keep the main chat report and record that the second channel failed, then retry the second channel at the next round.

- If the user has not designated an out-of-band channel, ask for one before the next blocking event instead of assuming a channel.

- If a block repeats for the same account, group the repeat under the open block instead of opening a new thread, but still report each new failure time.
