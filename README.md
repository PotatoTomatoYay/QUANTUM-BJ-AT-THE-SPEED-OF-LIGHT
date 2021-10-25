# QUANTUM-BLACKJACK
Made by Sidharth Srinivas, James Liu, Sameer Gupta, Gavin Wang, Raksheet Kota

After seeing the applications of quantum computing on a simple coin flip, we were inspired to use quantum computing to simulate another form of luck, in this case: drawing cards! More specifically, using Qiskit to create a game of blackjack. Two days later, Quantum BJ, a complex game that tests both skill and intelligence, was born.

# Playing Quantum BJ
To run the game, one just needs to download the python notebook file and run it through an online IDE that supports Qiskit(Jupiter Notebook, Strangeworks). This github repository can also be imported directly into Strangeworks to be run.

Quantam BJ is played synonomously to the well-known casino game BlackJack.

At the start of the game, the dealer gives 2 cards each to the player and themselves. One of the dealer's cards is unknown to the player.

With the intention of having a highest valued hand not exceeding 21, the user asks the dealer for a card. The process in which the dealer gives the user a card is referred to as 'hitting' the user. When the user thinks that receiving another card would bring their hand value above 21, they can ask to stop or _stand_. At this point, the dealer hits until her hand is valued 17 or higher. Assuming that neither the dealer nor the user has surpassed 21, each hand value is calculated and the winner is determined. If the user's hand is greater than the dealers,  the user wins. Otherwise, the user loses.

## The Objective of Quantum BJ
In Quantum BJ, the objective is to have the highest hand value not exceeding 21. 

# Game Mechanics

## Hand Value
The value of a player’s hand is equal to the sum of the numbers on each card in their hand. There are also special cards that have unique properties. The K, Q, and J cards represent faces, namely the front of an animal's head that features three of the head's sense organs, the eyes, nose, and mouth, and through which animals express many of their emotions. Because of the vigorous emotional attachment between humans and their faces, “face cards” are worth 10 points. In addition, the “A” card can either be worth either 1 or 11 points. The "A" card starts at the higher value of 11, but if the higher value would cause a player to have more than 21 points, it will decrease to 1 point.

## `HIT`
If the player wishes to receive another card, they type `hit`.  A single card is then given to the player. If the player’s hand value totals less than 21, the player has the option to `hit` again. If the player’s hand totals exactly 21, they must `stand`. If the player’s hand value exceeds 21, they `bust` and lose the game.

## `STAND`
If the player does not wish to receive another card, they type `stand`. The dealer will then receive their cards and the hand values will be compared.

## The Dealer
The dealer is the mysterious entity who serves as your opponent in Quantum BJ. If you lose to the dealer, she slurps your ***soul*** and you will never be able to have it back. There is no rematch or “best of three”. In Quantum BJ, there are real, tangible stakes, which serves to intensify your entertainment!
 
##### The dealer will always hit when her hand value is 16 or less, and she will stand otherwise. 


# Winning
A player wins if they have the highest hand value not exceeding 21 once both players `stand`. If a player's hand value exceeds 21 at any point, they automatically `bust` and lose the game. If both players have the same hand value, then the game will be tied. 


# How was Qiskit used?
We used Qiskit to model a quantum circuit that contained 6 qubits and 6 classical bits to represent a binary number that goes up to 63. This was the minimum amount of bits needed to model the deck of cards as there are 52 cards in a standard deck. By attaching an identity gate and a hadamard gate to each qubit and measuring the resulting value, we are able to randomly generate a binary string from 000000 to 111111 (0 to 63).  We run this experiment 500 times, and the value with the highest occurrence is chosen as our final value. This final value is essentially our version of drawing a card for blackjack. All of our qiskit tools happen in the background, none of which is seen by the client.

# What did we learn from this experience?
Oh boy, where do we start? Before this hackathon, our entire team had minimum practice with python, python notebooks, and most importantly, zero experience with quantum computing. 

We were all under the impression that programming a quantum computer would be no different than programming a normal computer with the exception that the programming language would be different. Through experimenting and reading the qiskit library, we discovered that quantum programming required the programmer to understand how to exploit entanglement and quantum properties to create efficient software. 

Throughout the experience, we learned that quantum computing may seem difficult at first, but with the right resources, anyone can learn it. As mentioned before, everyone on our team had minimal experience with quantum computing. Yet, by this time, we managed to create a whole game with it. One really specific thing we learned was in the counts object for qiskit. The most_frequent method in counts is unable to function when multiple items have the same frequency. Unfortunatly, we ran out of time before we were able to create our own findMax method.

