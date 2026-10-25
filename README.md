# ai-content--creator
An AI-powered short-video content series featuring study tips, thumbnails, and video editing for college students. 
import csv

# AI Influencer-Style Content Series Project

series_name = "AI-Powered Study Hacks for College Students"

videos = [
    {
        "title": "3 AI Tools Every Student Should Know",
        "script": "ChatGPT helps explain topics, Gemini helps explore ideas, and Canva helps create study visuals.",
        "caption": "Explore AI tools to make studying easier!"
    },
    {
        "title": "How to Make Study Notes Using AI",
        "script": "Use AI to organise notes into simple points, then verify the information with your class materials.",
        "caption": "Create clear study notes with AI assistance!"
    },
    {
        "title": "Study Smarter with Pomodoro",
        "script": "Choose one task, focus for 25 minutes, and take a short break.",
        "caption": "Try this simple time-management technique!"
    },
    {
        "title": "How to Prepare for Exams Using AI",
        "script": "Create a revision timetable, practise questions, and check answers using reliable sources.",
        "caption": "Prepare smarter for your next exam!"
    },
    {
        "title": "5 AI Tools to Explore for College Work",
        "script": "Explore ChatGPT, Gemini, Canva, CapCut, and Google Docs for different study and content tasks.",
        "caption": "Discover useful digital tools for college students!"
    }
]

# Display the content series
print("AI INFLUENCER-STYLE CONTENT SERIES")
print("Series Name:", series_name)
print("-" * 50)

for i, video in enumerate(videos, start=1):
    print("\nVideo", i)
    print("Title:", video["title"])
    print("Script:", video["script"])
    print("Caption:", video["caption"])

# Save the videos to a CSV file
with open("content_series.csv", "w", newline="", encoding="utf-8") as file:
    writer = csv.DictWriter(
        file,
        fieldnames=["title", "script", "caption"]
    )
    writer.writeheader()
    writer.writerows(videos)

print("\nContent series saved successfully!")
print("File name: content_series.csv")
