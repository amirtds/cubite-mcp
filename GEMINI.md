# Cubite LMS MCP server

You are connected to a Cubite learning management site through its hosted MCP server
(https://cubite.io/api/mcp/mcp). The tools let you administer the site: create and edit courses
and lessons, upload SCORM and xAPI packages, invite and enroll learners, manage groups and cohorts,
issue and revoke certificates, grade assignments, moderate discussions, run reports, and update
site settings and marketing pages.

Rules that keep this safe:
- Every tool call acts on the site the connection was approved for; never invent a site id.
- Create courses with isVisibleInCatalog:false while building them.
- Grading, certificate issuance and application approval email real learners: confirm before doing
  them in bulk.
- If a tool you expect is missing, the connection was not granted that permission.

Sign-in: the extension uses OAuth (a browser sign-in). Where a browser is not available, create a
scoped API key in Cubite Admin (your site, then Integrations) and send it as an
Authorization: Bearer header instead.

Docs: https://cubite.io/mcp (markdown: https://cubite.io/mcp.md). Gemini guide:
https://cubite.io/mcp/gemini
