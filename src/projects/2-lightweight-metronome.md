---
title: "Lightweight Metronome"
summary: "When I couldn't find a no-frills, lightweight native metronome app for macOS, I decided to build my own using SwiftUI."
image: /images/metronome-screenshot.png
imageAlt: "Screenshot of app"
tech:
  - "SwiftUI"
  - "Xcode"
siteUrl: "#"
repoUrl: "#"
---

<u><a href="https://www.dropbox.com/scl/fi/s8tcrmhs1lra424p98kz4/Lightweight-Metronome.zip?rlkey=zjbmzcyddv63548n2mwu6qbej&dl=0" target="_blank">Link to Download (must be on macOS Sonoma 14.0 or higher)</a></u>

<u><a href="https://github.com/RobKokochak/LightweightMetronome" target="_blank">Link to Github Repo</a></u>

<p>
  <img class="logo-preview" src="/images/metronome-logo-512.png">
</p>

## **Problem Statement**

Create a simple and efficient metronome for macOS. 

There are no shortage of metronome apps for iOS. But as someone who practices near the computer, I needed something quick and easy to pull up on the computer without opening a DAW. While I could use my phone, I have often found my phone battery is drained by the end of a practice session. iOS metronomes tend to have an abundance of features, but I only need the most fundamental in a metronome: keep time. 

Sometimes you just want a tool that does one thing very well. I don't want to be overwhelmed with functionality, but I do want the features that the app is designed to fulfill to be efficient and to work very well.

## **Technologies Used**

Xcode, SwiftUI

## **Challenges Faced**

- **High Accuracy Sound Triggering**

There are plenty of tools and libraries for triggering sound samples, But I needed those samples to be triggered at extremely precise intervals, and make those intervals controllable by the user. I managed to find a solution using a high-accuracy timer in combination with the audio engine library provided by SwiftUI, which then triggers the metronome sound sample.  

## **Lessons Learned**

- **Audio Processing and Low-Level Timer Control**

Through this project, I've learned that granular control of audio processing is difficult. Documentation is few and far-between, especially for native Apple hardware. 

- **Apple Development**

Developing for the Apple ecosystem has its quirks, including a clunky Xcode experience and the infamous $99 subscription to get your apps notarized. While there are certainly frustrations, seeing the app you built become a part of your daily workflow and sharing that utility with others is a great feeling.

- **Logo Design**

Designing a proper logo from scratch was one of the most interesting challenges in building the app. I learned that while iOS handles the polish of the logo, macOS requires you to export multiple resolutions and implement design decisions like border radius yourself. 
