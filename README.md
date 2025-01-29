# ShopAssistAI 2.0
Conversational Laptop Recommendation System using OpenAI function calling feature
<table><tbody><tr><th><p>Project Report</p><h3>ShopAssistAI 2.0: Conversational Laptop Recommendation System using Open AI function calling feature.</h3><h3>Date: 2024/11/01</h3><p>Name: Dipak Sah</p></th></tr></tbody></table>

**1\. Introduction**

ShopAssistAI 2.0 is a  conversational application designed to assist users in finding the perfect laptop based on their needs. It leverages the power of Generative Artificial Intelligence (AI) to guide users through a conversation, gather their preferences, and recommend suitable laptops from a database.

**2\. System Requirements**

- **Back-End:** Python
- **AI Engine:** OpenAI's API for conversation generation and moderation, Function calling feature used
- **Database:** Excel CSV file to store laptop data (specifications, models, etc.)

**3\. System functionalities**

- **Conversational AI:** The core of ShopAssistAI is the conversational AI powered by OpenAI's chat model. It guides the user through the process by asking relevant questions and understanding their needs.
- **User Input Moderation:** User input is moderated using OpenAI's moderation API to ensure a safe and secure conversation.
- **User Profile Extraction:** The AI assistant extracts key information from the conversation to build a user profile that reflects their laptop preferences (budget, screen size, processing power, etc.). OpenAI's function calling mechanism is designed to convert a user_requirement string object into a JSON object.

**3.1. Extracting User Requirements**

- ShopAssistAI utilizes OpenAI's chat-completion endpoint to generate responses and potentially extract user requirements within the conversation flow. This is achieved by sending prompts and conversation history to the API, and the response might contain user-expressed preferences.
- While OpenAI's API doesn't natively convert text to JSON, the OpenAI’s function calling mechanism and technique is used to convert the user string extract to relevant user requirements as key-value pairs.

**3.2. Building the User Profile**

- The extracted key-value pairs can then be used to construct a user profile dictionary in JSON format. This dictionary would represent the user's preferences for various laptop attributes.

**4\. System Architecture**

 The application interacts with OpenAI's API for conversation generation and moderation. Additionally, it retrieves and compares laptop data from an external database.

**5\. Implementation Details**

- **Conversation Management:** Handles conversation initiation, response generation through OpenAI's chat model, and conversation history maintenance.
- **User Input Processing:** Captures user input, performs moderation checks, and extracts user profiles from conversation history (using Open AI Function calling it converts the user input string to JSON object).
- **Recommendation Logic:** Compares user profiles with laptop data, validates recommendations, and generates recommendation text.

**6\. Conclusion**

ShopAssistAI provides a user-friendly and interactive way for users to find the perfect laptop. By leveraging AI-powered conversation and personalized recommendations, ShopAssistAI simplifies the laptop selection process. Future development could involve:

- Integrating a wider variety of AI models for more sophisticated conversation capabilities and potentially leveraging OpenAI's fine-tuning abilities to tailor the model to the laptop recommendation domain.
- Expanding the recommendation engine to include other electronic products.
- Implementing a user feedback mechanism to continuously improve the recommendation accuracy and potentially using reinforcement learning techniques for this purpose.



