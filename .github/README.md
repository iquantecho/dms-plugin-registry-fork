# Fork automation

GitHub Actions stays disabled in this personal registry fork. The unused plugin
and theme preview workflows were removed because they executed Python from an
untrusted pull-request checkout with privileged credentials.

Before enabling automation or syncing workflows from upstream, review the trust
boundary. Generate previews without secrets under `pull_request`; any trusted
publisher must consume validated data without importing or executing PR code.
