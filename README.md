# QUANTUM-BlackJack(BJ)
Made by Sidharth Srinivas, James Liu, Sameer Gupta, Gavin Wang, Raksheet Kota


# Playing Quantum BJ

After seeing the applications of quantum computing on a simple coin flip, we were inspired to use quantum computing to simulate another form of luck, in this case: drawing cards! More specifically, using it to create a game of blackjack. And thus, Quantum BJ, a complex game that tests both skill and intelligence, was born.

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

Prior to this experience, we assumed that programming through a quantum computer only requires changes on the hardware side rather than the software side of things. We learned that not only does the hardware need to support particle entanglement, but programming is approached differently as computer scientists need to brainstorm and implement algorithms that not only function with qubits, but exploit them to its fullest with appropriate algorithms taking advantage of superposition.  

