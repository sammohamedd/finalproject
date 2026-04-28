````md
# LocalLoop

LocalLoop is a local information web app that helps users quickly find community-based information by entering an Iowa ZIP code. The app connects location data, weather, local services, school district information, Medicaid-related data, community college data, and local resource information into one simple dashboard. Users can also ask an AI assistant questions about their local area based on the information currently loaded into the app.

## Project Overview

LocalLoop was created to make local public information easier to access and understand. Many useful resources exist across different government websites, APIs, and local service pages, but they can be difficult to find quickly. This app brings that information together in a cleaner, more student-friendly interface.

After entering a ZIP code, users can view location-based details such as:

- City, county, and state
- Current weather
- Trash and recycling information
- School district information
- Medicaid data by county
- Iowa community college data
- Food, housing, and health resources
- AI-generated answers based on the loaded local data

## Features

### ZIP Code Search

Users can enter an Iowa ZIP code, and the app automatically pulls location information such as city, state, latitude, and longitude.

### County Detection

The app uses latitude and longitude coordinates to identify the user’s county.

### Weather Information

The app connects to the National Weather Service API to display current forecast information for the entered location.

### Local Services

The app displays trash and recycling information when available. Some cities currently use sample or placeholder service data.

### School District Information

The app connects to Iowa public data to retrieve school district information based on the user’s city.

### Medicaid Data

The app connects to Iowa public data to retrieve Medicaid-related information by county.

### Community College Data

The app retrieves Iowa community college information from a public Iowa dataset.

### Local Resource Directory

The app provides county-based resources for food, housing, and health services. Currently, some counties include manually added resources, while others display placeholder messages until more data is connected.

### AI Assistant

LocalLoop includes an AI chat feature powered by an OpenAI backend. The assistant answers questions using only the local data currently loaded into the app.

Example questions include:

- What is the weather today?
- When is trash day?
- Is recycling this week?
- What local resources are near me?
- Show Medicaid data for my county.
- What community colleges are in Iowa?

## Tech Stack

### Frontend

- React
- JavaScript
- CSS
- Vite

### Backend

- Node.js
- Express
- OpenAI API
- dotenv
- cors

### APIs Used

- Zippopotam.us ZIP Code API
- FCC Census Area API
- National Weather Service API
- Iowa Data API

## Project Structure

```txt
localloop/
  frontend/
    src/
      App.jsx
      App.css
      main.jsx
    package.json

  backend/
    server.js
    package.json
    .env
````

## Getting Started

### 1. Clone or download the project

```bash
git clone <your-repo-link>
cd localloop
```

### 2. Install frontend dependencies

```bash
cd frontend
npm install
```

### 3. Install backend dependencies

Open a second terminal:

```bash
cd backend
npm install
```

### 4. Create a `.env` file in the backend folder

Inside the `backend` folder, create a file called `.env`.

Add your OpenAI API key:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

Do not add quotation marks around the key.

### 5. Start the backend server

From inside the `backend` folder:

```bash
npm run dev
```

The backend should run at:

```txt
http://localhost:5001
```

### 6. Start the frontend

In a separate terminal, from inside the `frontend` folder:

```bash
npm run dev
```

The frontend should run at:

```txt
http://localhost:5173
```

## How to Use the App

1. Enter an Iowa ZIP code.
2. Click **Find My Local Info**.
3. View the dashboard with local weather, trash, recycling, and school district information.
4. Use the quick question buttons or type your own question into the LocalLoop chat.
5. The AI assistant will answer based on the available local data.

## Example ZIP Codes

```txt
52240 - Iowa City
50309 - Des Moines
```

## Current Limitations

Some parts of the app are still in progress:

* Trash and recycling data is not fully connected for every Iowa city.
* School closure calendar data is not connected yet.
* Some county resources are manually added instead of fully API-driven.
* The AI assistant can only answer based on the information currently loaded into the app.
* Some Iowa API field names may need further cleanup depending on the dataset structure.

## Future Improvements

Planned or possible future updates include:

* Connect real trash pickup APIs for more Iowa cities.
* Add school closure and calendar data.
* Expand food, housing, and health resources for all Iowa counties.
* Improve Medicaid data formatting.
* Add maps for nearby resources.
* Allow users to filter services by category.
* Add clearer error messages when an external API fails.
* Improve mobile responsiveness and dashboard design.

## Environment Variables

The backend requires the following environment variable:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

This key should stay private and should not be uploaded to GitHub.

## Notes

LocalLoop is designed as an educational and community-resource tool. Some information may be incomplete depending on available public datasets. Users should verify important service information, such as school closures, trash pickup schedules, or healthcare resources, through official local government or service provider websites.

## Author
Created by Samsam and Nity 
```
