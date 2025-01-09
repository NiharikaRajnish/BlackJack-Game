
# Blackjack Game (C# & .NET)

A simple console-based Blackjack game built using C# and the .NET framework. This game simulates a game of Blackjack between a player and the dealer, where the goal is to get as close to 21 as possible without going over.

## Features

- Player vs Dealer
- A deck of cards is used, with automatic reshuffling when the deck runs low
- Players can hit, stand, or double down
- Hand values are automatically calculated based on standard Blackjack rules
- The game continues with multiple rounds

## Requirements

- **.NET 6 or higher** (or you can use any version of .NET that supports C# development)
- C# (latest version compatible with .NET)

## Installation

1. Ensure that you have .NET SDK installed. You can download it from the official .NET website:  
   https://dotnet.microsoft.com/download

2. Clone the repository or download the files.

    ```bash
    git clone https://github.com/yourusername/blackjack-csharp.git
    ```

3. Navigate into the project directory:

    ```bash
    cd blackjack-csharp
    ```

4. Build the project using the .NET CLI:

    ```bash
    dotnet build
    ```

5. Run the game:

    ```bash
    dotnet run
    ```

## Gameplay

1. The game starts by dealing two cards to both the player and the dealer.
2. The player can choose one of the following actions:
   - **Hit**: Draw a card from the deck and add it to the player's hand.
   - **Stand**: End the player's turn, and the dealer will play.
   - **Double Down**: Double the player's bet and receive only one additional card.
3. The dealer will play automatically, drawing cards until reaching 17 or higher.
4. The game checks for a winner: 
   - If the player’s hand value exceeds 21, they lose.
   - If the dealer’s hand value exceeds 21, the player wins.
   - If both the player and dealer have the same hand value, the round is a tie.
   - The player wins if their hand is closer to 21 than the dealer's.
   
## Code Structure

### `Card.cs`
Defines a **Card** class, representing a single playing card. Includes properties for suit and value.

### `Deck.cs`
Handles the **Deck** of cards. It shuffles the deck, deals cards, and tracks the remaining cards.

### `Hand.cs`
Represents a player's or dealer's **hand** in the game. Contains logic for adding cards and calculating the total value of the hand.

### `Player.cs`
Contains the **Player** class which handles player-specific actions like hit, stand, and double down.

### `Game.cs`
Contains the core **Game** logic: initializes the deck, controls the game flow, and manages rounds.

### `Program.cs`
Entry point for the application. Starts the game and handles the user interface via the console.

## Example of Gameplay

```text
Welcome to Blackjack!

Your hand: [8♠, 6♦] (Total: 14)
Dealer's hand: [10♣, ?]

Do you want to (H)it, (S)tand, or (D)ouble Down?
> H

Your hand: [8♠, 6♦, 3♣] (Total: 17)
Dealer's hand: [10♣, ?]

Do you want to (H)it or (S)tand?
> S

The dealer reveals their hand: [10♣, 7♦] (Total: 17)

The dealer stands.

The winner is: You win!
```

## Customization

- You can modify the `Card`, `Deck`, or `Hand` classes to introduce additional rules or change the structure of the deck (for example, allowing multiple decks).
- You can enhance the user interface to include more visual elements like displaying the cards graphically.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

