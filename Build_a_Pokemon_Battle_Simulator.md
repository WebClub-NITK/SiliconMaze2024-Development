# **Objective**
Develop a simple **Battle Simulator** where users can select two Pokémon from a list of 15. The app will calculate the winner based on various stats like **Attack, Defense, Type advantages**, and other attributes. The goal is to create an **interactive and informative experience** where users can engage in battles while exploring detailed information about each Pokémon.

---

# **Task 1: Display Pokémon Cards**

### **Subtask 1 (15 points)**
Create a web page to display **15 Pokémon**, each represented as an individual card.

Each **Pokémon Card** should include:
- **Name**: The name of the Pokémon.
- **Image**: The front image of the Pokémon.
- **Cry Sound**: Play the Pokémon's cry sound when a user interacts with the card (e.g., by clicking a button). Use the latest version of the cry available.

### **Subtask 2 (30 points)**
When a user clicks on a Pokémon card, display a **modal or detailed view** with comprehensive information about the selected Pokémon.

This **Detailed View** must include:
- **Name**: The Pokémon's name.
- **Height**: The height of the Pokémon (in decimeters or meters).
- **Weight**: The weight of the Pokémon (in hectograms or kilograms).
- **Base Stats**: Key stats such as HP, Attack, Defense, Speed.
- **Abilities**: Include any hidden abilities.
- **Moves**: A list of moves the Pokémon can learn.
- **Color**: The Pokémon's primary color.
- **Shape**: The physical shape classification of the Pokémon.
- **Location**: Possible locations where the Pokémon can be found.
- **Egg Groups**: The breeding groups to which the Pokémon belongs.
---

# **Task 2: Battle Simulation**

### **Subtask 1 (10 points)**  
Allow users to select **two Pokémon** by clicking on their respective cards. When a Pokémon card is selected, visually highlight the card (e.g., change its border or background color) to indicate it has been chosen for battle.

### **Subtask 2: Initiate a Battle (90 points)**  
Implement a **"Battle" button** that initiates the battle between the two selected Pokémon.

#### **Battle Logic**:
- **Move Selection**: Randomly select a move from the list of available moves for each Pokémon.
- **Damage Calculation Formula**:

    ![Damage Calculation Formula](https://s3.amazonaws.com/hr-assets/0/1727503131-68a5aa8839-unnamed.jpg)

    **Where**:
  - **Level**: Assume a constant level of **50** for both Pokémon.
  - **Attack**: The attacking Pokémon's Attack stat.
  - **Defense**: The defending Pokémon's Defense stat.
  - **Move Power**: The power of the move being used by the attacking Pokémon.
  - **Type Effectiveness**: A multiplier based on the move's type and the defending Pokémon’s type (explained below).
  - **Accuracy**: The accuracy of the move being used (e.g., 1.0 for 100% accuracy).
  - **Speed**: The speed stat of the attacking Pokémon.

#### **Type Effectiveness**:
The **type effectiveness** of a move is determined by the interaction between the **attacking Pokémon's move type** and the **defending Pokémon's type**. This multiplier significantly impacts the **damage calculation** and can fall into three categories:
- **Super Effective (2.0x multiplier)**:  
  If the attacking Pokémon's move type is **strong against** the defending Pokémon’s type (e.g., a Fire-type move against a Grass-type Pokémon), apply a **2.0x multiplier** to double the damage.
- **Neutral (1.0x multiplier)**:  
  If the attacking Pokémon's move type has **no specific advantage or disadvantage** against the defending Pokémon's type (e.g., a Normal-type move against a Grass-type Pokémon), apply a **1.0x multiplier**, leaving the damage unchanged.
- **Not Very Effective (0.5x multiplier)**:  
  If the attacking Pokémon's move type is **weak against** the defending Pokémon's type (e.g., a Fire-type move against a Water-type Pokémon), apply a **0.5x multiplier** to halve the damage.
You can retrieve **type effectiveness data** for each move's type using the **Pokémon API**. For example, if the attacking Pokémon uses an **Electric-type move**, you can fetch the Electric type’s **damage relations** to determine:
- **Super Effective (2.0x)**: If the defending Pokémon’s type appears under **`double_damage_to`**, apply a **2.0x multiplier**.
- **Not Very Effective (0.5x)**: If the defending Pokémon’s type appears under **`half_damage_to`**, apply a **0.5x multiplier**.
- **Neutral (1.0x)**: If the defending Pokémon’s type is **not listed** under either category, apply a **1.0x multiplier**.


### **Subtask 3: Battle Summary (10 points)**  
After the battle, display a **summary**:
- The **winner** (e.g., "Charizard wins!")
- **Move used** by each Pokémon.
- **Damage caused** by each Pokémon.
- **Tip**: Add simple visual effects (e.g., flashing borders or animations) when declaring the winner to make the experience more engaging.

---

# **Task 3: Deployment with GitHub Pages (45 points)**
1. Create and push your project to a new **GitHub repository**.
2. Configure **GitHub Pages** in the repository settings to deploy the project.
---

# **Example Scenario for Damage Calculation**:

### **Pokémon Stats**:

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

### **Assumptions**:

1. **Level**: 50 for both Pokémon.
2. **Move Power**: Gengar's Shadow Ball (80), Alakazam's Psychic (90).
3. **Type Effectiveness**:  
   - Gengar’s Shadow Ball is **super effective** against Alakazam (2.0x).  
   - Alakazam’s Psychic is **super effective** against Gengar (2.0x).
4. **Accuracy**:  
   - Gengar’s Shadow Ball accuracy: 85% (0.85).  
   - Alakazam’s Psychic accuracy: 90% (0.90).

### **Damage Calculation**:

**Gengar’s Attack on Alakazam**:  
Damage = `((2 × 50 / 5 + 2) × (65 / 45) × 80 × 2.0 × 0.85 × 110 / 100) ≈ 5920.51`

**Alakazam’s Attack on Gengar**:  
Damage = `((2 × 50 / 5 + 2) × (50 / 60) × 90 × 2.0 × 0.90 × 120 / 100) ≈ 4359.23`


### **Winner**:  
Since **Gengar**’s attack damage (5920.51) is greater than **Alakazam**’s attack damage (4359.23), **Gengar** wins the battle.

# **Resources, Tools, and References**

- **Pokémon API**: [Pokémon API Documentation](https://pokeapi.co/)
- **GitHub Pages Documentation**: [GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages)

---

**Note**:  
You are free to use any technology stack, databases, or programming languages to complete this project. Choose tools and technologies that best fit your development needs and preferences.
