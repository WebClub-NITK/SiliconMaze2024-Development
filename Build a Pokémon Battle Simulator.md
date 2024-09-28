# Objective
Develop a simple battle simulator where users can select two Pokémon from a list of 15, and the app calculates the winner based on various stats like attack, defense, type advantages, and other attributes. The goal is to create an interactive and informative experience where users can engage in battles while exploring detailed information about each Pokémon.

# Task 1: Display Pokémon Cards
### Subtask 1 (20 points)
Create a web page with a Pokémon card and display 15 Pokémon on the web page, each represented as an individual card.

Each card should include  Pokémon's:

- Name: Display the name of the Pokémon.
- Image: Display the front image of the Pokémon.
- Cry Sound: The cry sound should play when a user interacts with the card (e.g., clicks a button). Use the latest version of the cry available. 
<br><br>

### Subtask 2 (20 points)
When a user clicks on a Pokémon card, a modal or detailed view should appear, providing comprehensive information about the selected Pokémon.

This detailed view must include the following: 

- Name: The Pokémon's name.
- Height: The height of the Pokémon (in decimetres or meters).
- Weight: The weight of the Pokémon (in hectograms or kilograms).
- Base Stats: Key stats include HP, Attack, Defense,Speed.
- Abilities: The Pokémon's abilities, including any hidden abilities.
- Moves: A list of moves the Pokémon can learn
- Color: The Pokémon's color.
- Shape: The physical shape classification of the Pokémon.
- Location: Possible locations where the Pokémon can be found.
- Egg Groups: The breeding groups to which the Pokémon belongs.
<br><br>
 
# Task 2: Battle Simulation
### Subtask 1 (2.5 points)
Allow users to select two Pokémon by clicking on their respective cards. When a Pokémon card is selected, highlight the card visually (e.g., with a border or background color change) to indicate it's been chosen for the battle.
<br><br>

### Subtask 2: Initiate a Battle (35 points)
Implement a "Battle" button that, when clicked, initiates the battle between the two selected Pokémon.

**Battle Logic:**
- Move Selection: Randomly select a move from the list of moves available to each Pokémon.
- Damage Calculation Formula: 

![image](https://s3.amazonaws.com/hr-assets/0/1727503131-68a5aa8839-unnamed.jpg)

- Where:
  * Level: Assume a constant level for both Pokémon (e.g., Level 50) to simplify the calculations.
  * Attack: The attacking Pokémon's Attack stat.
  * Defense: The defending Pokémon's Defense stat.
  * Move Power: The power of the move being used by the attacking Pokémon.
  * Type Effectiveness: A multiplier based on type matchups:
    * 2.0: Super effective against the opponent’s type (e.g., Fire-type move against Grass-type Pokémon).
    * 1.0: Neutral against the opponent’s type (e.g., Normal-type move against Grass-type Pokémon).
    * 0.5: Not very effective against the opponent’s type (e.g., Fire-type move against Water-type Pokémon).
  * Accuracy: The accuracy of the move being used as a decimal (e.g., 1.0 for 100% accuracy).
  * Speed: The speed stat of the attacking Pokémon
<br><br>

### Subtask 3: Battle Summary (2.5 points)
Display the winner (e.g., "Charizard wins!"), moves used and damage caused by each Pokémon.
<br><br>


# Task 3: Deployment with GitHub Pages (20 points)

1. Create and push your project to a new GitHub repository.
1. Configure GitHub Pages in the repository settings to deploy the project.
<br><br>


# Example Scenario for calculating damage:

### Pokémon Stats:

1. Gengar: Attack 65, Defense 60, HP 60, Speed 110, Type: Ghost/Poison
2. Alakazam: Attack 50, Defense 45, HP 55, Speed 120, Type: Psychic
<br>

### Assumptions:

1. Level: 50 for both Pokémon
2. Move Power: Gengar's Shadow Ball (80), Alakazam's Psychic (90)
3. Type Effectiveness: Gengar's Shadow Ball is super effective against Alakazam (2.0), and Alakazam's Psychic is also super effective against Gengar (2.0)
4. Accuracy: Gengar's Shadow Ball accuracy is 0.85 (85%), Alakazam's Psychic accuracy is 0.90 (90%)
<br><br>

**Gengar’s Attack on Alakazam:** Damage = ((2 × 50 / 5 + 2) ×( 65 / 45) × 80 × 2.0 × 0.85 × 110 / 100) ≈ 5920.51

**Alakazam’s Attack on Gengar:** Damage = ((2 × 50 / 5 + 2) × 50 / 60 × 90 × 2.0 × 0.95 × 120 / 100) ≈ 4359.23

**Winner:** Gengar’s attack damage (5920.51) is greater than Alakazam’s attack damage (4359.23). Therefore, Gengar is the winner based on the damage caused.
<br><br>

# Resources, Tools, and References
- Pokémon API - General Data: [Pokémon API Documentation](https://pokeapi.co/)
- [GitHub Pages Documentation](https://docs.github.com/en/pages/getting-started-with-github-pages)
<br><br>

**Note:**
You are free to use any technology stack, databases, or programming languages of your choice to complete this project. Choose tools and technologies that best fit your development needs and preferences.
