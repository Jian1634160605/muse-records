# Pending approval lock for outbound sends

## Check the lock before you send

- Read the pending approval record for the recipient, thread, or item before you prepare any outbound send.

- Treat a record that names the same recipient, thread, or item as locked even when the draft text differs from the version you would write.

- Skip the send when a lock is present and do not substitute your own wording for the waiting draft.

- Check the record again immediately before sending when any time has passed since your first check.

- Treat a missing or unreadable record as locked for that recipient, thread, or item until you can confirm the approval state another way.

## Set and clear the lock

- Create a pending approval record as soon as a draft, reply, or post is put to the user for a decision and note the exact text, the recipient, and the time you asked.

- Keep the lock in place while the user has not replied, while an approval card is still open, and while a timeout has not yet produced an explicit approval.

- Clear the lock only when the user approves that exact text, when the user sends the message themselves, or when the user explicitly cancels the draft.

- Never clear a lock because a new reply arrived, because a scheduled round started, or because a follow up interval elapsed.

- Record each lock, each skip, and each clearance with the time and the reason so a later round can see what happened.

## Handle a new reply on a locked thread

- Treat a new inbound reply as information about the conversation and not as approval to send a waiting draft.

- Read the new reply, update the record, and leave the locked draft untouched when the user has not yet approved it.

- Answer a new reply with a fresh message only when no lock covers that thread and the content is already settled.

- Wait for the user decision when the new reply changes what the waiting draft should say and ask the user to approve the revised text.

- Never use speed, a reply deadline, or a routine trigger as a reason to send past a lock.

## Report a skipped send

- Tell the user in the same round that you skipped a send because of a lock and name the recipient and the reason.

- Keep the waiting draft available for the user to approve, edit, or cancel and do not send it in a later round without that decision.

- Log the skipped send in the thread record so the next worker does not retry it as a fresh send.

- Ask the user for a decision when a lock has stayed open across several rounds and the conversation needs an answer.

## Available connectors

- [Messenger](/opt/hatch/connectors/messenger_read/CONNECTOR.md) for reading and sending messages in a thread you have already checked for a lock.

- [Facebook](/opt/hatch/connectors/facebook_cli/CONNECTOR.md) for reading posts and comments and for publishing a post only after its exact text is approved.

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Draft the message and wait for approval when the user is nearby instead of sending a substitute version.

- Send a short status update to the user about the waiting draft when a reply needs attention and the draft itself must stay unsent.

- Split the work so one worker prepares drafts and a different check confirms approval before any worker sends.
