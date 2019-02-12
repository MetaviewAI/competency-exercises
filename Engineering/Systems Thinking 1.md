## Problem

At Metaview, there are humans, Data Annotators (DAs), in the loop when processing data. We think it’s right for this to be the case for the foreseeable future.

Let's assume once the audio for an interview has been transcribed, using one of the many potential services (e.g. [Temi](https://www.temi.com), [AWS Transcribe](https://aws.amazon.com/transcribe/), [Google Speech-to-Text](https://cloud.google.com/speech-to-text/)), our DAs need to modify the transcription to:

- Ensure the [speaker diarisation](https://en.wikipedia.org/wiki/Speaker_diarisation) is 100% accurate.
- Ensure the transcription of the interviewer and candidate questions are as close to 100% accurate as possible.
- Ensure relevant interviewer and candidate questions are labelled with specific categories (e.g. problem solving, team composition)

In this data processing pipeline, we want to maximise:

1. **Correctness:** We need to know what changes were made and by whom. We can then perhaps assumptions about the correctness of the changes that are made by DAs.
2. **Predictability:** We need to be able to predict how long it'll take us to process a transcription.
3. **Velocity:** We need our Data Annotators to experience as little friction as possible when cleaning and labelling data.

In order to have maximal control over this process, we need to develop our own internal tooling and products. In the long run, we want our DAs to be able to do more cleansing and labelling in the same amount of time.

**In this exercise, we want you to write a [design doc](https://medium.freecodecamp.org/how-to-write-a-good-software-design-document-66fcf019569c) for the full stack implementation of such product.**