<template>
  <div class="cw-root">
    <div class="cw-left">
      <div class="cw-terminal">
        <div class="cw-term-header">
          <span class="cw-term-dot red"></span>
          <span class="cw-term-dot yellow"></span>
          <span class="cw-term-dot green"></span>
          <span class="cw-term-title">Context Usage</span>
          <span class="cw-term-model">claude-opus-4.6 · 88k/200k tokens (44%)</span>
        </div>
        <div class="cw-term-body">
          <div class="cw-bar-row">
            <div class="cw-bar">
              <div class="cw-bar-seg sys" style="width: 1.6%"></div>
              <div class="cw-bar-seg tools" style="width: 8.5%"></div>
              <div class="cw-bar-seg memory" style="width: 0.8%"></div>
              <div class="cw-bar-seg skills" style="width: 1.1%"></div>
              <div class="cw-bar-seg msgs" style="width: 10.5%"></div>
              <div class="cw-bar-seg compact" style="width: 22.5%"></div>
              <div class="cw-bar-seg free" style="width: 55%"></div>
            </div>
          </div>

          <div class="cw-category-header">Estimated usage by category</div>

          <div class="cw-category">
            <span class="cw-cat-dot sys"></span>
            <div class="cw-cat-left">
              <span class="cw-cat-label">System prompt <span class="cw-freq never">never</span></span>
              <span class="cw-cat-desc">role, rules, persona</span>
            </div>
            <span class="cw-cat-tokens">3.2k</span>
            <span class="cw-cat-pct">(1.6%)</span>
          </div>
          <div class="cw-category">
            <span class="cw-cat-dot tools"></span>
            <div class="cw-cat-left">
              <span class="cw-cat-label">Tool definitions <span class="cw-freq never">never</span></span>
              <span class="cw-cat-desc">schemas for read, edit, bash, grep...</span>
            </div>
            <span class="cw-cat-tokens">17.0k</span>
            <span class="cw-cat-pct">(8.5%)</span>
          </div>
          <div class="cw-category">
            <span class="cw-cat-dot memory"></span>
            <div class="cw-cat-left">
              <span class="cw-cat-label">Memory files <span class="cw-freq rarely">rarely</span></span>
              <span class="cw-cat-desc">CLAUDE.md, AGENTS.md</span>
            </div>
            <span class="cw-cat-tokens">1.5k</span>
            <span class="cw-cat-pct">(0.8%)</span>
          </div>
          <div class="cw-category">
            <span class="cw-cat-dot skills"></span>
            <div class="cw-cat-left">
              <span class="cw-cat-label">Skills <span class="cw-freq sometimes">sometimes</span></span>
              <span class="cw-cat-desc">loaded on demand via /skill</span>
            </div>
            <span class="cw-cat-tokens">2.3k</span>
            <span class="cw-cat-pct">(1.1%)</span>
          </div>
          <div class="cw-category">
            <span class="cw-cat-dot msgs"></span>
            <div class="cw-cat-left">
              <span class="cw-cat-label">Messages <span class="cw-freq every">each turn</span></span>
              <span class="cw-cat-desc">your prompts + model replies + tool results</span>
            </div>
            <span class="cw-cat-tokens">21.0k</span>
            <span class="cw-cat-pct">(10.5%)</span>
          </div>
          <div class="cw-category">
            <span class="cw-cat-dot compact"></span>
            <div class="cw-cat-left">
              <span class="cw-cat-label">Autocompact buffer <span class="cw-freq sometimes">when near limit</span></span>
              <span class="cw-cat-desc">summarized older turns</span>
            </div>
            <span class="cw-cat-tokens">45.0k</span>
            <span class="cw-cat-pct">(22.5%)</span>
          </div>
          <div class="cw-category free-row">
            <span class="cw-cat-dot free"></span>
            <div class="cw-cat-left">
              <span class="cw-cat-label">Free space <span class="cw-freq every">shrinks</span></span>
              <span class="cw-cat-desc">room for reasoning + output</span>
            </div>
            <span class="cw-cat-tokens">110.0k</span>
            <span class="cw-cat-pct">(55.0%)</span>
          </div>

          <div class="cw-cache-note">
            <span class="cw-cache-icon">$</span>
            <span class="cw-cache-text">The <span class="cw-hl-never">never</span> and <span class="cw-hl-rarely">rarely</span> parts are identical across calls — harnesses use <strong>prompt caching</strong> to avoid re-sending them.</span>
          </div>
        </div>
      </div>
    </div>

    <div class="cw-right">
      <div class="cw-callout danger">
        <div class="cw-callout-title">Fixed-size box</div>
        <div class="cw-callout-text">The model sees one window of text per call. System prompt, conversation history, tool output, files and everything else all share the same budget.</div>
      </div>
      <div class="cw-callout warn">
        <div class="cw-callout-title">Already half-full before you type</div>
        <div class="cw-callout-text">Tool definitions + system prompt alone can eat 10%+ of the window. Add a few tool calls and you're past 40%. Enable tools wisely.</div>
      </div>
      <div class="cw-callout info">
        <div class="cw-callout-title">What kills it</div>
        <div class="cw-callout-text">Verbose tool output, giant files pasted in, and long conversations. When it fills up, the harness starts dropping older messages or compacting them.</div>
      </div>
      <div class="cw-callout dim">
        <div class="cw-callout-title">Compaction</div>
        <div class="cw-callout-text">When the context nears the limit, the harness summarizes older turns to reclaim space. Every harness does this. Useful, but lossy — the model loses detail.</div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cw-root {
  display: grid;
  grid-template-columns: 1.15fr 0.85fr;
  gap: 1rem;
  align-items: start;
  margin-top: 0.4rem;
}

