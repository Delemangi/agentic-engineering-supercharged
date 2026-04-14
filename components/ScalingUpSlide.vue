<template>
  <div class="sc-root">
    <div class="sc-subtitle">When one agent isn't enough.</div>

    <div class="sc-grid">
      <div class="sc-card subagents">
        <div class="sc-card-top">
          <div class="sc-card-header">
            <span class="sc-icon">🧠×N</span>
            <div>
              <div class="sc-title">Subagents</div>
              <div class="sc-tagline">Delegate tasks to specialized child agents</div>
            </div>
          </div>
          <div class="sc-desc">The main agent can spawn child agents to handle subtasks in parallel. Each subagent gets its own context window, its own tools, and its own conversation. The parent coordinates.</div>
        </div>

        <div class="sc-visual">
          <div class="sc-agent-row">
            <div class="sc-agent parent">
              <span class="sc-agent-label">Main agent</span>
              <span class="sc-agent-hint">"add auth to the API"</span>
            </div>
          </div>
          <div class="sc-arrow-row">
            <span class="sc-arrow">↙</span>
            <span class="sc-arrow">↓</span>
            <span class="sc-arrow">↘</span>
          </div>
          <div class="sc-agent-row children">
            <div class="sc-agent child">
              <span class="sc-agent-label">explore</span>
              <span class="sc-agent-hint">find patterns</span>
            </div>
            <div class="sc-agent child">
              <span class="sc-agent-label">implement</span>
              <span class="sc-agent-hint">write middleware</span>
            </div>
            <div class="sc-agent child">
              <span class="sc-agent-label">test</span>
              <span class="sc-agent-hint">write + run tests</span>
            </div>
          </div>
        </div>

        <div class="sc-benefit">
          <span class="sc-benefit-plus">+</span>
          <span>Parallel execution. Isolated contexts. Each agent focused on one job.</span>
        </div>
      </div>

      <div class="sc-card worktrees">
        <div class="sc-card-top">
          <div class="sc-card-header">
            <span class="sc-icon">🌲</span>
            <div>
              <div class="sc-title">Git Worktrees</div>
              <div class="sc-tagline">Isolated branches, no stashing, no conflicts</div>
            </div>
          </div>
          <div class="sc-desc">Each agent (or subagent) works in its own git worktree — a separate checkout of the same repo. No stepping on each other's files. Merge when done.</div>
        </div>

        <div class="sc-visual">
          <div class="sc-tree-diagram">
            <div class="sc-tree-repo">
              <span class="sc-tree-label">repo/</span>
            </div>
            <div class="sc-tree-branches">
              <div class="sc-tree-branch main">
                <span class="sc-branch-name">main</span>
                <span class="sc-branch-path">repo/</span>
                <span class="sc-branch-status">your editor</span>
              </div>
              <div class="sc-tree-branch wt1">
                <span class="sc-branch-name">feat/auth</span>
                <span class="sc-branch-path">../repo-auth/</span>
                <span class="sc-branch-status">agent 1</span>
              </div>
              <div class="sc-tree-branch wt2">
                <span class="sc-branch-name">fix/login</span>
                <span class="sc-branch-path">../repo-login/</span>
                <span class="sc-branch-status">agent 2</span>
              </div>
            </div>
          </div>
        </div>

        <div class="sc-benefit">
          <span class="sc-benefit-plus">+</span>
          <span>You keep working in your editor. Agents work in parallel on separate branches. No conflicts until merge.</span>
        </div>
      </div>
    </div>

    <div class="sc-footer">
      <span class="sc-footer-icon">💡</span>
      <span>Subagents + worktrees together = multiple agents working on different features simultaneously, each in their own branch. This is where agentic engineering gets <strong>wild</strong>.</span>
    </div>
  </div>
</template>

<style scoped>
.sc-root {
  margin-top: 0.3rem;
}

.sc-subtitle {
  font-size: 0.85rem;
  opacity: 0.45;
  margin-bottom: 0.7rem;
  line-height: 1.4;
}

.sc-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0.8rem;
}

.sc-card {
  border-radius: 10px;
  padding: 0.7rem 0.75rem;
  display: flex;
  flex-direction: column;
  gap: 0.45rem;
}

.sc-card.subagents {
  border: 1px solid rgba(140, 120, 255, 0.2);
  background: rgba(140, 120, 255, 0.04);
}

.sc-card.worktrees {
  border: 1px solid rgba(40, 200, 64, 0.2);
  background: rgba(40, 200, 64, 0.04);
}

