<template>
  <div class="enh-root">
    <div class="enh-subtitle">How you shape the agent's behavior without touching its code.</div>

    <div class="enh-grid">
      <div class="enh-card skills">
        <div class="enh-card-header">
          <span class="enh-icon">📜</span>
          <div>
            <div class="enh-title">Skills</div>
            <div class="enh-tagline">Injected expertise, on demand</div>
          </div>
        </div>
        <div class="enh-desc">Markdown files with domain-specific instructions, workflows, and rules. Loaded into context when relevant. The agent follows them like a checklist.</div>
        <div class="enh-example">
          <div class="enh-ex-label">Example</div>
          <div class="enh-ex-code">/skill conventional-commit</div>
          <div class="enh-ex-effect">Agent now writes commits in Conventional Commits format — every time, without being told.</div>
        </div>
      </div>

      <div class="enh-card mcps">
        <div class="enh-card-header">
          <span class="enh-icon">🔌</span>
          <div>
            <div class="enh-title">MCPs</div>
            <div class="enh-tagline">Model Context Protocol — external tool servers</div>
          </div>
        </div>
        <div class="enh-desc">A standard for connecting the agent to external systems. Databases, browsers, APIs, design tools — anything that exposes an MCP server becomes a tool the agent can call.</div>
        <div class="enh-example">
          <div class="enh-ex-label">Example</div>
          <div class="enh-ex-code">mcp: playwright → browser automation</div>
          <div class="enh-ex-effect">Agent can navigate pages, fill forms, take screenshots, run E2E tests.</div>
        </div>
      </div>

      <div class="enh-card agents-md">
        <div class="enh-card-header">
          <span class="enh-icon">📋</span>
          <div>
            <div class="enh-title">AGENTS.md</div>
            <div class="enh-tagline">Project-level instructions, checked into git</div>
          </div>
        </div>
        <div class="enh-desc">A file in your repo that tells the agent how this project works. Conventions, architecture decisions, things to avoid. Every team member's agent reads the same file.</div>
        <div class="enh-example">
          <div class="enh-ex-label">Example</div>
          <div class="enh-ex-code">"Always use pnpm. Never import from @internal/legacy."</div>
          <div class="enh-ex-effect">Agent follows your team's rules without you repeating them every session.</div>
        </div>
      </div>
    </div>

    <div class="enh-footer">
      <span class="enh-footer-icon">!</span>
      <span>Every enhancement eats context. MCPs are the hungriest — each server adds tool schemas to every call. Skills are compact by design (loaded on demand, plain markdown).</span>
    </div>
  </div>
</template>

<style scoped>
.enh-root {
  margin-top: 0.3rem;
}

.enh-subtitle {
  font-size: 0.85rem;
  opacity: 0.45;
  margin-bottom: 0.7rem;
  line-height: 1.4;
}

.enh-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.7rem;
}

.enh-card {
  border-radius: 10px;
  padding: 0.7rem 0.75rem;
  display: flex;
  flex-direction: column;
  gap: 0.4rem;
}

.enh-card.skills {
  border: 1px solid rgba(0, 210, 255, 0.2);
  background: rgba(0, 210, 255, 0.04);
}

.enh-card.mcps {
  border: 1px solid rgba(227, 6, 19, 0.2);
  background: rgba(227, 6, 19, 0.04);
}

.enh-card.agents-md {
  border: 1px solid rgba(255, 180, 50, 0.2);
  background: rgba(255, 180, 50, 0.04);
}

.enh-card-header {
  display: flex;
  align-items: flex-start;
  gap: 0.5rem;
}

.enh-icon {
  font-size: 1.15rem;
  flex-shrink: 0;
  margin-top: 0.05rem;
}

.enh-title {
  font-size: 1rem;
  font-weight: 800;
}

.enh-tagline {
  font-size: 0.65rem;
  opacity: 0.4;
  margin-top: 0.05rem;
}

.enh-desc {
  font-size: 0.72rem;
  opacity: 0.7;
  line-height: 1.45;
}

.enh-example {
  margin-top: auto;
  padding: 0.45rem 0.55rem;
  background: rgba(255, 255, 255, 0.03);
  border-radius: 6px;
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.enh-ex-label {
  font-size: 0.55rem;
  text-transform: uppercase;
  letter-spacing: 0.12em;
  opacity: 0.35;
  margin-bottom: 0.2rem;
}

.enh-ex-code {
  font-family: 'SF Mono', 'Fira Code', 'Cascadia Code', monospace;
  font-size: 0.65rem;
  color: rgba(255, 255, 255, 0.65);
  padding: 0.15rem 0;
}

.enh-ex-effect {
  font-size: 0.62rem;
  opacity: 0.4;
  font-style: italic;
  line-height: 1.4;
  margin-top: 0.15rem;
}

.enh-footer {
  margin-top: 0.65rem;
  padding: 0.5rem 0.7rem;
  border-left: 3px solid rgba(255, 180, 50, 0.65);
  background: rgba(255, 180, 50, 0.05);
  border-radius: 0 6px 6px 0;
  font-size: 0.78rem;
  opacity: 0.75;
  line-height: 1.4;
  display: flex;
  align-items: flex-start;
  gap: 0.4rem;
}

.enh-footer-icon {
  flex-shrink: 0;
  font-size: 0.6rem;
  font-weight: 800;
  width: 1.1rem;
  height: 1.1rem;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: rgba(255, 180, 50, 0.2);
  color: rgba(255, 180, 50, 0.9);
  margin-top: 0.05rem;
}
</style>
