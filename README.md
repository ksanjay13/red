# Movie Recommendation Bot

An AI-powered movie recommendation chatbot built with React and the Gemini API. This application provides personalized movie suggestions based on user preferences and maintains conversation context for better recommendations.

## Features

- 🤖 **AI-Powered Recommendations**: Uses Google's Gemini API for intelligent movie suggestions
- 💬 **Conversational Interface**: Chat-like interface with typing indicators and smooth animations
- 🎯 **Context-Aware**: Remembers conversation history for better personalized recommendations
- 📱 **Responsive Design**: Works seamlessly on desktop and mobile devices
- 🎨 **Modern UI**: Beautiful dark theme with smooth animations and hover effects
- 🔗 **Quick Search**: Direct links to Google search for each recommended movie

## Prerequisites

- Node.js (version 14 or higher)
- npm or yarn
- Google Gemini API key

## Setup Instructions

1. **Clone or download the project files**

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up your Gemini API key**
   
   Create a `.env` file in the root directory and add your API key:
   ```
   REACT_APP_GEMINI_API_KEY=your_gemini_api_key_here
   ```
   
   To get a Gemini API key:
   - Go to [Google AI Studio](https://makersuite.google.com/app/apikey)
   - Sign in with your Google account
   - Create a new API key
   - Copy the key and paste it in your `.env` file

4. **Start the development server**
   ```bash
   npm start
   ```

5. **Open your browser**
   
   The application will open at `http://localhost:3000`

## Usage

1. **Start a conversation**: The bot will greet you with an initial message
2. **Ask for recommendations**: Describe what kind of movie you're looking for
   - Examples: "a funny sci-fi movie from the 80s"
   - Examples: "something with a strong female lead"
   - Examples: "a thriller that will keep me guessing"
3. **Get personalized suggestions**: The bot will recommend up to 3 movies with reasons
4. **Explore movies**: Click "Find on Google" to search for more information about each movie
5. **Continue the conversation**: Ask follow-up questions for more specific recommendations

## Project Structure

```
movie-recommendation-bot/
├── public/
│   └── index.html          # Main HTML file
├── src/
│   ├── App.js             # Main React component
│   ├── index.js           # React entry point
│   └── index.css          # Global styles and Tailwind imports
├── package.json           # Dependencies and scripts
├── tailwind.config.js     # Tailwind CSS configuration
├── .env                   # Environment variables (create this)
└── README.md             # This file
```

## Technologies Used

- **React 18**: Modern React with hooks
- **Tailwind CSS**: Utility-first CSS framework
- **Google Gemini API**: AI-powered text generation
- **Fetch API**: For making HTTP requests
- **CSS Animations**: Custom keyframe animations

## API Configuration

The application uses the Gemini 2.5 Flash model with structured JSON responses. The API call includes:

- **Model**: `gemini-2.5-flash-preview-05-20`
- **Response Format**: Structured JSON with `response` and `recommendations` fields
- **Schema Validation**: Ensures proper movie object structure

## Customization

### Styling
- Modify `src/index.css` for global styles
- Update `tailwind.config.js` for theme customization
- Edit the `GlobalStyles` component in `App.js` for custom animations

### API Integration
- Change the model in the `apiUrl` variable
- Modify the prompt in `generatePrompt()` function
- Adjust the response schema in the API payload

## Troubleshooting

### Common Issues

1. **API Key Error**
   - Ensure your `.env` file is in the root directory
   - Check that the API key is correct and active
   - Restart the development server after adding the `.env` file

2. **CORS Issues**
   - The Gemini API supports CORS for browser requests
   - If you encounter issues, check your API key permissions

3. **Build Errors**
   - Clear `node_modules` and reinstall: `rm -rf node_modules && npm install`
   - Check Node.js version compatibility

## License

This project is open source and available under the MIT License.

## Contributing

Feel free to submit issues and enhancement requests! 