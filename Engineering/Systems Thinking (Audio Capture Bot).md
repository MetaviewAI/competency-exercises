## Audio Capture Bot

### Background

At Metaview, we give our customers their interview analytics no matter what the interview medium. Some interviews are in person, some are over video conference, and some are on the phone. As such, we need to have tools/products that enable us to capture the audio in any of these scenarios. Since we do our analysis on audio, we *don't* need these tools/products to capture the video, even if possible.

### Product

**In this exercise, we want you to write a design doc<sup>1</sup> for the full stack implementation of a product that captures the audio in video conferences.**

We need this product to have the following characteristics:

1. **Delightful:** The customer experience must be delightful and as frictionless as possible.
2. **Extensible:** Amongst our current customers, [Google Meet](https://meet.google.com) is the most common video conferencing tool. However, we'd need this product to be easily extended to support other types of providers (e.g. [Zoom](https://zoom.us/)) as and when required.
3. **Observable:** When issues arise (e.g. we miss audio-minutes), we'd need to have enough information so that our debugging efforts are not entirely blind.

### Scope and Expectations

The scope of the design doc should be for the the quickest shippable implementation of this product. We appreciate this exercise is open-ended. We don't expect you to spend more than 6-8 hours on it.

### Evaluation

We're using this exercise as a means to learn more about your way of:

- Designing an end-to-end system satisfying the desired core characteristics.
- Communicating your design.
- Finding the balance between an advanced implementation that takes ages to ship vs. a less advanced implementation that's quicker to ship.

<br />
<br />

<sup>1</sup> Feel free to write the document however you want. In case it's helpful, [here's one opinion on how to write a software design doc](https://medium.freecodecamp.org/how-to-write-a-good-software-design-document-66fcf019569c).
