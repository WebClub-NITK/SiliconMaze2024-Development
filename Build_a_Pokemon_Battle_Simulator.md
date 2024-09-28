# **Build a Pokémon Battle Simulator**
**(Total Points: 200)**

## **Objective**
Develop a **Battle Simulator** where users select two Pokémon from a list of 15. The app calculates the winner based on stats like **Attack, Defense, Type advantages**, and other attributes. The goal is to create an interactive and informative experience for users to engage in battles and explore detailed Pokémon information.

---

# **Task 1: Display Pokémon Cards**

### **Subtask 1 (15 points)**
Create a web page to display **15 Pokémon**, each represented as an individual card.

Each **Pokémon Card** should include:
- **Name**: The Pokémon's name.
- **Image**: The front image of the Pokémon.
- **Cry Sound**: Play the Pokémon's cry sound when a user interacts with the card (e.g., by clicking a button).

### **Subtask 2 (30 points)**
When a user clicks on a Pokémon card, display a **modal or detailed view** with comprehensive information about the selected Pokémon.

This **Detailed View** must include:
- **Name**
- **Height**
- **Weight**
- **Base Stats** (HP, Attack, Defense, Speed)
- **Abilities** (including hidden abilities)
- **Moves**
- **Color**
- **Shape**
- **Location**
- **Egg Groups**

---

# **Task 2: Battle Simulation**

### **Subtask 1 (10 points)**  
Allow users to select **two Pokémon** by clicking on their respective cards. When a Pokémon is selected, visually highlight the card.

### **Subtask 2: Initiate a Battle (90 points)**  
Implement a **"Battle" button** that initiates the battle between the two selected Pokémon.

#### **Battle Logic**:
- **Move Selection**: Randomly select a move from the list of available moves.
- **Damage Calculation Formula** as described, including:
  - **Level (50)**
  - **Attack, Defense, Move Power**
  - **Type Effectiveness**
  - **Accuracy**
  - **Speed**

#### **Type Effectiveness**:  
Calculate type effectiveness using the **Pokémon API**.

---

### **Subtask 3: Battle Summary (10 points)**  
Display a **summary** after the battle, including:
- The **winner**.
- **Moves used** by each Pokémon.
- **Damage caused**.
- Add simple visual effects.

---

# **Task 3: Deployment with GitHub Pages (45 points)**

1. Create and push the project to a new **GitHub repository**.
2. Configure **GitHub Pages** for deployment.

---

# **Example Scenario for Damage Calculation**:

**Pokémon Stats**:

1. **Gengar**:  
   - Attack: 65  
   - Defense: 60  
   - HP: 60  
   - Speed: 110  
   - Type: Ghost/Poison  

2. **Alakazam**:  
   - Attack: 50  
   - Defense: 45  
   - HP: 55  
   - Speed: 120  
   - Type: Psychic  

**Assumptions**:

1. **Level**: 50 for both Pokémon.
2. **Move Power**: Gengar's Shadow Ball (80), Alakazam's Psychic (90).
3. **Type Effectiveness**:  
   - Gengar’s Shadow Ball is **super effective** against Alakazam (2.0x).  
   - Alakazam’s Psychic is **super effective** against Gengar (2.0x).
4. **Accuracy**:  
   - Gengar’s Shadow Ball accuracy: 85% (0.85).  
   - Alakazam’s Psychic accuracy: 90% (0.90).

**Damage Calculation**:

**Gengar’s Attack on Alakazam**:  
Damage = `((2 × 50 / 5 + 2) × (65 / 45) × 80 × 2.0 × 0.85 × 110 / 100) ≈ 5920.51`

**Alakazam’s Attack on Gengar**:  
Damage = `((2 × 50 / 5 + 2) × (50 / 60) × 90 × 2.0 × 0.90 × 120 / 100) ≈ 4359.23`

**Winner**:  
Since **Gengar**’s attack damage (5920.51) is greater than **Alakazam**’s attack damage (4359.23), **Gengar** wins the battle.

# **Resources, Tools, and References**

- **Pokémon API**: [Pokémon API Documentation](https://pokeapi.co/)
- **GitHub Pages Documentation**: [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages)

---

**Note**:  
You are free to use any technology stack, databases, or programming languages to complete this project. Choose tools and technologies that best fit your development needs and preferences.
