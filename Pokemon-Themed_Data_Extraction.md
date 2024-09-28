
# Pokémon-Themed Data Extraction  
**(Total Points: 300)**

## Objective  
Your mission is to help **Professor Oak** analyze the stats of seven **Pokémon-owned companies** in the Kanto region: **Voltas, Blue Star, Crompton, Orient Electric, Havells, Symphony, and Whirlpool**, to help the Pokémon understand their strengths and weaknesses better and improve their skills.

**Note:** This task must be completed using **web-scraping techniques**. You are allowed to use any available code-based web-scraping tools to complete the task. **Data cannot be manually extracted** or downloaded from the given site.

---

# Seed URL:  
Professor Oak has provided a single **Pokédex entry point (URL)** to access all the Pokémon stats from **Screener.in** for these companies. You will start by analyzing **Voltas**, but remember, you can only use one entry point to extract data for all companies. You can navigate to the other companies using the search bar located at the top of the page.

#### Pokémon Companies:

1. Voltas (CEO: Pikachu)
2. Blue Star (CEO: Squirtle)
3. Crompton (CEO: Charmander)
4. Orient Electric (CEO: Bulbasaur)
5. Havells (CEO: Eevee)
6. Symphony (CEO: Jigglypuff)
7. Whirlpool (CEO: Gyarados)

#### [Entry Point](https://www.screener.in/company/VOLTAS/consolidated/)

---

# Task 1: Extract Basic Pokémon Power Stats (45 Points)  
Help **Pikachu and friends** by gathering their basic **Power Stats**:  
- Market Cap  
- Stock P/E  
- ROCE  
- Current Price  
- ROCE  
- ROE  

This will give them insights into their current strengths.

![image](https://github.com/user-attachments/assets/46adb235-1fe9-4f5a-a3b9-27502a29015f)

---

# Task 2: Extract Pokémon Item Inventory (105 Points)  
Extract their **Item Inventory (balance sheet)** to understand how much:  
- Reserves  
- Borrowings  
- Total Liabilities  
- Fixed Assets  
- Investments  
- Total Assets  

Focus only on **March 2024** for this task.

![image](https://github.com/user-attachments/assets/71153c34-23a8-455f-bd77-b0cc14040f88)

---

# Task 3: Track Pokémon Battle Performance (150 Points)  
Finally, gather their **Battle Performance Stats** over the last three years (March 2022, March 2023, and March 2024):  
- Sales  
- Net Profit  
- OPM  
- EPS  

This will help the trainers see how well they’ve done in recent Pokémon battles!

![image](https://github.com/user-attachments/assets/03c6e4e7-60fd-45a1-bd8d-c9ef767cbc1f)

Each of these tasks needs to collect the specified data for **all 7 companies**, and aggregate them in the format given below. Each of the stats in every category needs to be extracted.

---

# Deliverables:  
You need to return your findings to Professor Oak in the form of three **Pokédex Data Files (CSV files)**:

1. **Basic_Pokemon_Stats.csv**
2. **Pokemon_Item_Inventory.csv**
3. **Battle_Performance_Stats.csv**

Each CSV file should correspond to one of the tasks mentioned above. Write **one separate function for each task** to generate the respective Pokédex Data File. Each task will be graded separately. Finally, execute **each function** to generate the Data Files.

#### Format for Data Files  
[Pokédex Data Files](https://docs.google.com/spreadsheets/d/1-UEN3tcM5PFc6ktqdIBZeAgpOq6RWtQi/edit?usp=sharing&ouid=112995622785589197872&rtpof=true&sd=true)

---

# Submission:  
As a Pokémon researcher, you must also upload your code to **GitHub (Pokémon HQ)**. This way, other Pokémon Trainers can also benefit from your findings! Follow the standard instructions from [README.md](/README.md). Also, make sure to upload the **Data Files** that you create to the GitHub repository.
