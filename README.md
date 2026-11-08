<picture><source media="(prefers-color-scheme: dark)" srcset="assets/imgs/manga-cutout.png"><img src="assets/imgs/manga-light.png" height="314" align="right" alt="Manga sketch of a woman smoking, in profile" /></picture>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=500&size=24&duration=3500&pause=400&color=E6E6E6&vCenter=true&multiline=true&repeat=false&width=600&height=74&lines=Hi%2C+I'm+Tristan;DevOps+Engineer+%C2%B7+AI+Platform+%26+LLMOps">
  <img width="68%" alt="Hi, I'm Tristan. DevOps Engineer, AI Platform and LLMOps." src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=500&size=24&duration=3500&pause=400&color=24292F&vCenter=true&multiline=true&repeat=false&width=600&height=74&lines=Hi%2C+I'm+Tristan;DevOps+Engineer+%C2%B7+AI+Platform+%26+LLMOps">
</picture>

<pre>
From 24/7 banking production ops to DevOps and AI engineering.

I build the platforms that let engineering teams put AI to work safely.
Design agentic workflows, give AI assistants secure access to internal
tools, keep LLM cost and quality in check, and help teams adopt AI in their
daily work.

Also a Grafana dashboard and terminal ricer, because why not.
No hard feelings if my zsh looks better than yours.
</pre>

<a href="https://www.linkedin.com/in/tristan-antiope-9b9a4699/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat&logo=linkedin&logoColor=white" /></a>
<a href="mailto:Antiope.Tristan01.pro@gmail.com"><img alt="Gmail" src="https://img.shields.io/badge/Gmail-EA4335?style=flat&logo=gmail&logoColor=white" /></a>
<a href="cv/Tristan-Antiope-CV-EN.pdf"><img alt="CV" src="assets/badges/cv.svg" /></a><br clear="right">

<p align="center"><img width="100%" height="1" alt="" src="assets/divider-red.svg" /></p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/stack-dark.svg">
  <img width="830" alt="Tech stack. Infra and GitOps: Kubernetes, Helm, Argo CD, Docker, Terraform, GitHub Actions, Velero. Observability: Prometheus, Grafana, Loki, Tempo, Pyroscope, OpenTelemetry, Datadog. Cloud and languages: GCP, AWS, Python, Go, TypeScript, Bash, Linux. Security: SonarQube, Trivy, Snyk, Sealed Secrets, Infisical, Auth0. Platform: Backstage, ToolHive. AI and agents: Claude, Claude Code, Codex, DeepSeek, LangGraph, Langfuse, n8n, MCP." src="assets/stack-light.svg">
</picture>

<p align="center"><img width="100%" height="1" alt="" src="assets/divider-red.svg" /></p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/label-certifications-dark.svg">
  <img alt="Certifications" src="assets/label-certifications-light.svg">
</picture>

<p>
  <a href="https://www.credly.com/badges/a7933e5c-2f48-4b7c-b6b1-bc7f28b39687/public_url"><img align="middle" width="96" alt="AWS Certified Solutions Architect – Associate" src="https://images.credly.com/size/110x110/images/0e284c3f-5164-4b21-8660-0d84737941bc/image.png" /></a>
  <a href="https://www.credly.com/badges/100078ba-bf1c-4c75-b3b5-401cb6307286/public_url"><img align="middle" width="96" alt="Datadog Certified: Datadog Fundamentals" src="https://images.credly.com/images/c953c302-f29b-4f29-a449-f070b800fca0/blob" /></a>
</p>

<p align="center"><img width="100%" height="1" alt="" src="assets/divider-red.svg" /></p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/label-open-source-dark.svg">
  <img alt="Open source" src="assets/label-open-source-light.svg">
</picture>

#### <img src="assets/icons/datadog.svg" width="22" height="22" alt="" /> [datadog-mcp-server](https://github.com/TANTIOPE/datadog-mcp-server) · Creator

MCP server that gives AI assistants access to Datadog, released before the official one. ~40k npm downloads.

- **22 tools**: logs, metrics, traces, monitors, SLOs, incidents, dashboards and more
- **Cross-correlation**: from a log to its trace to the service's latency metrics
- **Token-efficient**: log sampling and compact modes keep responses small
- **Safe writes**: read-only mode and dry-run validation

<a href="https://www.npmjs.com/package/datadog-mcp"><img alt="npm datadog-mcp" src="assets/badges/npm-datadog-mcp.svg" /></a>

#### <img src="assets/icons/toolhive.svg" width="22" height="22" alt="" /> [stacklok/toolhive #5996](https://github.com/stacklok/toolhive/pull/5996) · Contributor

Every client session re-embedded the whole tool catalogue.

- **Before**: 16–19 s per session at 140 tools, so the claude.ai connector timed out loading tools on every connect
- **After**: sub-second, zero embedding calls once warm
- **Fix**: cache keyed on the tool text and the live model id

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/label-at-work-dark.svg">
  <img alt="At work" src="assets/label-at-work-light.svg">
</picture>

#### <img src="assets/icons/langgraph.svg" width="22" height="22" alt="" /> SRE investigation agent · LangGraph multi-agent

Investigates incidents from the alert to the root cause, and proposes a quick patch and a lasting fix.

- **Three causal gates**: the cause must start before the symptom, hit the broken scope but not its healthy siblings, and have a concrete mechanism
- **Verbatim evidence**: every quote must match the real tool output, so hallucinated evidence never reaches a verdict
- **Human-approved fixes**: proposes an immediate patch (restart, scale, config value) or a lasting fix as a pull request; a separate executor with no LLM holds the write permissions and acts only after an authorized approver clicks in Slack
- **Memory**: each report versioned in Git, past investigations recalled on new incidents
- **Locked down**: read-only `kubectl exec` enforced by a CEL admission policy, secrets masked before the model
- **LLM observability**: self-hosted Langfuse, one trace per investigation, per-model cost, and a per-run spend cap that stops the agent cleanly
- **Evals**: a scorer written in code, with no LLM judge, that replays recorded runs on cases taken from real alerts

#### <img src="assets/icons/mcp.svg" width="22" height="22" alt="" /> MCP gateway

Opens internal tools to claude.ai and Claude Code, behind company SSO.

- **OAuth 2.1**: Python gateway (FastMCP) with Auth0, issuing its own audience-bound tokens
- **Per-tool authorization**: separate tool bundles for business and tech users
- **Audit**: every tool call logged per user
- **Lean context**: ToolHive lets assistants find tools on demand instead of loading them all

<p align="center"><img width="100%" height="1" alt="" src="assets/divider-red.svg" /></p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=TANTIOPE&hide_border=true&background=141414&ring=B3282D&fire=B3282D&currStreakNum=E6E6E6&sideNums=E6E6E6&currStreakLabel=D9474E&sideLabels=D9474E&dates=8A8A8A&stroke=3A3A3A">
    <img alt="TANTIOPE contribution streak" src="https://streak-stats.demolab.com/?user=TANTIOPE&hide_border=true&disable_animations=true&background=FFFFFF00&ring=B3282D&fire=B3282D&currStreakNum=141414&sideNums=141414&currStreakLabel=B3282D&sideLabels=B3282D&dates=5A5A5A&stroke=B3282D">
  </picture>
</p>
