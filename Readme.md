# Talent Scout - AI-Powered Hiring Assistant
## Project Overview
Talent Scout is a conversational AI-based hiring assistant designed to streamline the recruitment process. Built using Streamlit and Google’s Generative AI, the chatbot guides users through a step-by-step interview process, collecting information about their skills, experience, and preferences. It dynamically generates additional questions and evaluates candidates based on their responses, providing insights for recruiters.

Installation Instructions
Clone the Repository:

```bash
git clone https://github.com/your-repo/talent-scout.git
cd talent-scout
```
Set Up a Virtual Environment:

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```
Install Required Dependencies:

```bash
pip install -r requirements.txt
```
Add API Keys:

- Create a .env file in the project root directory.
- Add your Google API Key:
- GOOGLE_API_KEY=your_google_api_key_here
* Run the Application:

```bash
streamlit run test.py
```
Access the App:

- Open your browser and navigate to http://localhost:8501.


## Usage Guide
Launching the App:
After running the app, you'll be greeted with a welcome message and guided through a series of questions.

# Step-by-Step Information Gathering:

Enter details like your 
- full name
- email
- years of experience
- technical skills.
Respond to dynamically generated questions crafted by the AI model.

Candidate Evaluation:

Once all questions are answered, the assistant evaluates your responses using predefined criteria.
Recruiters can access the insights to make informed decisions.
Technical Details
Libraries Used:

Streamlit: Frontend framework for interactive web apps.
google.generativeai: API for generating questions and evaluations.
dotenv: Manages environment variables securely.
Model Details:

Utilizes Google's Generative AI (Gemini-pro) for generating content and evaluating candidates.
Architectural Decisions:

Modular design with an Agents class to encapsulate API interactions.
Session management using st.session_state for seamless user experience.
Prompt Design
Information Gathering:
Prompts are designed to elicit precise and structured responses. For example:

Prompt for name: "What is your full name?"
Prompt for skills: "What is your tech stack (e.g., Python, Django, SQL)?"
Dynamic Question Generation:
Prompts for additional questions are crafted to analyze candidate data and generate meaningful follow-ups, e.g., "Based on the user's tech stack, generate technical questions."

Evaluation:
Prompts for scoring candidates include:

"Evaluate this candidate based on experience, skills, and desired position. Provide a concise assessment."
Challenges & Solutions
Session State Management:

Challenge: Ensuring the chatbot flow remained consistent during user interactions.
Solution: Used st.session_state to persist chat history, user data, and flow stages.
Dynamic Question Parsing:

Challenge: Handling JSON parsing issues with AI-generated questions.
Solution: Implemented error handling to validate and parse JSON safely.
Prompt Engineering:

Challenge: Crafting effective prompts for diverse user inputs.
Solution: Iterated on prompts to balance specificity and adaptability for varied responses.
