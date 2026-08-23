cat << 'EOF' > assistant.py
import os
from google import genai

client = genai.Client(api_key=os.environ.get("GEMINI_API_KEY"))

while True:
    text = input("أنت: ")
    if text.lower() in ("exit", "quit"):
        break

    response = client.models.generate_content(
        model="gemini-3.6-flash",
        contents=text
    )

    print("المساعد:", response.text)
EOF
