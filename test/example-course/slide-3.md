:::layout{justifyContent="center" alignItems="flex-start"}
## Capture the Flag

Please Use the lab environment to complete the following Capture the Flag
:::

::::layout{justifyContent="center" alignItems="flex-start"}
:::ctf
```json
{
  "title": "Binary Recon",
  "cmi5QuizId": "ctf-binary-recon",
  "completionRequired": "attempted",
  "moveOnCriteria": "completed-and-passed",
  "passingScore": 100,
  "display": {
    "shouldNumberQuestions": true
  },
  "questions": [
    {
      "title": "Strings Recon",
      "question": "A binary called `crackme` has been placed at `/opt/challenges/crackme`. Without executing it, find the hardcoded password hidden inside. Submit the password as your flag.",
      "type": "freeResponse",
      "typeAttributes": {
        "correctAnswer": "Sentinel",
        "grading": "exact"
      },
      "cmi5QuestionId": "ctf-binary-recon_q1"
    },
    {
      "title": "Register Reading",
      "question": "Run `/opt/challenges/inspector` under gdb. Set a breakpoint at `main+42` and inspect the value stored in RAX at that point. Submit the hex value (e.g. 0x1a2b).",
      "type": "freeResponse",
      "typeAttributes": {
        "correctAnswer": "0xdeadbeef",
        "grading": "exact"
      },
      "cmi5QuestionId": "ctf-binary-recon_q2"
    },
    {
      "title": "Patch the Binary",
      "question": "The binary `/opt/challenges/locked` always prints `Access Denied`. Using a hex editor or debugger, patch the conditional jump at `0x401157` to always grant access. Once patched, run the binary — it will print your flag.",
      "type": "freeResponse",
      "typeAttributes": {
        "correctAnswer": "RE{p4tch3d}",
        "grading": "exact"
      },
      "cmi5QuestionId": "ctf-binary-recon_q3"
    }
  ]
}
```
:::
::::