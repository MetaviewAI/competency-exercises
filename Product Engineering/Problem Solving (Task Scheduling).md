## 📅 Task Scheduling

### Context

At Metaview, we have a complex data pipeline that turns raw data into data that's useful to our customers. An important part of our data pipeline is the process of humans manually labelling data. This is done by our group of Data Annotators. There are a variety of annotation tasks, and each Data Annotator is qualified to do one or more types of tasks. Some of these tasks are dependent on other tasks.

### Exercise

**In this exercise, we want you to implement an application that coordinates the scheduling/allocation of a large number of tasks.**

We will define a list of tasks, and their dependencies, in a JSON file that looks like this:

```json
{
    "tasks": [
        {
	    "taskId": 0,
            "taskType": "speaker-identification",
            "expectedTurnaroundTime": 50,
        },
        {
	    "taskId": 1,
            "taskType": "question-detection",
            "expectedTurnaroundTime": 100,
        },
        {
	    "taskId": 2,
            "taskType": "speech-splitting",
            "expectedTurnaroundTime": 800,
            "dependsOn": [0]
        },
        {
	    "taskId": 3,
            "taskType": "closed-question-detection",
            "expectedTurnaroundTime": 50,
            "dependsOn": [2]
        }
    ]
}
```

`taskType` is a unique identifier for a type of annotation task. `expectedTurnaroundTime` is the amount of time we expect the task to take a Data Annotator. And, `dependsOn` is a set of task IDs that must first be completed before a particular task can be started.

We will then also specify the Data Annotators and their qualification like so:

```json
{
    "annotators": [
        {
            "name": "Riley",
            "qualifications": ["speaker-identification", "question-detection", "closed-question-detection"],
        },
        {
            "name": "Jordan",
            "qualifications": ["question-detection", "speech-splitting"],
        },
        {
            "name": "Parker",
            "qualifications": ["question-detection", "closed-question-detection"],
        }
    ]
}
```

`name` is a Data Annotator's unique identifier. `qualifications` is a set of task types that a Data Annotator is able to complete.

For this task, we want you to implement an application that reads those two files, and then emits an ordered scheduling plan that manages all the constraints and dependencies. The goal is to execute the full list of tasks as quickly as possible. For example, based on the input data above, the schedule may look something like:

```json
{
    "schedule": [
        {
            "annotatorName": "Riley",
            "taskId": 0
        },
        {
            "annotatorName": "Jordan",
            "taskId": 2
        },
        {
            "annotatorName": "Parker",
            "taskId": 1
        },
        {
            "annotatorName": "Parker",
            "taskId": 3
        }
    ]
}
```

### **Expectations**

To complete this exercise, we expect you to use whatever tools you find appropriate and that you would choose to use if you were solving this problem in a day-to-day setting at work. We would anticipate some amount of research being useful to understand the tradeoffs involved. Python and/or Typescript are what we use at Metaview for development, but other reasonable technologies are fine for this exercise too.

Please include the following supporting material:

- A brief discussion of your approach, and all the assumptions and tradeoffs that you've made.
- Instructions on how to build and execute the application.
- Any test code, or test data sets you generated.
- References to other materials as appropriate.

Please do not spend more than the equivalent of a normal work-day on this exercise, and feel free to ask questions. While we would love to see a completed product, we expect that your final solution may not be completely “finished” in the available time.

### **Evaluation**

We're using this exercise to learn more about your:

- 🤔 **Technical approach:** We want to see how you approach and research a complex technical problem.
- 📝 **Communication:** We want to see how you communicate about your work.
- **🚀 Knack for making the right trade-offs:** We want to see how you navigate decisions in circumstances where there are multiple right answers.

Enjoy! 😄
