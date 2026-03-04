# Activities&#x20;

## Quizzes&#x20;

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

## Capture the flags

:::ctf
{
"title": "Network Recon Challenge",
"cmi5QuizId": "ctf-network-recon",
"completionRequired": "attempted",
"moveOnCriteria": "completed-and-passed",
"passingScore": 100,
"display": {
"shouldNumberQuestions": true
},
"questions": \[
{
"title": "Open Port",
"question": "You've been given access to a target machine at 10.0.0.1. Run an nmap scan and find the only open port. Submit the port number as your flag.",
"type": "freeResponse",
"typeAttributes": {
"correctAnswer": "8080",
"grading": "exact"
},
"cmi5QuestionId": "ctf-network-recon\_q1"
},
{
"title": "Hidden Header",
"question": "Make a GET request to http://10.0.0.1:8080. There is a secret value hidden in the response headers. What is the value of the X-Secret-Token header?",
"type": "freeResponse",
"typeAttributes": {
"correctAnswer": "Sentinel",
"grading": "exact"
},
"cmi5QuestionId": "ctf-network-recon\_q2"
},
{
"title": "Hash Cracking",
"question": "The following MD5 hash was found in a leaked database: 5f4dcc3b5aa765d61d8327deb882cf99. Crack the hash and submit the plaintext password.",
"type": "freeResponse",
"typeAttributes": {
"correctAnswer": "password",
"grading": "exact"
},
"cmi5QuestionId": "ctf-network-recon\_q3"
}
]
}
:::

## Individual Training Scenarios

:::scenario
```json
{
 "uuid": "772e9281-59e8-4867-be35-4c147caa1ca6",
 "name": "Demo Auto Graders - AT",
 "promptClass": false,
 "moveOnCriteria": "completed",
 "rc5id": "20260304172746-d10af030-2be4-4705-8595-9382f892262a"
}
```
:::