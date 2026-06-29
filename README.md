# Wordle

A from-scratch take on the word game. Six guesses to find a hidden five-letter word; every guess comes back color-coded — right letter right spot, right letter wrong spot, not in the word at all. I built it to get a feel for state management and UI feedback loops, which turn out to be most of what makes Wordle actually work.

**[Live demo →](https://wordle-game-theta-sand.vercel.app)**

This started as the final project for an Object-Oriented Java course (the desktop version with a Swing GUI), and there's a web version in here too.

## What it does

- Full game logic over a ~5,700-word dictionary
- Color-coded feedback on each guess
- Six-guess limit, with win/loss detection
- A small JUnit test suite

## The Java version

```
src/
  Main.java         entry point
  Wordle.java       game driver
  WordleModel.java  game state and guess evaluation
  WordleGUI.java    the Swing UI
Test/               JUnit tests
5_letter_words.txt  the word list
```

Compile and run from the repo root:

```bash
javac -cp stdlib.jar -d build src/*.java
java -cp build:stdlib.jar Main
```

(On Windows, swap the `:` in the classpath for `;`.) Or just open the project in IntelliJ and run `Main`.

One thing to know: the on-screen keyboard is display-only — type your guesses on your physical keyboard.

## The web version

`index.html` + `words.js` — open the live demo above, or serve the folder locally.

## Built with

Java · Swing · JUnit (desktop) · JavaScript (web)
