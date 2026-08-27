# NexusRecall Companion 0.1.0 (120)

Private-beta recovery and continuity update.

- Restores Tunnel ID and API key editors after a clean install or uninstall instead of showing nonfunctional Retry controls
- Adds explicit, single-flight **Repair Companion** recovery for a missing background agent, with one bounded launchd reclaim and no idle polling
- Keeps credential and Library errors separate from agent repair so Connect does not churn the Login Item registration
- Preserves entered credentials while Login Items approval is pending and commits both credentials through one Connect transaction
- Removes the update-recovery sleep loop in favor of the shared event-driven control-socket readiness path
- Adds signing-family diagnostics for background-agent launch failures

Soft tip with no `minimumRequiredBuild`. Distribution artifact uses Developer ID signing, hardened runtime, notarization, and the sanitized external MCP surface.
