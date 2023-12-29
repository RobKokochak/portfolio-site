---
title: "Rob Kokochak - Lightweight Metronome"
summary: "When I couldn't find a no-frills, lightweight metronome for macOS, I decided to build my own using SwiftUI."
image: /images/metronome-screenshots.jpg
imageAlt: "Screenshot of app"
tech:
  - "SwiftUI"
  - "Xcode"
siteUrl: "#"
repoUrl: "#"
---

<u><a href="https://github.com/RobKokochak/LightweightMetronome" target="_blank">Link to Github Repo</a></u>

## **Problem Statement**

Create a simple and efficient metronome for macOS. 

There are no shortage of metronome apps for iOS. But as someone who practices near the computer, I needed something quick and easy to pull up without opening a DAW. While I could use my phone, I have often found my phone battery is drained by the end of a practice session. iOS metronomes tend to have an abundance of features, but I only need the most fundamental in a metronome: keep time. 

Sometimes you just want a tool that does one thing very well. I don't want to be overwhelmed with functionality, but I do want the features that the app is designed to fulfill to be efficient and to work very well.

## **Technologies Used**

Xcode, SwiftUI

## **Challenges Faced**

**Real-Time Audio Processing**

There are plenty of tools and libraries for triggering sound samples, But I needed those samples to be triggered at extremely precise intervals, and make those intervals controllable by the user. I managed to find a solution using a high-accuracy timer in combination with the audio engine library provided by SwiftUI, which then triggers the metronome sound sample.  

## **Lessons Learned**

**Audio Processing**

Through this project, I am learning that native low level audio processing is difficult. Documentation is few and far-between, especially for native Apple hardware. Regardless, my end-goal is to have more granular control over the sound generation and interval time, and that will likely require the use of a lower level library like AudioKit or CoreAudio.

**Ongoing**

Development, testing and deployment to the App Store are still in the works. 
