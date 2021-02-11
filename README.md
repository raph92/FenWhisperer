# FenWhisperer
A websocket server that listens for chess boardstates in the FEN format and creates square dominance and piece attack states as JSON

## Goal
The goal of this program is to assist with analyzing chess games

## Features
- Ability to recreate chess board states from FEN.
- Colors cell dominance
  - Shows whether white or black have more pieces attacking a square.
  - Quanitifies the square dominance
    - A negative number means that black is dominating and vice-versa
## Screenshots

<img src="https://i.imgur.com/ijeat6Y.png" width="400">

## How it works
This client starts a websocket that listens on port 5002 and listens for FEN strings.
The format of the message it is anticipating is `fen rnbqkbnr/pppppppp/8/8/8/8/PPPPPPPP/2BQKBNR w Kkq - 0 1`.
Once it receives that message it will then recreate that game state and calculate the dominance and attack states of squares and pieces, respectively.
