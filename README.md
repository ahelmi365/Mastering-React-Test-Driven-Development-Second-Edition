# Mastering React Test Driven Development, Second Edition

This is the companion repository for the book _Mastering React Test-Driven Development_ by [Daniel Irvine](https://danielirvine.com), published by Packt and due for release in August 2022.

* [How to buy the book](#how-to-buy-the-book)
* [What's in this repository](#whats-in-this-repository)
* [What's not in this repository](#whats-not-in-this-repository)
* [How to use this repository](#how-to-use-this-repository)
  * [If you don't have the book](#if-you-dont-have-the-book)
  * [Following along with the book](#following-along-with-the-book)
  * [Running tests](#running-tests)
  * [Building and running the app](#building-and-running-the-app)
  * [Other commands you can run](#other-commands-you-can-run)
  * [Viewing the commit history](#viewing-the-commit-history)
* [Troubleshooting](#troubleshooting)
* [Other topics](#other-topics)
  * [Why did you use library _x_ instead of _y_?](#why-did-you-use-library-x-instead-of-y)
  * [How can I use Mocha instead of Jest?](#how-can-i-use-mocha-instead-of-jest)
* [Get in touch](#get-in-touch)

## How to buy the book

There should be links here at some point in August 2022. Please check back then :)

## What's in this repository

This repository stores the source code for two JavaScript web applications which have been produced using a test-driven development (TDD) workflow. In addition to the application code, there are almost 500 Jest unit tests and also some Cucumber tests that utilise Puppeteer.

You'll find a list of directories, `Chapter01` through `Chapter18`, that follow the first eighteen chapters of the book.

`Chapter01` to `Chapter13` cover an application called _Appointments_, which is an appointment booking system for hair salons.

`Chapter14` to `Chapter18` cover an application called _Spec Logo_, which is an implementation of the Logo programming environment.

These directories contains the following subfolders:
   * `Start`, which contains the code that begins the chapter. All the code samples and walkthroughs are built on top of this directory. If you're following along with the book, you'll want to use this start point.
   * `Exercises`, which contains the code at the end of the chapter, without any of the chapter exercises completely. If you're not following along but you do want to try the exercises, you'll want to start here.
   * `Complete`, which contains solutions to the exercises.

(Not all chapters have exercises, and `Chapter11` has no walkthrough.)

## What's not in this repository

The book has a final chapter, Chapter 19, _Understanding TDD in the Wider Testing Landscape_, that has no code :)

## How to use this repository

### If you don't have the book...

If you're interested in seeing the complete solutions to these applications, together with their implementations and all of the tests, take a look in `Chapter13/Complete` (for _Appointments_) and `Chapter18/Complete` (for _Spec Logo_), or you can look at the head of the `appointments` and `spec-logo` branches.

### Following along with the book

If you're using the book, please fork the repository and clone it on your local machine. Then you can start pushing your own commits as you work along with the book.

### Running tests

You'll need to have Node installed and a code editor of your choice.

1. Make sure you've cloned the repo.
2. In a terminal, navigate to the directory of your choice, e.g. `Chapter18/Complete`.
3. Run `npm install`.
4. Run `npm test`.

You can also run an individual test file by appending the test file path, for example, `npm test test/CustomerForm.test.js`.

### Building and running the app

#### For Chapter 1 through 5:

In the first 5 chapters, there's no server, so after building the app you'll need to navigate to the `dist/index.html` file in your browser.

1. Run `npm run build`.
2. Run `open dist/index.html` to open the application in your browser. If this step doesn't work, open your web browser manually and then paste in the full file path into the location bar.

_Note_: if you see a blank screen, check your console for errors, and see the [Troubleshooting](#troubleshooting) section at the bottom of this document.

#### From Chapter 6 onwards:

1. Run `npm run build`.
2. Run `npm run serve`.
3. Navigate to `http://localhost:3000` in your browser.

If port 3000 is in use or you'd rather use another port, you can use `PORT=8080 npm run serve`.

As the chapters progress, the build script will build not just the source code you're working on, but also the Node server application and the Relay GraphQL compiler.

### Other commands you can run

You can use `npm run lint` to see any linting issues using ESLint, and `npm run format` to format the source code using Prettier.

If you're playing around with the server source, you can use `npm run build-server` and `npm run test-server`.

### Viewing the commit history

There are two branches, `appointments` and `spec-logo` that were used during the writing process and show the history of how the application was built. You are welcome to inspect and use those too. All of the chapter directories in the `main` branch were auto-generated from these branches.

## Troubleshooting

### I see a white screen when I load dist/index.html

You may need to enable local file access in your browser. Take a look in the developer console and it should give you instructions for what to do.

(In Safari on MacOS, you need to select _Develop > Disable Local File Restrictions_.)

### Some other problem?

Please create a new Issue in the repository and I'll do my best to assist you.

## Other topics

### Why did you use library _x_ instead of _y_?

Because I preferred _x_ over _y_. This applies to the following, but note this list is probably not exhaustive:

| Book's choice | Another choice | Why? |
| ------------- | -------------- | ---- |
| Hand-rolled test library | React Testing Library | (I believe) you'll learn more this way. |
| Jest | Mocha | (I actually prefer Mocha, but) Jest is what most React developers are familiar with. See the [How can I use Mocha instead of Jest?](#how-can-i-use-mocha-instead-of-jest) section below. |
| Cucumber/Puppeteer | Cypress | I dislike that Cypress has an API that is unique to its product, whereas Puppeteer is a bolt-on to all the standard unit testing techniques, and Cucumber is a transferable skill because it has integrations for many different languages and runtimes.|
| Relay | Apollo | (I believe) Relay is simpler. |
| Redux saga | Redux thunk | (I believe) Sagas are more complicated, so at this point in this book it's a more interesting choice. |

### How can I use Mocha instead of Jest?

For the most part, there's a 1-to-1 mapping between the Jest API and the Mocha API. I maintain a page at https://reacttdd.com/migrating-from-jest-to-mocha that you can use as a quick guide to using Mocha rather than Jest as you go through the book.

## Get in touch

You can contact the author directly by raising Issues here in GitHub, or via his website at [danielirvine.com](https://danielirvine.com).
