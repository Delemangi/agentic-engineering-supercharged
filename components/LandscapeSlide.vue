<template>
  <div>
    <div style="display: flex; flex-direction: column; gap: 1.2rem; margin-top: 1.5rem;">

      <div style="display: flex; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); padding-bottom: 1.2rem;">
        <div style="width: 130px; font-weight: 800; color: #E30613; font-size: 1rem; text-transform: uppercase; letter-spacing: 2px; line-height: 1.2;">
          Coding<br/>Agents
        </div>
        <div style="flex: 1; display: flex; flex-wrap: wrap; gap: 0.4rem; font-size: 0.75rem;">
          <NcBadge type="accent" v-for="t in ['OpenCode', 'Pi', 'GitHub Copilot', 'Cursor', 'Claude Code', 'Windsurf', 'Cline', 'Aider', 'Augment Code', 'Codex CLI', 'Gemini CLI', 'Continue', 'Roo Code', 'JetBrains AI', 'Amazon Q', 'Sourcegraph Cody', 'Tabnine', 'Supermaven', 'Zed AI', 'Kiro', 'Plandex']" :key="t">{{ t }}</NcBadge>
        </div>
      </div>

      <div style="display: flex; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); padding-bottom: 1.2rem;">
        <div style="width: 130px; font-weight: 800; color: #E30613; font-size: 1rem; text-transform: uppercase; letter-spacing: 2px; line-height: 1.2;">
          Models
        </div>
        <div style="flex: 1; display: flex; flex-wrap: wrap; gap: 0.4rem; font-family: monospace;">
          <span v-for="m in ['Claude Sonnet 4.6', 'Claude Sonnet 4.5', 'Claude Opus 4.6', 'GPT-5.4', 'o3', 'GPT-4o', 'Gemini 2.5 Flash', 'Gemini 3.1 Pro', 'DeepSeek R1', 'Codestral', 'Qwen3-Coder']" :key="m" style="padding: 0.2rem 0.6rem; background: rgba(255,255,255,0.03); border: 1px solid rgba(255,255,255,0.1); border-radius: 4px; font-size: 0.75rem; color: #ddd;">{{ m }}</span>
        </div>
      </div>

      <div style="display: flex; align-items: center; border-bottom: 1px solid rgba(255,255,255,0.05); padding-bottom: 1.2rem;">
        <div style="width: 130px; font-weight: 800; color: #E30613; font-size: 1rem; text-transform: uppercase; letter-spacing: 2px; line-height: 1.2;">
          Subs
        </div>
        <div style="flex: 1; display: flex; flex-wrap: wrap; gap: 0.7rem;">
          <span v-for="s in ['Cursor Pro', 'GitHub Copilot', 'Windsurf Pro', 'JetBrains AI Pro', 'Augment', 'Tabnine Pro', 'Amazon Q Pro', 'OpenCode Go', 'OpenCode Zen']" :key="s" style="font-weight: 600; font-size: 0.9rem; border-bottom: 3px solid rgba(227,6,19,0.4); padding-bottom: 2px;">{{ s }}</span>
        </div>
      </div>

      <div style="display: flex; align-items: center;">
        <div style="width: 130px; font-weight: 800; color: #E30613; font-size: 1rem; text-transform: uppercase; letter-spacing: 2px; line-height: 1.2;">
          API<br/>Access
        </div>
        <div style="flex: 1; display: flex; flex-wrap: wrap; gap: 0.4rem;">
          <span v-for="a in ['OpenRouter', 'Anthropic API', 'OpenAI API', 'Google AI Studio', 'AWS Bedrock', 'Azure OpenAI', 'Fireworks', 'Together AI']" :key="a" style="padding: 0.2rem 0.7rem; border: 1px solid rgba(227,6,19,0.3); border-radius: 20px; font-size: 0.7rem; text-transform: uppercase; letter-spacing: 1px; background: rgba(227,6,19,0.05);">{{ a }}</span>
        </div>
      </div>

    </div>

    <div style="margin-top: 0.75rem; padding: 0.5rem 0.75rem; border: 1px solid rgba(255,200,50,0.3); background: rgba(255,200,50,0.06); border-radius: 4px; font-size: 0.65rem; color: rgba(255,220,100,0.7); line-height: 1.4;">
      ⚠️ This slide may contain information that is out of date. Reason: <span style="font-style: italic;">it has been more than 24 hours since it was last edited.</span> <span style="opacity: 0.5;">[update]</span>
    </div>
  </div>
</template>
