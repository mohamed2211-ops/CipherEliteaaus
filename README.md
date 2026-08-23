from google import genai
import os

client = genai.Client(api_key=os.environ.get("GEMINI_API_KEY"))

while True:
    user = input("أنت: ")

    if user.lower() in ["exit", "quit", "خروج"]:
        break

    response = client.models.generate_content(
        model="gemini-3.6-flash",
        contents=user
    )

    print("المساعد:", response.text)