.cw-terminal {
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  overflow: hidden;
  background: rgba(0, 0, 0, 0.3);
}

.cw-term-header {
  display: flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.5rem 0.7rem;
  background: rgba(255, 255, 255, 0.04);
  border-bottom: 1px solid rgba(255, 255, 255, 0.06);
}

.cw-term-dot {
  width: 9px;
  height: 9px;
  border-radius: 50%;
}
.cw-term-dot.red { background: #ff5f57; }
.cw-term-dot.yellow { background: #febc2e; }
.cw-term-dot.green { background: #28c840; }

.cw-term-title {
  font-weight: 800;
  font-size: 0.78rem;
  margin-left: 0.4rem;
  color: rgba(255, 255, 255, 0.9);
}

.cw-term-model {
  font-size: 0.62rem;
  opacity: 0.4;
  margin-left: auto;
  font-family: 'SF Mono', 'Fira Code', 'Cascadia Code', monospace;
}

.cw-term-body {
  padding: 0.7rem 0.8rem 0.8rem;
  font-family: 'SF Mono', 'Fira Code', 'Cascadia Code', monospace;
  font-size: 0.62rem;
  line-height: 1.6;
}

.cw-bar-row {
  margin-bottom: 0.6rem;
}

.cw-bar {
  display: flex;
  height: 16px;
  border-radius: 4px;
  overflow: hidden;
  background: rgba(255, 255, 255, 0.04);
  gap: 1px;
}

.cw-bar-seg {
  height: 100%;
  border-radius: 2px;
}

.cw-bar-seg.sys { background: #e06c75; }
.cw-bar-seg.tools { background: #c678dd; }
.cw-bar-seg.memory { background: #e5c07b; }
.cw-bar-seg.skills { background: #d19a66; }
.cw-bar-seg.msgs { background: #61afef; }
.cw-bar-seg.compact { background: rgba(255, 255, 255, 0.12); }
.cw-bar-seg.free { background: rgba(255, 255, 255, 0.03); }

.cw-category-header {
  font-size: 0.58rem;
  font-style: italic;
  opacity: 0.45;
  margin-bottom: 0.3rem;
  font-family: 'SF Mono', 'Fira Code', 'Cascadia Code', monospace;
}

.cw-category {
  display: grid;
  grid-template-columns: 10px 1fr auto auto;
  gap: 0.35rem;
  align-items: baseline;
  padding: 0.2rem 0;
  opacity: 0.85;
}

.cw-cat-left {
  display: flex;
  flex-direction: column;
  gap: 0.05rem;
}

.cw-category.free-row {
  margin-top: 0.15rem;
  padding-top: 0.2rem;
  border-top: 1px solid rgba(255, 255, 255, 0.06);
}

.cw-cat-dot {
  width: 7px;
  height: 7px;
  border-radius: 2px;
  margin-top: 0.3rem;
}

.cw-cat-dot.sys { background: #e06c75; }
.cw-cat-dot.tools { background: #c678dd; }
.cw-cat-dot.memory { background: #e5c07b; }
.cw-cat-dot.skills { background: #d19a66; }
.cw-cat-dot.msgs { background: #61afef; }
.cw-cat-dot.compact { background: rgba(255, 255, 255, 0.25); }
.cw-cat-dot.free { background: rgba(255, 255, 255, 0.08); border: 1px dashed rgba(255, 255, 255, 0.2); }

.cw-cat-label {
  color: rgba(255, 255, 255, 0.75);
  white-space: nowrap;
}

.cw-cat-desc {
  color: rgba(255, 255, 255, 0.3);
  font-style: italic;
  font-size: 0.56rem;
}

.cw-freq {
  font-size: 0.5rem;
  font-weight: 400;
  padding: 0.05rem 0.3rem;
  border-radius: 3px;
  margin-left: 0.3rem;
  vertical-align: middle;
  white-space: nowrap;
}

.cw-freq.never {
  color: rgba(255, 255, 255, 0.4);
  background: rgba(255, 255, 255, 0.06);
}

.cw-freq.rarely {
  color: rgba(225, 200, 120, 0.7);
  background: rgba(225, 200, 120, 0.1);
}

.cw-freq.sometimes {
  color: rgba(209, 154, 102, 0.7);
  background: rgba(209, 154, 102, 0.1);
}

.cw-freq.every {
  color: rgba(97, 175, 239, 0.7);
  background: rgba(97, 175, 239, 0.1);
}

.cw-cat-tokens {
  text-align: right;
  color: rgba(255, 255, 255, 0.55);
  white-space: nowrap;
}

.cw-cat-pct {
  text-align: right;
  min-width: 3rem;
  color: rgba(255, 255, 255, 0.35);
  white-space: nowrap;
}

.cw-right {
  display: flex;
  flex-direction: column;
  gap: 0.55rem;
}

.cw-callout {
  padding: 0.6rem 0.75rem;
  border-radius: 0 6px 6px 0;
}

.cw-callout-title {
  font-weight: 800;
  font-size: 0.82rem;
}

.cw-callout-text {
  font-size: 0.76rem;
  opacity: 0.75;
  margin-top: 0.2rem;
  line-height: 1.4;
}

.danger {
  border-left: 3px solid rgba(255, 80, 80, 0.65);
  background: rgba(255, 80, 80, 0.05);
}

.warn {
  border-left: 3px solid rgba(255, 180, 50, 0.65);
  background: rgba(255, 180, 50, 0.05);
}

.info {
  border-left: 3px solid rgba(0, 210, 255, 0.65);
  background: rgba(0, 210, 255, 0.05);
}

.dim {
  border-left: 3px solid rgba(255, 255, 255, 0.2);
  background: rgba(255, 255, 255, 0.02);
}

.cw-cache-note {
  display: flex;
  align-items: flex-start;
  gap: 0.45rem;
  margin-top: 0.5rem;
  padding-top: 0.45rem;
  border-top: 1px solid rgba(255, 255, 255, 0.06);
  font-family: 'SF Mono', 'Fira Code', 'Cascadia Code', monospace;
  font-size: 0.55rem;
  line-height: 1.5;
  color: rgba(255, 255, 255, 0.45);
}

.cw-cache-icon {
  font-size: 0.65rem;
  color: rgba(40, 200, 64, 0.7);
  flex-shrink: 0;
  margin-top: 0.05rem;
}

.cw-cache-text strong {
  color: rgba(255, 255, 255, 0.7);
  font-weight: 600;
}

.cw-hl-never {
  color: rgba(255, 255, 255, 0.5);
  background: rgba(255, 255, 255, 0.06);
  padding: 0.02rem 0.25rem;
  border-radius: 3px;
  font-size: 0.5rem;
}

.cw-hl-rarely {
  color: rgba(225, 200, 120, 0.7);
  background: rgba(225, 200, 120, 0.1);
  padding: 0.02rem 0.25rem;
  border-radius: 3px;
  font-size: 0.5rem;
}
</style>
