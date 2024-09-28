# Build an AI-powered PokéDex Assistant for Pokémon Trainers
**(Total Points: 500)**

In the world of Pokémon, the **PokéDex** is a legendary device that serves as an encyclopedia for all known Pokémon species. Whether you're a novice Trainer or a seasoned Pokémon Master, the PokéDex is your go-to resource for understanding the creatures that populate the Pokémon universe.

But now, we're in the **Generative AI** Era—a time where technology evolves beyond static databases and precise commands. Gone are the days when you had to input exact instructions for devices to work. Today, you can simply chat with your tools in natural language.

Your challenge? To **build the next-generation AI-powered PokéDex Assistant** —an intelligent, conversational AI chatbot that helps Pokémon Trainers (Users) in real-time, whether they’re seeking detailed Pokémon stats, analyzing battle strategies, or contributing their own knowledge and expertise to expand the ever-growing world of Pokémon research.

Using **Google's Gemini models (free tier)**, along with other advanced AI tools, your task is to equip the PokéDex Assistant with the ability to:

- Engage in natural conversations with Pokémon Trainers.
- Recognize Pokémon from images and offer insightful information about them.
- Let trainers upload their own battle notes and PDFs or even share their favorite website links to contribute their expertise.
- Query these new inputs and provide personalized responses that reflect the Trainer's unique strategies and knowledge.

By the end, you'll have built an AI-powered PokéDex that Trainers can rely on during their journey to becoming Pokémon Masters.

<hr>

### Task 1: Use Google's Gemini models (free tier) to create the PokéDex Assistant (60 Points)

1. Set up access to Google’s Gemini API (20 points)
   - Create a project and setup API Key in Google Cloud Console [hint](https://support.google.com/googleapi/answer/6158862?hl=en)
   - Enable the **Generative Language API** for you project [hint](https://support.google.com/googleapi/answer/6158841?hl=en)

2. Integrate the API in your development environment (40 points)
   - Set up the **Google's Gemini Model** in your environment
   - Test the API connection by sending and receiving a simple response


<hr>

### Task 2: Engineer a system prompt to shape the Assistant’s behavior as a PokéDex (80 points)
- Write a prompt to ensure the chatbot behaves as an intelligent, factual PokéDex resource.
- Ensure that the prompt focuses on delivering clear, concise explanations about Pokémon stats, types, evolutions, and other in-universe data.
- **Incorporate strict guidelines for the Assistant to ignore irrelevant or off-topic questions.** For instance, the Assistant should refuse to answer non-Pokémon-related queries politely, such as “What’s the weather?” or “Tell me a joke,” while remaining professional and helpful.


<hr>

### Task 3: Add the ability to provide an image as input for the PokéDex Assistant (60 Points)
- Ensure the PokéDex Assistant can analyze Pokémon images, like recognizing a Pikachu from a Trainer’s photograph [hint](https://ai.google.dev/gemini-api/docs/vision)

<hr>

### Task 4: Allow Trainers to add their own expertise to the PokéDex via PDF uploads (100 Points)

1. Use Langchain for uploading and splitting Trainer research papers or battle strategies (20 points)
   Ensure PDFs can be split into manageable sections for detailed analysis.

2. Use Google’s embeddings API to generate embeddings from Trainer expertise (30 points)
   Make sure the PokéDex Assistant accurately represents the knowledge from uploaded documents [hint](https://python.langchain.com/v0.2/docs/integrations/text_embedding/google_generative_ai/)

3. Store the embeddings in a vector database (ChromaDB, FAISS, etc.) for future queries (20 points)
   Allow the PokéDex Assistant to reference and access this expertise when Trainers ask related questions [hint](https://python.langchain.com/v0.2/docs/integrations/vectorstores/faiss/)

4. Extract the embeddings and use them to respond to queries like “What’s the best battle strategy for Charizard?” (30 points)

<hr>

### Task 5: Allow Trainers to add their expertise through a website link (100 Points)

1. Use Langchain to retrieve and process Pokémon battle guides or strategy articles from the link provided by the Trainer (20 points) [hint](https://python.langchain.com/v0.2/docs/integrations/document_loaders/url/))

2. Use Google’s embeddings API to generate embeddings from the fetched content (30 points)
   Ensure the PokéDex Assistant can analyze and store this knowledge for later use [hint](https://python.langchain.com/v0.2/docs/integrations/text_embedding/google_generative_ai/)

3. Store the embeddings in a vector database (20 points)
   Ensure the PokéDex Assistant can efficiently access and provide answers based on this new expertise [hint](https://python.langchain.com/v0.2/docs/integrations/vectorstores/faiss/)

4. Extract and use the stored embeddings to respond to queries like, “How do I train a Bulbasaur for competitive battles?” (30 points)

<hr>

### Task 6: Build a user-friendly front-end using Streamlit or any other preferred library/framework (80 points)

1. Design a user-friendly interface for Trainers to interact with the PokéDex Assistant (50 points)
   Ensure the interface supports text, image, PDF, and website link inputs from Trainers

2. Test the interface for usability, ensuring it’s intuitive for Trainers of all levels (30 points)

[**Hint**](https://streamlit.io/generative-ai)

<hr>

### Task 7: Deployment (20 Points)
Deploy the PokéDex Assistant to a cloud platform (e.g. Streamlit Community Cloud, render) so Trainers can access it globally.

