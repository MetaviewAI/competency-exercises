## Problem

At Metaview, we strive to give our customers their interview analytics no matter what the interview medium. Some interviews are in person, some are over video conference, and some are on the phone. Video conferences are the most common medium for interviews. So, one of our highest priorities is to be able to reliably record video conferences.

**In this exercise, we want you to write a [design doc](https://medium.freecodecamp.org/how-to-write-a-good-software-design-document-66fcf019569c) for the full stack implementation of a product that'll allow us to record video conferences.**

We need this product to be:

1. **Extensible:** For example, amongst our current customers, [Google Meet](https://meet.google.com) is the most common video conferencing tool. However, we'd need this product to be easily extended to support other types of providers (e.g. [Zoom](https://zoom.us/)) as and when required.
2. **Reliable:** For example, we'd need this product to reliably record video conferences and minimise the number of audio-minutes we miss.
3. **Observable:** For example, we'd need to be able to have insight into which video conference sessions are coming up, currently being recorded, and have been recorded. When issues arise (e.g. we miss audio-minutes), we'd also need to have enough information so that our debugging efforts are not entirely blind.

