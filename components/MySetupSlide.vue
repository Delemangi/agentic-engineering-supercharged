<template>
  <div>
    <div style="font-size: 0.85rem; opacity: 0.45; margin-bottom: 0.5rem;">OpenCode + Oh My OpenCode plugin</div>
    <div style="display: grid; grid-template-columns: 1fr 1fr; grid-template-rows: auto 1px auto; gap: 0;">
      <div style="display: flex; flex-direction: column; gap: 0.2rem; padding: 0.3rem 0.5rem 0.3rem 0;">
        <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.15em; opacity: 0.4; font-weight: 600;">Models by Role</div>
        <div style="display: flex; flex-direction: column; gap: 0.15rem;">
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Coding</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(217,119,60,0.08); border: 1px solid rgba(217,119,60,0.2); color: rgba(240,170,120,0.85);">Claude Opus 4.6</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.1); color: rgba(255,255,255,0.6);">Kimi K2.5</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">main agent, edits code</span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Delegation</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(217,119,60,0.08); border: 1px solid rgba(217,119,60,0.2); color: rgba(240,170,120,0.85);">Claude Sonnet 4.6</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.1); color: rgba(255,255,255,0.6);">Kimi K2.5</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">sub-agents, parallel tasks</span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Reasoning</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(16,163,127,0.08); border: 1px solid rgba(16,163,127,0.2); color: rgba(80,210,170,0.85);">GPT-5.4</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">debugging, review, architecture</span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Planning</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(217,119,60,0.08); border: 1px solid rgba(217,119,60,0.2); color: rgba(240,170,120,0.85);">Claude Opus 4.6</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">plans, analysis, scope</span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Exploration</span>
            <span style="font-size: 0.48rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.1); color: rgba(255,255,255,0.6);">MiniMax M2.7</span>
            <span style="font-size: 0.48rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(217,119,60,0.08); border: 1px solid rgba(217,119,60,0.2); color: rgba(240,170,120,0.85);">Claude Haiku 4.5</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">search, patterns</span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Visual</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(66,133,244,0.08); border: 1px solid rgba(66,133,244,0.2); color: rgba(130,180,255,0.85);">Gemini 3.1 Pro</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">UI, styling, frontend</span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Quick tasks</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(16,163,127,0.08); border: 1px solid rgba(16,163,127,0.2); color: rgba(80,210,170,0.85);">GPT-5.4 Mini</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">typos, small fixes</span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.35rem;">
            <span style="font-size: 0.52rem; opacity: 0.5; min-width: 4rem;">Writing</span>
            <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(66,133,244,0.08); border: 1px solid rgba(66,133,244,0.2); color: rgba(130,180,255,0.85);">Gemini 3 Flash</span>
            <span style="font-size: 0.42rem; opacity: 0.3;">docs, prose</span>
          </div>
        </div>
      </div>
      <div style="display: flex; flex-direction: column; gap: 0.2rem; padding: 0.3rem 0 0.3rem 0.5rem;">
        <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.15em; opacity: 0.4; font-weight: 600;">Providers</div>
        <div style="display: flex; flex-wrap: wrap; gap: 0.25rem; align-items: center;">
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(40,200,64,0.06); border: 1px solid rgba(40,200,64,0.15); color: rgba(130,230,150,0.8);">OpenAI</span>
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(140,120,255,0.06); border: 1px solid rgba(140,120,255,0.15); color: rgba(180,170,255,0.8);">Google</span>
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(40,200,64,0.06); border: 1px solid rgba(40,200,64,0.15); color: rgba(130,230,150,0.8);">GitHub Copilot Pro+</span>
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(40,200,64,0.06); border: 1px solid rgba(40,200,64,0.15); color: rgba(130,230,150,0.8);">OpenCode Go</span>
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,200,40,0.06); border: 1px solid rgba(255,200,40,0.15); color: rgba(255,220,120,0.8);">OpenCode Zen</span>
        </div>
        <div style="display: flex; gap: 0.6rem; margin-top: 0.1rem;">
          <span style="font-size: 0.42rem; opacity: 0.45; display: flex; align-items: center; gap: 0.15rem;"><span style="display: inline-block; width: 5px; height: 5px; border-radius: 2px; background: rgba(40,200,64,0.5);"></span> subscription</span>
          <span style="font-size: 0.42rem; opacity: 0.45; display: flex; align-items: center; gap: 0.15rem;"><span style="display: inline-block; width: 5px; height: 5px; border-radius: 2px; background: rgba(255,200,40,0.5);"></span> token billing</span>
          <span style="font-size: 0.42rem; opacity: 0.45; display: flex; align-items: center; gap: 0.15rem;"><span style="display: inline-block; width: 5px; height: 5px; border-radius: 2px; background: rgba(140,120,255,0.5);"></span> free tier</span>
        </div>
      </div>
      <div style="height: 1px; background: rgba(255,255,255,0.08); grid-column: 1 / -1;"></div>
      <div style="display: flex; flex-direction: column; gap: 0.2rem; padding: 0.3rem 0.5rem 0 0;">
        <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.15em; opacity: 0.4; font-weight: 600;">MCPs</div>
        <div style="display: grid; grid-template-columns: 4rem 1fr; gap: 0.15rem 0.3rem; align-items: baseline;">
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,100,200,0.06); border: 1px solid rgba(255,100,200,0.15); color: rgba(255,160,220,0.8); text-align: center;">context7</span>
          <span style="font-size: 0.42rem; opacity: 0.3;">live library docs</span>
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,100,200,0.06); border: 1px solid rgba(255,100,200,0.15); color: rgba(255,160,220,0.8); text-align: center;">grep_app</span>
          <span style="font-size: 0.42rem; opacity: 0.3;">search GitHub code</span>
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,100,200,0.06); border: 1px solid rgba(255,100,200,0.15); color: rgba(255,160,220,0.8); text-align: center;">websearch</span>
          <span style="font-size: 0.42rem; opacity: 0.3;">Exa web search</span>
          <span style="font-size: 0.52rem; padding: 0.1rem 0.3rem; border-radius: 4px; font-family: monospace; background: rgba(255,100,200,0.06); border: 1px solid rgba(255,100,200,0.15); color: rgba(255,160,220,0.8); text-align: center;">xrite</span>
          <span style="font-size: 0.42rem; opacity: 0.3;">color science, devices</span>
        </div>
      </div>
      <div style="display: flex; flex-direction: column; gap: 0.2rem; padding: 0.3rem 0 0 0.5rem;">
        <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.15em; opacity: 0.4; font-weight: 600;">Skills <span style="opacity: 0.6; font-weight: 400;">20</span></div>
        <div style="display: flex; flex-wrap: wrap; gap: 0.18rem;">
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">brainstorming</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">git-master</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">playwright</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">shadcn</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">frontend-design</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">ai-slop-remover</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">review-work</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">find-docs</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">conventional-commit</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">find-skills</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">frontend-ui-ux</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">dev-browser</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">gh-cli</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">multi-stage-dockerfile</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">tailwind-design-system</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">ui-ux-pro-max</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">using-git-worktrees</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">vercel-composition-patterns</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">vercel-react-best-practices</span>
          <span style="font-size: 0.45rem; padding: 0.08rem 0.25rem; border-radius: 4px; font-family: monospace; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.15); color: rgba(120,225,255,0.8);">web-design-guidelines</span>
        </div>
      </div>
    </div>
  </div>
</template>
