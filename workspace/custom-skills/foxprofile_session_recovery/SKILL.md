# Recover FoxProfile sessions before judging them broken

## Check the service before checking the accounts

- Check that the FoxProfile service responds on its local endpoint before you open any account environment.

- Restart the service with the workspace start script when the endpoint does not respond, then check the endpoint again before you retry an account.

- Treat a dead local service as a service failure, never as a broken account or a dead proxy line.

## Wait for stored tabs before navigating

- Wait 45 seconds after an environment opens so its stored tabs can restore before you navigate anywhere.

- Navigate only after that wait, even when the environment looks ready sooner.

- Treat a navigation timeout that followed a short wait as a slow restore, not as proof that the account is broken.

## Check status without exposing credentials

- Query the profiles endpoint only for the environment name and whether it is running.

- Never print, copy, or save the raw profiles response, because it carries proxy credentials inline.

- Stop at once when a credential value appears in tool output, and do not write it to a ledger, a log, a report, or memory.

- Use a proxy only through an export assignment, and verify connectivity with a real call through that proxy instead of printing the proxy value.

- Report a leaked line to the user at once and treat it as needing replacement, and do not reuse the printed value.

## Separate proxy, service, and session failures

- Test the proxy line directly against a public site when a FoxProfile start fails, before you blame the proxy line.

- Treat a passing direct test plus a failing FoxProfile start as a FoxProfile launch problem, not a proxy problem.

- Retry a failed account once after a service restart and the full stored-tab wait before you report it as failed.

- Retest one account alone when a batch round fails, so one slow environment does not hide the state of the others.

## Report only what you verified

- Report an account as unusable only after the service check, the full wait, and one restart retry have all failed.

- Name the exact step that failed in the report, with the wait used and whether the direct proxy test passed.

- Report a round as partial when some accounts pass, and list the passed and failed accounts separately instead of calling the whole round failed.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Alternatives for better results

- Run the check again at the next scheduled round when a single retry still fails, since these failures have been transient rather than permanent.

- Ask the user for help only when the service check, the full wait, the direct proxy test, and the restart retry have all failed for the same account.
