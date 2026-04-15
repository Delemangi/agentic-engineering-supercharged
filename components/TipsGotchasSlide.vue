<template>
  <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 0.7rem; margin-top: 0.8rem;">

    <div style="display: flex; flex-direction: column; gap: 0.6rem;">
      <div style="font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.18em; opacity: 0.4; margin-bottom: -0.2rem;">Do</div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(40,200,64,0.15); background: rgba(40,200,64,0.04); border-radius: 8px;">
        <span style="color: rgba(40,200,64,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">+</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Be specific with prompts</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Vague in = vague out. "Add auth" is worse than "Add JWT auth middleware to the Express API using the existing User model."</div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(40,200,64,0.15); background: rgba(40,200,64,0.04); border-radius: 8px;">
        <span style="color: rgba(40,200,64,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">+</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Use AGENTS.md</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Set project conventions once. Every session reads it. Saves you from repeating "use pnpm, not npm" forever.</div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(40,200,64,0.15); background: rgba(40,200,64,0.04); border-radius: 8px;">
        <span style="color: rgba(40,200,64,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">+</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Review diffs before accepting</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">The agent is fast, not infallible. Read the diff. Catch the edge case it missed. This is still your code, and by extension, <strong>your responsibility.</strong></div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(40,200,64,0.15); background: rgba(40,200,64,0.04); border-radius: 8px;">
        <span style="color: rgba(40,200,64,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">+</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Reference specific content</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Point to the exact file, function, or doc. "Fix the bug in src/auth/login.ts" saves tokens and avoids wrong guesses.</div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(40,200,64,0.15); background: rgba(40,200,64,0.04); border-radius: 8px;">
        <span style="color: rgba(40,200,64,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">+</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Start new sessions often</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Long sessions = bloated context = worse output. Finish a task, start fresh. Cheaper and smarter.</div>
        </div>
      </div>
    </div>

    <div style="display: flex; flex-direction: column; gap: 0.6rem;">
      <div style="font-size: 0.65rem; text-transform: uppercase; letter-spacing: 0.18em; opacity: 0.4; margin-bottom: -0.2rem;">Don't</div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(227,6,19,0.15); background: rgba(227,6,19,0.04); border-radius: 8px;">
        <span style="color: rgba(227,6,19,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">−</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Dump your entire repo</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Let the agent explore. Don't paste 50 files upfront — you'll fill the context window with noise.</div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(227,6,19,0.15); background: rgba(227,6,19,0.04); border-radius: 8px;">
        <span style="color: rgba(227,6,19,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">−</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Trust blindly</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Models hallucinate. They'll confidently write code that looks right but isn't. Run the tests. Read the output.</div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(227,6,19,0.15); background: rgba(227,6,19,0.04); border-radius: 8px;">
        <span style="color: rgba(227,6,19,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">−</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Use it for everything</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Not every task needs an agent. Bumping a dependency or fixing a typo is faster by hand. Reach for it when it saves time, not out of habit.</div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(227,6,19,0.15); background: rgba(227,6,19,0.04); border-radius: 8px;">
        <span style="color: rgba(227,6,19,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">−</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Expose secrets</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Agents read your codebase — including .env files, credentials, and API keys. They can also commit and push them. Lock down what the agent can access.</div>
        </div>
      </div>

      <div style="display: flex; gap: 0.5rem; align-items: flex-start; padding: 0.55rem 0.65rem; border: 1px solid rgba(227,6,19,0.15); background: rgba(227,6,19,0.04); border-radius: 8px;">
        <span style="color: rgba(227,6,19,0.8); font-weight: 800; font-size: 0.75rem; min-width: 0.8rem;">−</span>
        <div>
          <div style="font-size: 0.82rem; font-weight: 600;">Skip code quality tools and tests</div>
          <div style="font-size: 0.65rem; opacity: 0.45; margin-top: 0.1rem;">Linters, type checkers, tests — they catch what the agent won't. Fast and wrong scales faster than fast and right.</div>
        </div>
      </div>
    </div>

  </div>
</template>
