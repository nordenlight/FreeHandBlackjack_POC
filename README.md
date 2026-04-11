# Shadow Duel Blackjack POC

A frontend proof of concept for a modern crypto-casino-inspired blackjack game with a custom bonus-hand mechanic.

This project is a **UI/UX and gameplay prototype** built in React. It does **not** include real gambling functionality, wallet integration, deposits, withdrawals, or real-money transactions.

## Overview

Shadow Duel Blackjack is a blackjack concept with a custom pre-round guessing mechanic:

- The player starts with **two potential hands**
- Only part of the first hand is revealed at the beginning
- The player must guess the final value of the main hand from **6 possible options**
- If the guess is correct, a **bonus hand** is unlocked and played automatically with **50% of the original bet**
- If the guess is incorrect, only the main hand is played
- The rest of the round follows normal blackjack flow

## Features

- React-based single-page prototype
- Animated card dealing and card flipping
- Main hand + locked bonus hand system
- Guess modal with 6 possible values
- Dealer hand logic
- Hit / Stand / Double actions
- Hand value calculation with Ace support
- Fake in-game currency / mock balance
- Responsive dark casino UI

## Game Rules in this POC

### Main flow
1. Place a bet
2. Cards are dealt:
   - Main Hand: 2 cards
   - Bonus Hand: 2 cards (initially locked)
   - Dealer: 2 cards
3. The player sees:
   - first card of the Main Hand face up
   - second card of the Main Hand face down
   - both Bonus Hand cards face down
4. The player guesses the final value of the Main Hand
5. If correct:
   - the Bonus Hand is unlocked
   - it joins the round with 50% of the original bet
6. If incorrect:
   - only the Main Hand continues
7. The rest of the round plays like blackjack

### Blackjack rules used
- Number cards count as face value
- J, Q, K = 10
- Ace = 1 or 11
- Dealer draws to 16 and stands on 17
- Bust over 21
- Double is available on a 2-card hand
- Bonus hand is not a split hand

## Tech Stack

- React
- JavaScript
- Tailwind CSS
- lucide-react icons

## Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/nordenlight/FreeHandBlackjack_POC.git
cd FreeHandBlackjack_POC
