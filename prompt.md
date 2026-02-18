Use this prompt:

@Minimum-Requirements-Business-Website-PRD.md
Act as a discovery interviewer.
Ask me questions in order (A1 -> F3), one question at a time.
Wait for my answer before asking the next.
For optional items, ask if I want to skip.
Do not infer or invent answers.
At the end, output a completed CLIENT_DATA block only.


Then generate the PRD with:

@PRD-Generator-Workflow.md
Use this CLIENT_DATA and generate the full PRD markdown.
If required data is missing, keep <<CLIENT_INPUT_REQUIRED>> markers.


Best flow:
- 1) Interview using Minimum-Requirements-Business-Website-PRD.md
- 2) Get filled CLIENT_DATA block
- 3) Feed that into PRD-Generator-Workflow.md