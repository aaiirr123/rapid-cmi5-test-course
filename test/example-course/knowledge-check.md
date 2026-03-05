:::layout{justifyContent="center" alignItems="flex-start"}
# <span style="color: #004d7f;">Knowledge Check</span>

Test your understanding of reverse engineering fundamentals. You need **80%** to pass.
:::

:::quiz
```json
{
  "title": "Reverse Engineering Fundamentals",
  "cmi5QuizId": "quiz-re-fundamentals",
  "completionRequired": "passed",
  "moveOnCriteria": "completed-and-passed",
  "passingScore": 80,
  "questions": [
    {
      "question": "Which register holds the return value of a function in x86_64 Linux?",
      "type": "multipleChoice",
      "typeAttributes": {
        "correctAnswer": "0",
        "grading": "exact",
        "shuffleAnswers": true,
        "options": [
          { "text": "RAX", "correct": true },
          { "text": "RBX", "correct": false },
          { "text": "RDI", "correct": false },
          { "text": "RSP", "correct": false }
        ]
      },
      "cmi5QuestionId": "quiz-re-fundamentals_q1"
    },
    {
      "question": "True or False: Dynamic analysis involves executing the binary.",
      "type": "trueFalse",
      "typeAttributes": {
        "correctAnswer": "True",
        "grading": "exact",
        "options": [
          { "text": "True", "correct": true },
          { "text": "False", "correct": false }
        ]
      },
      "cmi5QuestionId": "quiz-re-fundamentals_q2"
    },
    {
      "question": "Which of the following are unsafe C functions that can lead to buffer overflows? (Select all that apply)",
      "type": "selectAll",
      "typeAttributes": {
        "correctAnswer": "0,1,3",
        "grading": "exact",
        "options": [
          { "text": "strcpy", "correct": true },
          { "text": "gets", "correct": true },
          { "text": "fgets", "correct": false },
          { "text": "sprintf", "correct": true }
        ]
      },
      "cmi5QuestionId": "quiz-re-fundamentals_q3"
    },
    {
      "question": "Match each tool to its primary use.",
      "type": "matching",
      "typeAttributes": {
        "correctAnswer": "",
        "grading": "exact",
        "matching": [
          { "option": "Ghidra", "response": "Open-source decompiler" },
          { "option": "strace", "response": "Trace system calls at runtime" },
          { "option": "Binwalk", "response": "Extract firmware and binary contents" },
          { "option": "Frida", "response": "Dynamic instrumentation framework" }
        ]
      },
      "cmi5QuestionId": "quiz-re-fundamentals_q4"
    },
    {
      "question": "What assembly instruction is commonly used to zero out a register?",
      "type": "freeResponse",
      "typeAttributes": {
        "correctAnswer": "xor",
        "grading": "exact"
      },
      "cmi5QuestionId": "quiz-re-fundamentals_q5"
    }
  ]
}
```
:::