.sc-card-top {
  display: flex;
  flex-direction: column;
  gap: 0.35rem;
}

.sc-card-header {
  display: flex;
  align-items: flex-start;
  gap: 0.5rem;
}

.sc-icon {
  font-size: 1.05rem;
  flex-shrink: 0;
  margin-top: 0.05rem;
}

.sc-title {
  font-size: 1rem;
  font-weight: 800;
}

.sc-tagline {
  font-size: 0.65rem;
  opacity: 0.4;
  margin-top: 0.05rem;
}

.sc-desc {
  font-size: 0.72rem;
  opacity: 0.65;
  line-height: 1.45;
}

/* Subagent visual */
.sc-visual {
  margin-top: 0.15rem;
  padding: 0.5rem;
  background: rgba(0, 0, 0, 0.2);
  border-radius: 8px;
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.sc-agent-row {
  display: flex;
  justify-content: center;
  gap: 0.4rem;
}

.sc-agent-row.children {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0.35rem;
}

.sc-agent {
  text-align: center;
  padding: 0.3rem 0.5rem;
  border-radius: 6px;
}

.sc-agent.parent {
  background: rgba(140, 120, 255, 0.12);
  border: 1px solid rgba(140, 120, 255, 0.25);
  display: inline-flex;
  flex-direction: column;
  gap: 0.1rem;
}

.sc-agent.child {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
  display: flex;
  flex-direction: column;
  gap: 0.1rem;
}

.sc-agent-label {
  font-size: 0.68rem;
  font-weight: 700;
  color: rgba(255, 255, 255, 0.75);
}

.sc-agent-hint {
  font-size: 0.55rem;
  opacity: 0.35;
  font-style: italic;
}

.sc-arrow-row {
  display: flex;
  justify-content: center;
  gap: 2.2rem;
  font-size: 0.75rem;
  color: rgba(140, 120, 255, 0.4);
  padding: 0.15rem 0;
}

/* Worktree visual */
.sc-tree-diagram {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}

.sc-tree-repo {
  text-align: center;
}

.sc-tree-label {
  font-family: 'SF Mono', 'Fira Code', 'Cascadia Code', monospace;
  font-size: 0.65rem;
  color: rgba(255, 255, 255, 0.5);
  background: rgba(255, 255, 255, 0.05);
  padding: 0.15rem 0.5rem;
  border-radius: 4px;
}

.sc-tree-branches {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.sc-tree-branch {
  display: grid;
  grid-template-columns: auto 1fr auto;
  gap: 0.4rem;
  align-items: center;
  padding: 0.25rem 0.45rem;
  border-radius: 5px;
  font-family: 'SF Mono', 'Fira Code', 'Cascadia Code', monospace;
  font-size: 0.6rem;
}

.sc-tree-branch.main {
  background: rgba(40, 200, 64, 0.08);
  border: 1px solid rgba(40, 200, 64, 0.15);
}

.sc-tree-branch.wt1 {
  background: rgba(140, 120, 255, 0.06);
  border: 1px solid rgba(140, 120, 255, 0.12);
}

.sc-tree-branch.wt2 {
  background: rgba(0, 210, 255, 0.06);
  border: 1px solid rgba(0, 210, 255, 0.12);
}

.sc-branch-name {
  font-weight: 700;
  color: rgba(255, 255, 255, 0.7);
  white-space: nowrap;
}

.sc-branch-path {
  color: rgba(255, 255, 255, 0.3);
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.sc-branch-status {
  font-size: 0.55rem;
  opacity: 0.4;
  font-style: italic;
  white-space: nowrap;
}

.sc-benefit {
  display: flex;
  align-items: flex-start;
  gap: 0.35rem;
  font-size: 0.68rem;
  opacity: 0.55;
  line-height: 1.4;
  margin-top: auto;
}

.sc-benefit-plus {
  color: rgba(40, 200, 64, 0.8);
  font-weight: 800;
  flex-shrink: 0;
}

.sc-footer {
  margin-top: 0.65rem;
  padding: 0.5rem 0.7rem;
  border-left: 3px solid rgba(140, 120, 255, 0.65);
  background: rgba(140, 120, 255, 0.05);
  border-radius: 0 6px 6px 0;
  font-size: 0.78rem;
  opacity: 0.75;
  line-height: 1.4;
  display: flex;
  align-items: flex-start;
  gap: 0.4rem;
}

.sc-footer-icon {
  flex-shrink: 0;
  opacity: 0.8;
}

.sc-footer strong {
  opacity: 1;
  color: rgba(255, 255, 255, 0.95);
}
</style>
