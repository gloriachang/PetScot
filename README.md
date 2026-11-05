# PetScot

PetScot is a gamified productivity app built in Unity and C# that helps students turn personal goals into structured quests and daily tasks. The app integrates the Claude API to generate personalized academic, professional, social, and self-improvement goals based on user profile data.

## Demo

https://github.com/user-attachments/assets/97bfe4ba-20ac-4fb0-ab86-58d5800cd556

## Features

- Personalized AI-generated quests using the Claude API
- Academic, professional, social, and self-improvement goal generation
- Task completion, points, and leveling system
- Persistent user profile data
- Multi-page Unity UI and navigation
- API error handling with fallback quests

## Tech Stack

- **C#**
- **Unity**
- **Claude API**
- **UnityWebRequest**
- **TextMesh Pro**
- **Unity UI**

## Architecture

```text
User Onboarding
      |
      v
Player Profile Data
      |
      v
QuestGenerator
      |
      +----> Claude API
      |         |
      |         v
      |    Generated Quests
      |
      v
Unity UI
      |
      v
Task / Quest Completion
      |
      v
TaskManager
      |
      v
Points + Level Progression
```

## Core Components

- `QuestGenerator.cs` — generates personalized quests through the Claude API and handles response parsing/fallbacks
- `TaskManager.cs` — manages task completion, points, and player levels
- `NavigationManager.cs` — handles page navigation and UI state
- `PlayerData.cs` — stores player profile information used throughout the app

## Running the Project

1. Clone the repository:

```bash
git clone https://github.com/gloriachang/petscot.git
```

2. Open the project in Unity.
3. Configure your Claude API key securely.
4. Run the project from the Unity Editor.

## Future Improvements

- Secure backend proxy for API requests
- Persistent cloud storage
- Expanded personalization
- More progression and social features
