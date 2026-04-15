<template>
  <div style="display: flex; flex-direction: column; gap: 0.9rem; height: 100%; justify-content: center;">

    <div style="display: flex; align-items: stretch; gap: 0;">

      <div style="flex: 1; display: flex; flex-direction: column; padding: 0.9rem 1rem; border: 1px solid rgba(140,120,255,0.2); background: rgba(140,120,255,0.025); border-radius: 8px 0 0 8px; opacity: 0.78; position: relative; overflow: hidden;">
        <div style="position: absolute; top: 0; left: 0; right: 0; height: 2px; background: rgba(140,120,255,0.3);"></div>
        <div style="display: flex; align-items: baseline; gap: 0.5rem; margin-bottom: 0.4rem;">
          <span style="font-size: 1.6rem; font-weight: 900; letter-spacing: -0.04em; color: rgba(140,120,255,0.65); font-family: monospace;">2021</span>
          <span style="font-size: 0.55rem; font-weight: 700; letter-spacing: 0.15em; text-transform: uppercase; color: rgba(140,120,255,0.6); font-family: monospace;">AUTOCOMPLETE</span>
        </div>
        <div style="font-size: 0.7rem; color: rgba(255,255,255,0.52); line-height: 1.6; font-family: monospace; margin-bottom: 0.5rem;">
          Tab to accept.<br />
          You write the code.<br />
          AI fills in the boring parts.
        </div>
        <div style="background: rgba(0,0,0,0.4); border: 1px solid rgba(140,120,255,0.12); border-radius: 4px; padding: 0.45rem 0.6rem; font-family: monospace; font-size: 0.65rem; line-height: 1.6; margin-bottom: 0.5rem; flex-grow: 1;">
          <span style="color: rgba(140,120,255,0.6);">fn</span> <span style="color: rgba(255,255,255,0.6);">validate(</span><span style="color: rgba(255,180,50,0.55);">s</span><span style="color: rgba(255,255,255,0.6);">)</span> <span style="color: rgba(255,255,255,0.6);">{</span><br />
          <span style="color: rgba(255,255,255,0.3);">&nbsp;&nbsp;return s.len() > 0</span>
          <span style="display: inline-block; width: 5px; height: 0.85em; background: rgba(140,120,255,0.45); vertical-align: middle; margin-left: 2px;"></span><br />
          <span style="color: rgba(255,255,255,0.6);">}</span>
        </div>
        <div style="display: flex; justify-content: space-between; align-items: center; padding-top: 0.35rem; border-top: 1px solid rgba(140,120,255,0.1);">
          <span style="font-size: 0.55rem; font-weight: 700; letter-spacing: 0.18em; text-transform: uppercase; color: rgba(140,120,255,0.55); font-family: monospace;">YOU TYPE</span>
          <span style="font-size: 0.5rem; color: rgba(140,120,255,0.4); font-family: monospace;">Copilot</span>
        </div>
      </div>

      <div style="display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0.15rem; width: 1.8rem; flex-shrink: 0;">
        <div style="width: 1px; flex: 1; background: linear-gradient(180deg, transparent, rgba(140,120,255,0.08), rgba(0,210,255,0.08), transparent);"></div>
        <span style="color: rgba(255,255,255,0.15); font-size: 0.65rem; font-family: monospace;">&#x25B6;</span>
        <div style="width: 1px; flex: 1; background: linear-gradient(180deg, transparent, rgba(0,210,255,0.1), rgba(140,120,255,0.1), transparent);"></div>
      </div>

      <div style="flex: 1; display: flex; flex-direction: column; padding: 0.9rem 1rem; border: 1px solid rgba(0,210,255,0.22); background: rgba(0,210,255,0.03); border-radius: 0; opacity: 0.88; position: relative; overflow: hidden;">
        <div style="position: absolute; top: 0; left: 0; right: 0; height: 2px; background: rgba(0,210,255,0.4);"></div>
        <div style="display: flex; align-items: baseline; gap: 0.5rem; margin-bottom: 0.4rem;">
          <span style="font-size: 1.6rem; font-weight: 900; letter-spacing: -0.04em; color: rgba(0,210,255,0.7); font-family: monospace;">2023</span>
          <span style="font-size: 0.55rem; font-weight: 700; letter-spacing: 0.15em; text-transform: uppercase; color: rgba(0,210,255,0.65); font-family: monospace;">CHAT</span>
        </div>
        <div style="font-size: 0.7rem; color: rgba(255,255,255,0.58); line-height: 1.6; font-family: monospace; margin-bottom: 0.5rem;">
          Ask a question, get a snippet.<br />
          Copy-paste into your editor.<br />
          You're still driving.
        </div>
        <div style="background: rgba(0,0,0,0.4); border: 1px solid rgba(0,210,255,0.12); border-radius: 4px; padding: 0.45rem 0.6rem; font-family: monospace; font-size: 0.65rem; line-height: 1.6; margin-bottom: 0.5rem; flex-grow: 1;">
          <span style="color: rgba(0,210,255,0.65);">&gt;</span> <span style="color: rgba(255,255,255,0.6);">How do I validate</span><br />
          <span style="color: rgba(255,255,255,0.6);">&nbsp;&nbsp;a string in Rust?</span><br />
          <span style="color: rgba(0,210,255,0.5);">&lt;</span> <span style="color: rgba(255,255,255,0.38);">Here's a function...</span>
        </div>
        <div style="display: flex; justify-content: space-between; align-items: center; padding-top: 0.35rem; border-top: 1px solid rgba(0,210,255,0.12);">
          <span style="font-size: 0.55rem; font-weight: 700; letter-spacing: 0.18em; text-transform: uppercase; color: rgba(0,210,255,0.6); font-family: monospace;">YOU ASK</span>
          <span style="font-size: 0.5rem; color: rgba(0,210,255,0.45); font-family: monospace;">ChatGPT</span>
        </div>
      </div>

      <div style="display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0.15rem; width: 1.8rem; flex-shrink: 0;">
        <div style="width: 1px; flex: 1; background: linear-gradient(180deg, transparent, rgba(0,210,255,0.1), rgba(227,6,19,0.1), transparent);"></div>
        <span style="color: rgba(255,255,255,0.15); font-size: 0.65rem; font-family: monospace;">&#x25B6;</span>
        <div style="width: 1px; flex: 1; background: linear-gradient(180deg, transparent, rgba(227,6,19,0.1), rgba(0,210,255,0.1), transparent);"></div>
      </div>

      <div style="flex: 1.3; display: flex; flex-direction: column; padding: 0.9rem 1rem; border: 1px solid rgba(227,6,19,0.4); background: rgba(227,6,19,0.045); border-radius: 0 8px 8px 0; position: relative; overflow: hidden; box-shadow: 0 0 28px rgba(227,6,19,0.08), inset 0 0 18px rgba(227,6,19,0.025);">
        <div style="position: absolute; top: 0; left: 0; right: 0; height: 3px; background: linear-gradient(90deg, rgba(227,6,19,0.6), rgba(255,80,80,0.8), rgba(227,6,19,0.6));"></div>
        <div style="position: absolute; top: 0.45rem; right: 0.55rem; font-size: 0.5rem; font-weight: 700; letter-spacing: 0.18em; text-transform: uppercase; color: rgba(227,6,19,0.9); font-family: monospace; border: 1px solid rgba(227,6,19,0.45); background: rgba(227,6,19,0.1); padding: 0.08rem 0.4rem; border-radius: 2px;">NOW</div>
        <div style="display: flex; align-items: baseline; gap: 0.5rem; margin-bottom: 0.4rem;">
          <span style="font-size: 1.9rem; font-weight: 900; letter-spacing: -0.04em; color: #E30613; font-family: monospace; text-shadow: 0 0 16px rgba(227,6,19,0.35);">2025</span>
          <span style="font-size: 0.55rem; font-weight: 700; letter-spacing: 0.15em; text-transform: uppercase; color: rgba(227,6,19,0.8); font-family: monospace;">AGENTS</span>
        </div>
        <div style="font-size: 0.72rem; color: rgba(255,255,255,0.75); line-height: 1.6; font-family: monospace; margin-bottom: 0.5rem;">
          Describe the goal.<br />
          The agent reads, plans, edits, tests.<br />
          You review and steer.
        </div>
        <div style="background: rgba(0,0,0,0.4); border: 1px solid rgba(227,6,19,0.15); border-radius: 4px; padding: 0.45rem 0.6rem; font-family: monospace; font-size: 0.65rem; line-height: 1.6; margin-bottom: 0.5rem; flex-grow: 1;">
          <span style="color: rgba(227,6,19,0.65);">$</span> <span style="color: rgba(255,255,255,0.75);">opencode</span><br />
          <span style="color: rgba(0,210,255,0.55);">&gt;</span> <span style="color: rgba(255,255,255,0.65);">fix the login bug</span><br />
          <span style="color: rgba(255,180,50,0.6);">grep</span> <span style="color: rgba(255,255,255,0.38);">auth.ts</span> <span style="color: rgba(255,255,255,0.18);">..</span> <span style="color: rgba(255,180,50,0.6);">edit</span> <span style="color: rgba(255,255,255,0.38);">auth.ts</span> <span style="color: rgba(255,255,255,0.18);">..</span> <span style="color: rgba(70,200,120,0.7);">tests pass</span>
        </div>
        <div style="display: flex; justify-content: space-between; align-items: center; padding-top: 0.35rem; border-top: 1px solid rgba(227,6,19,0.18);">
          <span style="font-size: 0.55rem; font-weight: 700; letter-spacing: 0.18em; text-transform: uppercase; color: rgba(227,6,19,0.65); font-family: monospace;">YOU STEER</span>
          <span style="font-size: 0.5rem; color: rgba(227,6,19,0.4); font-family: monospace;">opencode, Claude Code, Cursor</span>
        </div>
      </div>

    </div>

    <div style="display: flex; align-items: center; gap: 0.7rem;">
      <div style="flex: 1; height: 1px; background: linear-gradient(90deg, rgba(140,120,255,0.12), rgba(0,210,255,0.2), rgba(227,6,19,0.4));"></div>
      <span style="font-size: 0.55rem; font-weight: 700; letter-spacing: 0.25em; text-transform: uppercase; color: rgba(255,255,255,0.25); font-family: monospace; white-space: nowrap;">passive &#x2192; interactive &#x2192; autonomous</span>
      <div style="flex: 1; height: 1px; background: linear-gradient(90deg, rgba(227,6,19,0.4), rgba(0,210,255,0.2), rgba(140,120,255,0.12));"></div>
    </div>

  </div>
</template>
