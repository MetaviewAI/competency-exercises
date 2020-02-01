## Calendly Integration

### Background

At Metaview, we need to know when our customers' interviews are scheduled so that we can be present. Typically, we're made aware of scheduled interviews by having our customers have interview@metaview.ai automatically added to the calendar invite. However, sometimes there's no automatic way to add us to the invite; our customers have to do it manually. This manual step is error-prone (e.g. easy to forget) and suboptimal.

### Product Statement

Some of our customers schedule their phone screen interviews using [Calendly](https://calendly.com/). With [Calendly's Basic plan](https://calendly.com/pages/pricing), there's no automatic way to add an additional attendee to every scheduled event. As such, we need to have a Calendly integration that enables us to automatically know when an interview has been scheduled or canceled.

**In this exercise, we want you to work on the full stack implementation of a product that has a Calendly integration in order to solve the issue above.**

We need this product to have the following characteristics:

1. **🤗 Delightful:** The customer experience must be delightful and as frictionless as possible.
2. **🔨 Resilient:** We need to maximally reduce the chance of us missing a scheduled interview.
3. **👀 Observable:** When issues arise (e.g. the application crashes), we'd need to have enough information so that our debugging efforts are not entirely blind.

### Scope and Expectations

The scope of the implementation should be for the quickest shippable implementation of this product. We appreciate this exercise is open-ended. We don't expect you to spend more than 8 hours on it.

### Evaluation

We're using this exercise as a means to learn more about your:

- **🐙 Practical technical breadth:** Ability to design and implement an end-to-end product satisfying the desired core characteristics.
- **🚀 Knack for making the right trade-offs:** Ability to know when it makes sense to take the quick and dirty vs. the scalable approach.
