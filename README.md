# PRD Generator

This project guides a discovery interview and then generates a Product Requirements Document (PRD) using the provided workflow.

## Quick Start

1) Open [prompt.md](prompt.md).
2) Run the interview by asking questions from [Min-Req-Questionnaire.md](Min-Req-Questionnaire.md) in order (A1 -> F3), one at a time, waiting for each answer.
3) Output the completed `CLIENT_DATA` block only.
4) Generate the PRD using [PRD-Generator-Workflow.md](PRD-Generator-Workflow.md), keeping `<<CLIENT_INPUT_REQUIRED>>` markers if required data is missing.

## How it works

1) **Interview**
   - Use the prompt instructions in [prompt.md](prompt.md).
   - Ask questions from [Min-Req-Questionnaire.md](Min-Req-Questionnaire.md) in order (A1 -> F3), one at a time.
   - Wait for each answer before proceeding.
   - For optional items, ask whether to skip.
   - Do not infer or invent answers.

2) **CLIENT_DATA output**
   - After the interview, output a completed `CLIENT_DATA` block only.

3) **Generate PRD**
   - Feed the `CLIENT_DATA` block into [PRD-Generator-Workflow.md](PRD-Generator-Workflow.md).
   - If required data is missing, keep `<<CLIENT_INPUT_REQUIRED>>` markers in the PRD.

## Files

- [prompt.md](prompt.md): Orchestration prompt for the interview and PRD generation flow.
- [Min-Req-Questionnaire.md](Min-Req-Questionnaire.md): Ordered discovery questions (A1 -> F3).
- [PRD-Generator-Workflow.md](PRD-Generator-Workflow.md): PRD generation workflow.
- [plans/](plans/): Example or generated PRDs.
