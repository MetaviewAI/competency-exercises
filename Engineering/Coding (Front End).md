## Problem

At Metaview, there are humans, Data Annotators (DAs), in the loop when processing data. We think it’s right for this to be the case for the foreseeable future.

Let's assume once the audio for an interview has been transcribed, using one of the many potential services (e.g. [Temi](https://www.temi.com), [AWS Transcribe](https://aws.amazon.com/transcribe/), [Google Speech-to-Text](https://cloud.google.com/speech-to-text/)), our DAs need to modify the transcription to:

- Ensure the speaker diarization is 100% accurate.
- Ensure the transcription of the interviewer and candidate questions are as close to 100% accurate as possible.
- Ensure relevant interviewer and candidate questions are labelled with specific categories (e.g. problem solving, team composition)

In order to have maximal control over this process, we need to develop our own internal tooling and products. In the long run, we want our DAs to be able to do more cleansing and labelling in the same amount of time.
In this exercise, we want you to write a design doc for the full stack implementation of such product.

**In this exercise, we want you to build the front end on a product that'll help our DAs to the tasks above. You can use any technology you want but it would be preferable if you used React and/or TypeScript.**

*Please don't spend more than 10 hours on this task.*