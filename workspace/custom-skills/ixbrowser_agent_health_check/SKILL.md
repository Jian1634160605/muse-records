# Check the ixBrowser agent before a round and escalate a long outage

## Check liveness before every round

- Check the ixBrowser agent health endpoint before any publish, hunt, DM, or group watch round that needs the agent.

- Check both the agent port and the Concat bridge port, and treat the agent as down when either health check does not answer.

- Run the check close to the round start, and do not reuse a health result from an earlier round as proof the agent is still up.

- Treat a single failed health check as unverified, and retry the check once after a short wait before you call the agent dead.

- Record the time of the check and which ports answered, so a later round can see whether the outage is new or continuing.

## Skip the round when the agent is dead

- Skip the browser steps of the round when the agent is dead, and do not open profiles or attempt publishes through it.

- Keep the round items in their queue, and carry them forward to the next live round instead of marking them failed or done.

- Do not report an account as broken, locked, or out of content when the only evidence is a dead agent.

- Write a skip log entry with the round name, the time, and the health result, so the missed round is visible in the next review.

- Report the missed items as carried forward with their counts, and do not claim a publish count for items that never ran.

## Escalate a prolonged outage once

- Report the outage at once through the blocking escalation route when the first round finds the agent dead.

- Ask the user for one restart of the agent service, and name the exact service and the health result that shows it is down.

- Group later rounds under the same open outage, and report only the new failure time and the carried item count instead of asking for another restart each round.

- Escalate again only when the outage passes twelve hours without recovery, and then name the duration, the rounds skipped, and the items still carried forward.

- Stop asking for restarts after the user has already been asked and the agent is still down, and wait for the user or the engineer to report the restart result.

## Do not switch to the backup agent alone

- Treat the alternate agent service as untested for live operation until the user or the engineer approves the switch.

- Surface the backup as an option in the prolonged outage report, and state that it needs a token decision before use.

- Leave the switch decision to the user or the engineer, and keep using the primary agent path once it recovers.

- Never print an agent token, a proxy value, or a raw status response while you check health or report an outage.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Run the check again at the next scheduled round when a short outage clears on its own, since earlier outages have recovered without a restart.

- Ask the user for help only when the health check, the short wait retry, and the restart request have all failed for the same outage.
