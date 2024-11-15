# 1. Introduction

## 1.3 Software Requirements

## 1.4 Installing Requirements

- We need Java and XCode to run RN

- React Native's infra-structure contains...

  - App
    - Platform APIs
    - React Native native modules
    - React Native - JavaScript Interpreter
    - React Native JS Modules
      - JavaScript
      - Markup/Styling
    - and the bridges : platform APIs <-> RN native modules <-> RN
      => All this is made for our JS to talk with OS

- We are going to test our codes immediately in _our phone_ => **Expo**
  - We don't need to complie the application we made
  - There is already complied app in iOS App Store and Google Play Store
  - The only code we have to write down is **JavaScript** and **Markup/Styling** part!
  - We will download the complied application and we will send our code to the app
  - [Go to Expo](https://docs.expo.dev/get-started/create-a-project/)

## 1.5 How Does React Native Work

### React Native is a beautiful translator!

- RN is an interface between our OS and us
  - When you make a code, that code will be translated into object-C or Swift(iOS code) or Java (android code)
  - Who makes the component? Our OS like iOS or Android
  - RN sends a message to iOS and Android
  - There is no browser in RN

### RN's Working Process

Native -> Bridge -> JavaScript -> Bridge -> Native

1. (Native) Event happend - Native is the one who controls the screen
2. (Native) Collect data and notify
3. (Bridge) Serialized payload
4. (JavaScript) Process event
5. (JavaScript) Call native methods or update UI
6. (Bridge) Serialized batched response
7. (Native) Process commands
8. (Native) Update UI

In this process, JS is just the layer that developers use to send and receive the messages from the OS
