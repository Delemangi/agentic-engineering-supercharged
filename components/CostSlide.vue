<template>
  <div>
    <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-top: 0.5rem;">
      <div style="display: flex; flex-direction: column; gap: 0.15rem;">
        <div style="font-size: 0.6rem; text-transform: uppercase; letter-spacing: 0.15em; opacity: 0.4; font-weight: 600; margin-bottom: 0.2rem;">Tokens by model</div>
        <div style="display: grid; grid-template-columns: 1fr auto; gap: 0.05rem 0.5rem; align-items: baseline;">
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">Claude Opus 4.6</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">4.5M</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">GPT-5.4</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">2.1M</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">GPT-5 Nano</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">1.3M</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">Gemini 3.1 Pro</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">444K</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">MiniMax M2.5</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">154K</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">Kimi K2.5</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">102K</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">GPT-5.4 Mini</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">77K</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">MiniMax M2.7</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">22K</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">Claude Sonnet 4.6</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">11K</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.7;">GPT-5 Mini</span>
          <span style="font-size: 0.55rem; font-family: monospace; opacity: 0.5; text-align: right;">6K</span>
        </div>
      </div>
      <div style="display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 0.3rem;">
        <div style="display: flex; align-items: baseline; gap: 0.8rem; line-height: 0.9; margin-bottom: 0.5rem;">
          <span style="font-size: 3.5rem; font-weight: 900; letter-spacing: -0.04em;">~8.7M</span>
          <span style="font-size: 2rem; font-weight: 700; opacity: 0.5;">tokens</span>
        </div>
        <div style="display: flex; flex-direction: column; gap: 0.5rem;">
          <div style="display: flex; align-items: baseline; gap: 0.5rem;">
            <span style="font-size: 0.75rem; opacity: 0.4; min-width: 7rem; text-align: right;">Provider cost</span>
            <span style="font-size: 2rem; font-weight: 800; letter-spacing: -0.03em;">~$1,220</span>
          </div>
          <div style="display: flex; align-items: baseline; gap: 0.5rem;">
            <span style="font-size: 0.75rem; opacity: 0.4; min-width: 7rem; text-align: right;">API cost</span>
            <span style="font-size: 2rem; font-weight: 800; letter-spacing: -0.03em;">~$120</span>
          </div>
          <div style="display: flex; align-items: baseline; gap: 0.5rem;">
            <span style="font-size: 0.75rem; opacity: 0.4; min-width: 7rem; text-align: right;">My cost</span>
            <span style="font-size: 2rem; font-weight: 900; letter-spacing: -0.03em;">$0</span>
            <span style="font-size: 1.2rem; font-weight: 700; opacity: 0.4;">*</span>
          </div>
        </div>
        <div style="font-size: 0.65rem; opacity: 0.25; margin-top: 1rem; font-style: italic;">* subscriptions, no per-token billing</div>
      </div>
    </div>
  </div>
</template>
