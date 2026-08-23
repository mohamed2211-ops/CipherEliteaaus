from google import genai
import os

client = genai.Client(api_key=os.environ["GEMINI_API_KEY"])

while True:
    text = input("أنت: ")

    if text.lower() in ("exit", "quit"):
        break

    response = client.models.generate_content(
        model="gemini-2.5-flash",
        contents=text
    )

    print("المساعد:", response.text)
