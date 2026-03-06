# CMI5 and xAPI Course

## Introduction to xAPI

**xAPI** (Experience API), also known as Tin Can API, is a modern e-learning specification that tracks learning experiences.

### What is an xAPI Statement?

Every learning activity is recorded as a simple statement:

**Actor** + **Verb** + **Object** \= **Statement**

Example: "John completed Introduction to Sales"

### Key Benefits

* Track learning anywhere (mobile, web, offline)
* Rich, detailed data collection
* Works with any platform
* Simple JSON format

***

## Understanding CMI5

**CMI5** combines the best of SCORM with xAPI's flexibility.

### Key Features

* Mobile-friendly
* Works across platforms
* Uses xAPI for tracking
* Simpler than SCORM

### Basic Structure

```
LMS (launches content)
  ↓
AU (your course)
  ↓
LRS (stores data)
```

***

## xAPI Statement Structure

```json
{
  "actor": {
    "name": "John Doe",
    "mbox": "mailto:john@example.com"
  },
  "verb": {
    "id": "http://adlnet.gov/expapi/verbs/completed",
    "display": { "en-US": "completed" }
  },
  "object": {
    "id": "http://example.com/course/intro",
    "definition": {
      "name": { "en-US": "Introduction Course" }
    }
  }
}
```

***

## Common xAPI Verbs

* **completed** - Finished an activity
* **passed** - Met success criteria
* **failed** - Did not meet criteria
* **attempted** - Tried an activity
* **experienced** - Encountered content

***

## CMI5 Requirements

Every CMI5 course must send these statements:

1. **initialized** - Course started
2. **completed** - Course finished
3. **terminated** - Session ended

Optional statements:

* **passed** / **failed** - If scoring is used
* **progressed** - For tracking progress

***

## SCORM vs CMI5

<table class="rc5-table"><thead><tr><th style="background-color: transparent">Feature</th><th style="background-color: transparent">SCORM</th><th style="background-color: transparent">CMI5</th></tr></thead><tbody><tr><td style="background-color: transparent">Mobile Support</td><td style="background-color: transparent">❌</td><td style="background-color: transparent">✅</td></tr><tr><td style="background-color: transparent">Offline Tracking</td><td style="background-color: transparent">❌</td><td style="background-color: transparent">✅</td></tr><tr><td style="background-color: transparent">Modern API</td><td style="background-color: transparent">❌</td><td style="background-color: transparent">✅</td></tr><tr><td style="background-color: transparent">Flexible Data</td><td style="background-color: transparent">❌</td><td style="background-color: transparent">✅</td></tr></tbody></table>

***

## Quick Start Example

### JavaScript Implementation

```javascript
// Send a completion statement
const statement = {
  actor: {
    name: "Learner Name",
    mbox: "mailto:learner@example.com"
  },
  verb: {
    id: "http://adlnet.gov/expapi/verbs/completed"
  },
  object: {
    id: "http://example.com/course/my-course"
  },
  result: {
    completion: true,
    success: true,
    score: {
      scaled: 0.95
    }
  }
};

// Send to LRS
fetch('https://lrs.example.com/xapi/statements', {
  method: 'POST',
  headers: {
    'Content-Type': 'application/json',
    'X-Experience-API-Version': '1.0.3'
  },
  body: JSON.stringify(statement)
});
```

***

## Summary

* **xAPI** tracks learning activities as simple statements
* **CMI5** provides structure for xAPI-based courses
* Both enable modern, flexible e-learning
* Easy to implement and extend

***

## Resources

* [xAPI Specification](https://github.com/adlnet/xAPI-Spec)
* [CMI5 Specification](https://github.com/AICC/CMI-5_Spec_Current)
* [xAPI Registry](https://registry.tincanapi.com/)