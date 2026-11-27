# Approval lock and blocking escalation

## Hold outbound sends awaiting approval

- Read the pending approval record for the recipient, thread, or item before you prepare any outbound send.

- Treat a record that names the same recipient, thread, or item as locked even when the draft text differs from the version you would write.

- Skip the send when a lock is present and do not substitute your own wording for the waiting draft.

- Check the record again immediately before sending when any time has passed since your first check.

- Treat a missing or unreadable record as locked for that recipient, thread, or item until you can confirm the approval state another way.

- Create a pending approval record as soon as a draft, reply, or post is put to the user for a decision and note the exact text, the recipient, and the time you asked.

- Keep the lock in place while the user has not replied, while an approval card is still open, and while a timeout has not yet produced an explicit approval.

- Clear the lock only when the user approves that exact text, when the user sends the message themselves, or when the user explicitly cancels the draft.

- Never clear a lock because a new reply arrived, because a scheduled round started, or because a follow up interval elapsed.

- Record each lock, each skip, and each clearance with the time and the reason so a later round can see what happened.

- Treat a new inbound reply as information about the conversation and not as approval to send a waiting draft.

- Read the new reply, update the record, and leave the locked draft untouched when the user has not yet approved it.

- Answer a new reply with a fresh message only when no lock covers that thread and the content is already settled.

- Wait for the user decision when the new reply changes what the waiting draft should say and ask the user to approve the revised text.

- Never use speed, a reply deadline, or a routine trigger as a reason to send past a lock.

- Tell the user in the same round that you skipped a send because of a lock and name the recipient and the reason.

- Keep the waiting draft available for the user to approve, edit, or cancel and do not send it in a later round without that decision.

- Log the skipped send in the thread record so the next worker does not retry it as a fresh send.

- Ask the user for a decision when a lock has stayed open across several rounds and the conversation needs an answer.

## Report blocking problems at once

- Treat an approval request, a login or verification challenge, a platform limit, and any failure that stops a scheduled task as a blocking event.

- Treat a short wait threshold for user action as the trigger itself. Notify when the threshold passes without action and never wait for the job to time out or for the next report round.

- Treat a timed out browser or tool task as unverified, not as sent or done. Report the timeout as the problem and keep the work unconfirmed until a server side or tool side check proves it.

- Report the blocking event in the main chat at once, in the same turn that you detect it.

- Send the same report through the out-of-band channel the user has designated for urgent help, in the same turn. Do not choose a new channel and do not wait for the user to notice the main chat.

- Repeat the report only if the block is still open at the next scheduled round and the user has not yet acted. Do not batch open blocks into a daily summary.

- Name the platform or service that blocked the work.

- Name the account or task that hit the block.

- State what happened in plain language and what evidence shows it.

- State clearly whether the user must act and exactly what action you need, or state that no user action is needed and you are handling it.

## Propagate the rule to every task

- When you learn a new escalation rule or threshold, copy it into every active task body that can hit the same kind of block in the same turn.

- Check scheduled tasks, background workers, and hunter style tasks, not only the task where the rule first appeared.

- Re-read the updated task body before the next run to confirm the rule is present in each place that needs it.

## Available connectors

- [Messenger](/opt/hatch/connectors/messenger_read/CONNECTOR.md) for reading and sending messages in a thread you have already checked for a lock.

- [Facebook](/opt/hatch/connectors/facebook_cli/CONNECTOR.md) for reading posts and comments and for publishing a post only after its exact text is approved.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- If the designated out-of-band channel is unavailable, keep the main chat report and record that the second channel failed, then retry the second channel at the next round.

- If the user has not designated an out-of-band channel, ask for one before the next blocking event instead of assuming a channel.

- If a block repeats for the same account, group the repeat under the open block instead of opening a new thread, but still report each new failure time.

- Draft the message and wait for approval when the user is nearby instead of sending a substitute version.

- Split the work so one worker prepares drafts and a different check confirms approval before any worker sends.
