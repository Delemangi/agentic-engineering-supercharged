<template>
  <div>
    <div style="font-size: 0.92rem; opacity: 0.7; line-height: 1.5;">A model does not see text. It sees <strong>chunks</strong> called tokens.</div>

    <div style="display: grid; grid-template-columns: 1.3fr 1fr; gap: 1.2rem; margin-top: 0.9rem; align-items: start;">
      <div>
        <div style="padding: 1rem; background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); border-radius: 10px;">
          <div style="font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.18em; opacity: 0.4; margin-bottom: 0.65rem;">Tokenizer</div>
          <div style="display: inline-flex; flex-wrap: wrap; gap: 0; font-family: 'Courier New', Courier, monospace; font-size: 0.95rem; line-height: 1;">
            <span style="padding: 0.35rem 0; background: rgba(227,6,19,0.35); color: #fff;"><span style="padding: 0 0.3rem;">Many</span></span><span style="padding: 0.35rem 0; background: rgba(0,210,255,0.3); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;words</span></span><span style="padding: 0.35rem 0; background: rgba(255,180,50,0.35); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;map</span></span><span style="padding: 0.35rem 0; background: rgba(140,120,255,0.35); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;to</span></span><span style="padding: 0.35rem 0; background: rgba(70,200,120,0.3); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;one</span></span><span style="padding: 0.35rem 0; background: rgba(255,120,180,0.35); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;token</span></span><span style="padding: 0.35rem 0; background: rgba(227,6,19,0.35); color: #fff;"><span style="padding: 0 0.3rem;">,</span></span><span style="padding: 0.35rem 0; background: rgba(0,210,255,0.3); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;but</span></span><span style="padding: 0.35rem 0; background: rgba(255,180,50,0.35); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;some</span></span><span style="padding: 0.35rem 0; background: rgba(140,120,255,0.35); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;don</span></span><span style="padding: 0.35rem 0; background: rgba(70,200,120,0.3); color: #fff;"><span style="padding: 0 0.3rem;">'t</span></span><span style="padding: 0.35rem 0; background: rgba(255,120,180,0.35); color: #fff;"><span style="padding: 0 0.3rem;">:</span></span><span style="padding: 0.35rem 0; background: rgba(227,6,19,0.35); color: #fff;"><span style="padding: 0 0.3rem;">&nbsp;ind</span></span><span style="padding: 0.35rem 0; background: rgba(0,210,255,0.3); color: #fff;"><span style="padding: 0 0.3rem;">iv</span></span><span style="padding: 0.35rem 0; background: rgba(255,180,50,0.35); color: #fff;"><span style="padding: 0 0.3rem;">idu</span></span><span style="padding: 0.35rem 0; background: rgba(140,120,255,0.35); color: #fff;"><span style="padding: 0 0.3rem;">ally</span></span><span style="padding: 0.35rem 0; background: rgba(70,200,120,0.3); color: #fff;"><span style="padding: 0 0.3rem;">.</span></span>
          </div>
          <div style="margin-top: 0.6rem; font-size: 0.72rem; opacity: 0.45;">17 tokens</div>
        </div>
        <div style="margin-top: 0.85rem; padding: 0.85rem 1rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.06); border-radius: 8px;">
          <div style="font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.18em; opacity: 0.4; margin-bottom: 0.55rem;">Claude Opus 4.6 — per 1M tokens</div>
          <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.35rem 0.8rem; font-size: 0.78rem;">
            <div style="display: flex; justify-content: space-between;"><span style="opacity: 0.6;">Input</span><span style="font-family: monospace; font-weight: 700;">$5.00</span></div>
            <div style="display: flex; justify-content: space-between;"><span style="opacity: 0.6;">Output</span><span style="font-family: monospace; font-weight: 700;">$25.00</span></div>
            <div style="display: flex; justify-content: space-between;"><span style="opacity: 0.6;">Cache write</span><span style="font-family: monospace; font-weight: 700;">$6.25</span></div>
            <div style="display: flex; justify-content: space-between;"><span style="opacity: 0.6;">Cache read</span><span style="font-family: monospace; font-weight: 700; color: rgba(70,200,120,0.9);">$0.50</span></div>
          </div>
          <div style="margin-top: 0.4rem; font-size: 0.68rem; opacity: 0.45; line-height: 1.4;">Cache write = first time context is stored. Cache read = reusing it on subsequent calls.</div>
          <div style="margin-top: 0.45rem; font-size: 0.68rem; opacity: 0.4; line-height: 1.35;">Tokens are expensive. Subscriptions offer heavily subsidized rates — far cheaper per token than the API pricing.</div>
        </div>
      </div>
      <div>
        <div style="font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.18em; opacity: 0.4; margin-bottom: 0.55rem;">In practice</div>
        <div style="display: flex; flex-direction: column; gap: 0.4rem;">
          <div style="display: flex; justify-content: space-between; align-items: center; padding: 0.45rem 0.7rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.06); border-radius: 6px; font-size: 0.78rem;">
            <span style="opacity: 0.7;">"Fix the login bug"</span>
            <span style="font-family: monospace; font-weight: 700; color: rgba(70,200,120,0.9);">~6</span>
          </div>
          <div style="display: flex; justify-content: space-between; align-items: center; padding: 0.45rem 0.7rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.06); border-radius: 6px; font-size: 0.78rem;">
            <span style="opacity: 0.7;">Reading a 200-line file</span>
            <span style="font-family: monospace; font-weight: 700; color: rgba(255,180,50,0.9);">~800</span>
          </div>
          <div style="display: flex; justify-content: space-between; align-items: center; padding: 0.45rem 0.7rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.06); border-radius: 6px; font-size: 0.78rem;">
            <span style="opacity: 0.7;">System prompt + skills</span>
            <span style="font-family: monospace; font-weight: 700; color: rgba(255,120,180,0.9);">~4k</span>
          </div>
          <div style="display: flex; justify-content: space-between; align-items: center; padding: 0.45rem 0.7rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.06); border-radius: 6px; font-size: 0.78rem;">
            <span style="opacity: 0.7;">One agent loop turn</span>
            <span style="font-family: monospace; font-weight: 700; color: rgba(227,6,19,0.9);">~15-50k</span>
          </div>
          <div style="display: flex; justify-content: space-between; align-items: center; padding: 0.45rem 0.7rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.06); border-radius: 6px; font-size: 0.78rem;">
            <span style="opacity: 0.7;">Full coding session</span>
            <span style="font-family: monospace; font-weight: 700; color: rgba(227,6,19,0.9);">~500k+</span>
          </div>
        </div>
        <div style="margin-top: 0.65rem; font-size: 0.72rem; opacity: 0.4; line-height: 1.4;">Tokens add up fast. Every file read, every tool call, every context reconstruction — it all counts.</div>
      </div>
    </div>
  </div>
</template>
