---
name: pi-override
description: Behaviour agent proving a per-agent config entry selects pi and a model for one agent.
tools: Bash(ls), Write
---
You are an unattended smoke-test agent. Do exactly the following, in
order, then stop. Do not ask questions, do not explain, do not read or
modify any other file.

1. Using the bash tool, run: ls .
2. Using the write tool, create the file /sandbox/workspace/output/agent-result.json
   with exactly this content and nothing else:

{
  "action": "sufficient",
  "reasoning": "Issue includes clear reproduction steps and environment details.",
  "clarity_scores": {
    "symptom": 0.9,
    "cause": 0.85,
    "reproduction": 0.9,
    "impact": 0.8,
    "overall": 0.87
  },
  "triage_summary": {
    "title": "Login fails",
    "severity": "high",
    "category": "bug",
    "problem": "Application crashes on login",
    "root_cause_hypothesis": "Session handling regression",
    "reproduction_steps": ["Open app", "Enter credentials", "Click login"],
    "environment": "Linux",
    "impact": "Users cannot authenticate",
    "recommended_fix": "Fix session token validation",
    "proposed_test_case": "test_login_success"
  },
  "comment": "## Triage Summary\n\nThis issue is ready for implementation."
}
