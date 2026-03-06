## Individual Training Scenarios

## Cyber Training Scenarios

A **Cyber Training Scenario** is an interactive learning environment that connects training content to a live **cyber range infrastructure**. Instead of only reading material or answering questions, learners can access real systems and practice tasks in a controlled environment.

Scenarios are commonly used for exercises such as:

* network reconnaissance
* incident response
* malware analysis
* system administration
* penetration testing

Each scenario provisions or connects the learner to one or more **virtual machines or services** inside a cyber range.

***

### How Scenarios Work

When a learner launches a scenario from a Rapid CMI5 course, RangeOS communicates with the range infrastructure to provide the learner with the necessary resources.

Typical workflow:

1. The learner launches the **scenario activity**.
2. RangeOS identifies the associated **cyber range environment**.
3. The system allocates the learner access to the required machines or services.
4. Console access links appear in the training interface.
5. The learner performs tasks inside the range environment.

These environments are isolated and temporary, ensuring learners can safely experiment without affecting other systems.

***

### Console Access

RangeOS scenarios can provide access to multiple types of systems through integrated consoles. These consoles are embedded directly in the training interface so learners do not need external tools.

Common console types include:

This allows learners to interact with the training environment in real time while following instructions from the course.

***

### Why Use Scenarios?

Cyber training scenarios provide a bridge between **theoretical knowledge and hands-on practice**. They allow learners to:

* apply skills in realistic environments
* safely practice offensive and defensive techniques
* gain experience with real tools and systems
* complete guided cyber exercises

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