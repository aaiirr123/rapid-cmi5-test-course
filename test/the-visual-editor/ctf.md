## Capture the Flag (CTF)

The **Capture the Flag (CTF)** activity in Rapid CMI5 is a challenge-based assessment format commonly used in cybersecurity training. Instead of answering traditional multiple-choice questions, learners must **solve technical problems and submit the discovered "flag" as the answer**.

Flags typically represent values uncovered through tasks such as:

* network scanning
* log analysis
* reverse engineering
* cryptography
* web exploitation

This format encourages **hands-on problem solving** and simulates real-world security investigation workflows.

***

### How CTF Activities Work

A CTF activity is defined similarly to a quiz but focuses on **free-response answers** where learners submit the flag they discovered.

Typical workflow:

1. Learner reads the challenge instructions.
2. Learner performs the required investigation (e.g., using `nmap`, `curl`, or cracking a hash).
3. Learner submits the discovered flag.
4. Rapid CMI5 validates the answer and records the result.

Each challenge can include:

* a **title**
* a **technical task**
* the **expected flag**
* grading criteria

***

### Tracking with xAPI and the LRS

Just like quizzes, CTF activities generate **xAPI statements** that are sent to the Learning Record Store (LRS).

***

### Why Use CTF Challenges?

CTF activities are ideal for technical training because they:

* promote **active learning**
* simulate **real-world security tasks**
* reinforce investigative skills
* provide measurable outcomes through xAPI tracking

While quizzes measure **knowledge**, CTF challenges measure **practical skill application**.

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