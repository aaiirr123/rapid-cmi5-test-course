## Quizzes&#x20;

## Why Use Quizzes in Rapid CMI5?

Quizzes play a critical role in validating learner understanding and measuring training effectiveness. In **Rapid CMI5**, quizzes are not just simple assessments — they are tightly integrated with the **cmi5 specification** and the **xAPI Learning Record Store (LRS)**.

This means every quiz interaction can be tracked, analyzed, and reported across systems in a standardized way.

***

### 🎯 Purpose of Quizzes

Quizzes in Rapid CMI5 serve several important purposes:

<table class="rc5-table"><thead><tr><th style="background-color: transparent">Purpose</th><th style="background-color: transparent">Description</th></tr></thead><tbody><tr><td style="background-color: transparent"></td><td style="background-color: transparent">Confirm that learners understand the key concepts presented in the course.</td></tr><tr><td style="background-color: transparent"></td><td style="background-color: transparent">Enforce passing criteria before allowing learners to move to the next AU (Assignable Unit).</td></tr><tr><td style="background-color: transparent"></td><td style="background-color: transparent">Capture scores, completion status, and pass/fail results.</td></tr><tr><td style="background-color: transparent"></td><td style="background-color: transparent">Send detailed learning activity data to an LRS using xAPI statements.</td></tr></tbody></table>

***

### 📊 How Rapid CMI5 Tracks Quiz Activity

When a learner interacts with a quiz, **xAPI statements are generated and sent to the Learning Record Store (LRS)**. These statements describe what the learner did and the outcome of the interaction.

For example, Rapid CMI5 may generate statements like:

Each statement includes additional metadata such as:

* learner identity
* quiz ID
* question ID
* selected answers
* score
* timestamp
* completion status

This data is stored in the **LRS**, allowing organizations to analyze learning behavior beyond the LMS.

***

:::quiz
```json
{
  "title": "Cybersecurity Fundamentals",
  "cmi5QuizId": "quiz-cybersec-101",
  "completionRequired": "passed",
  "moveOnCriteria": "completed-and-passed",
  "passingScore": 80,
  "questions": [
    {
      "question": "What type of attack floods a server with traffic to make it unavailable?",
      "type": "multipleChoice",
      "typeAttributes": {
        "correctAnswer": "0",
        "grading": "exact",
        "shuffleAnswers": true,
        "options": [
          { "text": "DDoS", "correct": true },
          { "text": "Phishing", "correct": false },
          { "text": "Spoofing", "correct": false },
          { "text": "Keylogging", "correct": false }
        ]
      },
      "cmi5QuestionId": "quiz-cybersec-101_q1"
    },
    {
      "question": "True or False: HTTPS encrypts data in transit.",
      "type": "trueFalse",
      "typeAttributes": {
        "correctAnswer": "True",
        "grading": "exact",
        "options": [
          { "text": "True", "correct": true },
          { "text": "False", "correct": false }
        ]
      },
      "cmi5QuestionId": "quiz-cybersec-101_q2"
    },
    {
      "question": "Which of the following are examples of multi-factor authentication? (Select all that apply)",
      "type": "selectAll",
      "typeAttributes": {
        "correctAnswer": "0,2",
        "grading": "exact",
        "options": [
          { "text": "SMS code", "correct": true },
          { "text": "Password", "correct": false },
          { "text": "Fingerprint", "correct": true },
          { "text": "Username", "correct": false }
        ]
      },
      "cmi5QuestionId": "quiz-cybersec-101_q3"
    },
    {
      "question": "Match each attack type to its description.",
      "type": "matching",
      "typeAttributes": {
        "correctAnswer": "",
        "grading": "exact",
        "matching": [
          { "option": "Phishing", "response": "Deceptive email to steal credentials" },
          { "option": "Ransomware", "response": "Encrypts files and demands payment" },
          { "option": "Rootkit", "response": "Hides malware from the OS" },
          { "option": "Brute Force", "response": "Tries all password combinations" }
        ]
      },
      "cmi5QuestionId": "quiz-cybersec-101_q4"
    },
    {
      "question": "What port does HTTPS use by default?",
      "type": "number",
      "typeAttributes": {
        "correctAnswer": 443,
        "grading": "exact"
      },
      "cmi5QuestionId": "quiz-cybersec-101_q5"
    }
  ]
}
```
:::