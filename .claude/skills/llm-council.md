# LLM Council

name: llm-council

description: "Run any question, idea, or decision through a council of 5 AI advisors who independently analyze it, peer-review each other anonymously, and synthesize a final verdict. Based on Karpathy's LLM Council methodology. MANDATORY TRIGGERS: 'council this', 'run the council', 'war room this', 'pressure-test this', 'stress-test this', 'debate this'. STRONG TRIGGERS (use when combined with a real decision or tradeoff): 'should I X or Y', 'which option', 'what would you do', 'is this the right move', 'validate this', 'get multiple perspectives', 'I can't decide', 'I'm torn between'. Do NOT trigger on simple yes/no questions, factual lookups, or casual 'should I' without a meaningful tradeoff (e.g. 'should I use markdown' is not a council question). DO trigger when the user presents a genuine decision with stakes, multiple options, and context that suggests they want it pressure-tested from multiple angles."

## Overview

The LLM Council uses five independent advisors who analyze questions from distinct perspectives, peer-review each other anonymously, and produce synthesized recommendations addressing high-stakes decisions.

## Five Advisor Perspectives

**The Contrarian** actively identifies weaknesses, fatal flaws, and what could fail, asking questions the user avoids.

**The First Principles Thinker** strips away surface assumptions, rebuilds problems from fundamentals, and questions whether you're asking the right question.

**The Expansionist** identifies overlooked upside, adjacent opportunities, and undervalued possibilities.

**The Outsider** brings zero domain context, catching obvious-to-experts blind spots and clarity problems.

**The Executor** focuses on feasibility and immediate next steps, asking "what happens Monday morning?"

## Council Process

**Step 1:** Enrich context by scanning workspace files, then frame the question neutrally with relevant details.

**Step 2:** Spawn five advisors simultaneously, each responding 150-300 words from their assigned perspective without hedging.

**Step 3:** Conduct anonymous peer review—five reviewers identify strongest responses, blind spots, and collective gaps.

**Step 4:** Chairman synthesizes findings covering agreement points, clashes, caught blind spots, clear recommendations, and single first actions.

**Step 5:** Present verdict in markdown directly in chat (no separate files).

**Step 6:** Save transcript optionally to `council-transcript-[timestamp].md`.

## When to Use

Ideal for decisions where being wrong carries significant cost: pricing strategy, pivots, positioning, hiring choices, product launches.

Avoid for factual questions, pure creation tasks, or when you already know your answer.
