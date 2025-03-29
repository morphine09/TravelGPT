Travel Itinerary Planner Chatbot - Documentation
1. Overview
AI chatbot that generates personalized travel itineraries based on:

Destination

Budget

Duration

Dietary needs

Mobility level

Interests

Integrations: Google Gemini AI + WeatherAPI

2. Quick Setup
A. Install Dependencies
bash
Copy
pip install gradio google-generativeai requests
B. Run the App
python
Copy
python app.py
→ Access at: http://localhost:7860

3. Key Files
app.py (Main Gradio app)

requirements.txt (Must include):

Copy
gradio>=4.0
google-generativeai>=0.3.0
requests
4. API Keys Required
Service	Key Variable	Get It From
Google Gemini	GEMINI_API_KEY	Google AI Studio
WeatherAPI	WEATHER_API_KEY	WeatherAPI.com
Store keys securely:

For local use: .env file

For Hugging Face: Repository Secrets

5. Hosting (Free Options)
A. Hugging Face Spaces
Create new Space → Gradio SDK

Upload:

app.py

requirements.txt

Add API keys in Settings → Secrets

B. Local Sharing
python
Copy
demo.launch(server_name="0.0.0.0")  # Share LAN IP
6. How Recruiters Can Test
Sample Inputs:

"3-day Tokyo trip with $2000 for food lovers"

"Weekend getaway to Rome, luxury stay"

Output Includes:
✔ Daily schedule
✔ Meal recommendations
✔ Weather-based packing tips
✔ Cost breakdown

7. Troubleshooting
Blank screen? → Check browser console (F12)

API errors? → Verify keys + internet connection

Can’t type? → Ensure interactive=True in gr.Textbox()
