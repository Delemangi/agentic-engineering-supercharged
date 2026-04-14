<template>
  <div>
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1.2rem; margin-top: 0.7rem; align-items: start;">
      <div>
        <div style="font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.18em; opacity: 0.4; margin-bottom: 0.55rem;">Anatomy</div>
        <div style="border: 2px solid rgba(227,6,19,0.3); background: rgba(227,6,19,0.05); border-radius: 12px; padding: 0.7rem 0.8rem 0.8rem;">
          <div style="display: flex; align-items: baseline; gap: 0.4rem;">
            <span style="font-size: 0.95rem; font-weight: 800; color: #fff;">Harness</span>
            <span style="font-size: 0.65rem; opacity: 0.4;">opencode · Claude Code · Cursor · Windsurf</span>
          </div>
          <div style="margin-top: 0.15rem; opacity: 0.5; font-size: 0.7rem; line-height: 1.35;">The software you run. It orchestrates everything below.</div>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.45rem; margin-top: 0.55rem;">
            <div style="border: 1px solid rgba(140,120,255,0.2); background: rgba(140,120,255,0.06); border-radius: 8px; padding: 0.55rem;">
              <div style="font-size: 0.82rem; font-weight: 800; color: rgba(140,120,255,0.9);">Model</div>
              <div style="margin-top: 0.15rem; opacity: 0.5; font-size: 0.65rem; line-height: 1.3;">Thinks. Decides what to do next. Has no memory between calls.</div>
            </div>
            <div style="border: 1px solid rgba(255,180,50,0.2); background: rgba(255,180,50,0.06); border-radius: 8px; padding: 0.55rem;">
              <div style="font-size: 0.82rem; font-weight: 800; color: rgba(255,180,50,0.9);">Tools</div>
              <div style="margin-top: 0.15rem; opacity: 0.5; font-size: 0.65rem; line-height: 1.3;">Acts. Reads files, edits code, runs commands, searches.</div>
            </div>
          </div>
        </div>
        <div style="margin-top: 0.45rem; font-size: 0.72rem; opacity: 0.45; line-height: 1.4; padding-left: 0.2rem;">Harness + Model + Tools in a loop = what we call an <strong style="opacity: 1;">Agent</strong>.</div>
      </div>
      <div>
        <div style="font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.18em; opacity: 0.4; margin-bottom: 0.55rem;">How it works</div>
        <div style="display: flex; flex-direction: column; gap: 0;">
          <div style="display: flex; align-items: center; gap: 0.6rem; padding: 0.5rem 0.7rem; background: rgba(0,210,255,0.06); border: 1px solid rgba(0,210,255,0.12); border-radius: 8px 8px 0 0;">
            <span style="font-size: 0.85rem; font-weight: 800; color: rgba(0,210,255,0.7); min-width: 1.2rem;">1</span>
            <span style="font-size: 0.82rem;"><strong>You prompt</strong> <span style="opacity: 0.45;">→ harness builds full context</span></span>
          </div>
          <div style="display: flex; align-items: center; gap: 0.6rem; padding: 0.5rem 0.7rem; background: rgba(140,120,255,0.06); border: 1px solid rgba(140,120,255,0.12); border-top: none;">
            <span style="font-size: 0.85rem; font-weight: 800; color: rgba(140,120,255,0.7); min-width: 1.2rem;">2</span>
            <span style="font-size: 0.82rem;"><strong>Model decides</strong> <span style="opacity: 0.45;">→ call a tool <em>or</em> respond</span></span>
          </div>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.35rem; margin-top: 0.35rem;">
            <div style="position: relative; border: 1px solid rgba(255,180,50,0.15); border-radius: 8px; padding: 0.45rem 0.5rem; background: rgba(255,180,50,0.04);">
              <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.1em; color: rgba(255,180,50,0.6); margin-bottom: 0.3rem;">Tool path ⟳</div>
              <div style="display: flex; align-items: center; gap: 0.4rem; padding: 0.3rem 0; border-bottom: 1px solid rgba(255,180,50,0.08);">
                <span style="font-size: 0.7rem; font-weight: 800; color: rgba(255,180,50,0.7);">3</span>
                <span style="font-size: 0.72rem;"><strong>Tool runs</strong></span>
              </div>
              <div style="display: flex; align-items: center; gap: 0.4rem; padding: 0.3rem 0; border-bottom: 1px solid rgba(255,180,50,0.08);">
                <span style="font-size: 0.7rem; font-weight: 800; color: rgba(70,200,120,0.7);">4</span>
                <span style="font-size: 0.72rem;"><strong>Result fed back</strong></span>
              </div>
              <div style="margin-top: 0.3rem; text-align: center; font-size: 0.65rem; color: rgba(140,120,255,0.6); font-weight: 700;">↑ back to step 2</div>
            </div>
            <div style="border: 1px dashed rgba(255,255,255,0.12); border-radius: 8px; padding: 0.45rem 0.5rem; background: rgba(255,255,255,0.02); display: flex; flex-direction: column; justify-content: center; align-items: center; text-align: center;">
              <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.1em; color: rgba(255,255,255,0.3); margin-bottom: 0.3rem;">Response path</div>
              <div style="font-size: 0.78rem; font-weight: 800; color: rgba(255,255,255,0.4);">✓</div>
              <div style="font-size: 0.72rem; opacity: 0.5; margin-top: 0.15rem;"><strong>Model responds</strong></div>
              <div style="font-size: 0.62rem; opacity: 0.3; margin-top: 0.1rem;">Done. You see the answer.</div>
            </div>
          </div>
        </div>
        <div style="margin-top: 0.5rem; font-size: 0.72rem; opacity: 0.4; line-height: 1.4;">Each call reconstructs the entire conversation. Nothing persists in the model.</div>
      </div>
    </div>

    <div style="margin-top: 0.7rem; padding: 0.7rem 0.9rem; border-left: 3px solid rgba(227,6,19,0.85); background: rgba(227,6,19,0.08); border-radius: 0 6px 6px 0; font-size: 0.88rem; line-height: 1.45;">
      <strong>The memory is a LIE.</strong> The model forgets everything between calls. The harness just keeps reconstructing the conversation.
    </div>

    <div style="margin-top: 0.55rem; background: rgba(255,255,255,0.02); border: 1px solid rgba(255,255,255,0.06); border-radius: 8px; padding: 0.5rem 0.7rem;">
      <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.12em; opacity: 0.35; margin-bottom: 0.4rem;">In practice (Oversimplification)</div>
      <div style="display: flex; flex-direction: column; gap: 0.35rem; font-size: 0.68rem;">
        <div style="display: flex; align-items: center; gap: 0.3rem; flex-wrap: wrap; line-height: 1.8;">
          <span style="background: rgba(0,210,255,0.1); border: 1px solid rgba(0,210,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem; font-style: italic;">"fix the login bug"</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(140,120,255,0.1); border: 1px solid rgba(140,120,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem;">grep "login"</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(140,120,255,0.1); border: 1px solid rgba(140,120,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem;">read auth.ts</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(140,120,255,0.1); border: 1px solid rgba(140,120,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem;">edit auth.ts</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(140,120,255,0.1); border: 1px solid rgba(140,120,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem;">npm test</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(255,255,255,0.06); border: 1px dashed rgba(255,255,255,0.12); border-radius: 4px; padding: 0.1rem 0.4rem; opacity: 0.5;">"Fixed the null check in validateSession()"</span>
        </div>
        <div style="display: flex; align-items: center; gap: 0.3rem; flex-wrap: wrap; line-height: 1.8;">
          <span style="background: rgba(0,210,255,0.1); border: 1px solid rgba(0,210,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem; font-style: italic;">"add dark mode"</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(140,120,255,0.1); border: 1px solid rgba(140,120,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem;">read globals.css</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(140,120,255,0.1); border: 1px solid rgba(140,120,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem;">edit 5 files</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(140,120,255,0.1); border: 1px solid rgba(140,120,255,0.15); border-radius: 4px; padding: 0.1rem 0.4rem;">npm run build</span>
          <span style="opacity: 0.25;">→</span>
          <span style="background: rgba(255,255,255,0.06); border: 1px dashed rgba(255,255,255,0.12); border-radius: 4px; padding: 0.1rem 0.4rem; opacity: 0.5;">"Done. Toggle is in Settings → Appearance"</span>
        </div>
      </div>
    </div>
  </div>
</template>
