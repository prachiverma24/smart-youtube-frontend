# YouTube Learning Assistant - Frontend

A modern React-based web application that transforms YouTube videos into structured learning content with AI-generated summaries, key points, and interactive quiz questions.

## 🚀 Features

- **YouTube URL Processing**: Paste any YouTube video URL to generate learning content
- **Direct Transcript Input**: Manually paste transcripts for processing
- **AI-Powered Content Generation**: 
  - Comprehensive video summaries
  - Key learning points extraction
  - Interactive quiz questions with multiple choice answers
- **Interactive Quiz Interface**:
  - Clickable answer options
  - Visual feedback for correct/incorrect answers
  - Show/Hide answer functionality
- **Responsive Design**: Beautiful gradient UI that works on all devices
- **Real-time Processing**: Live status updates during content generation

## 🛠️ Tech Stack

- **React 18.2.0**: Modern React with Hooks
- **CSS3**: Custom styling with gradients and animations
- **Fetch API**: RESTful API communication
- **Node.js Environment**: Development and build tools

## 📋 Prerequisites

- Node.js (v14 or higher)
- npm or yarn package manager
- Backend API running (see backend repository)

## 🔧 Installation

1. **Clone the repository**
```bash
git clone https://github.com/prachiverma24/smart-youtube-frontend.git
cd smart-youtube-frontend
```

2. **Install dependencies**
```bash
npm install
```

3. **Configure Environment Variables** (Optional)
Create a `.env` file in the root directory:
```
REACT_APP_API_URL=http://localhost:5000/api
```

4. **Start the development server**
```bash
npm start
```

The app will open at `http://localhost:3000`

## 🎯 Usage

### YouTube URL Mode
1. Select "YouTube URL" tab
2. Paste a YouTube video URL
3. Click "Generate Learning Content"
4. Wait for processing (15-30 seconds)
5. View summary, key points, and take the quiz!

### Direct Transcript Mode
1. Select "Paste Transcript" tab
2. Enter a video title (optional)
3. Paste the transcript text (minimum 50 characters)
4. Click "Generate Learning Content"
5. Explore the AI-generated content

### Quiz Interaction
- Click on any answer option to select it
- Click "Show Answer" to reveal the correct answer
- Selected answers are highlighted in blue
- Correct answers show in green
- Incorrect selections show in red

## 📁 Project Structure

```
smart-youtube-frontend/
├── public/
│   └── index.html          # HTML template
├── src/
│   ├── App.js              # Main React component
│   ├── App.css             # Styling
│   └── index.js            # React entry point
├── package.json            # Dependencies
└── README.md              # This file
```

## 🎨 Key Components

### State Management
- `youtubeUrl`: Stores the YouTube URL input
- `transcript`: Stores direct transcript input
- `result`: Stores the AI-generated content
- `showAnswers`: Tracks which quiz answers are visible
- `selectedAnswers`: Tracks user's selected quiz options
- `loading`: Controls loading state
- `error`: Stores error messages

### API Endpoints Used

**Process YouTube Video**
```javascript
POST /api/videos/process
Body: { youtubeUrl: string }
```

**Process Direct Transcript**
```javascript
POST /api/videos/transcript
Body: { transcript: string, title: string }
```

## 🎨 Styling Features

- Modern gradient background (purple to violet)
- Smooth animations and transitions
- Interactive hover effects
- Responsive design for mobile/tablet
- Color-coded quiz feedback system
- Loading spinner with status messages

## 🔌 Backend Integration

This frontend requires the YouTube Learning Assistant backend API. Make sure the backend is running before starting the frontend.

Default backend URL: `http://localhost:5000/api`

## 🚀 Building for Production

```bash
npm run build
```

This creates an optimized production build in the `build/` directory.

## 🌐 Deployment

### Deploy to Vercel
```bash
npm install -g vercel
vercel
```

### Deploy to Netlify
```bash
npm install -g netlify-cli
netlify deploy --prod
```

### Environment Variables for Production
Set `REACT_APP_API_URL` to your production backend URL.

## 🐛 Troubleshooting

**Issue**: "Could not fetch transcript from any source"
- Solution: Try a different YouTube video with captions enabled

**Issue**: API connection errors
- Solution: Verify backend is running on the correct port
- Check CORS configuration on backend

**Issue**: Quiz buttons not working
- Solution: Clear browser cache and refresh

## 📝 Recent Updates

- ✅ Added interactive quiz with clickable options
- ✅ Implemented visual feedback for correct/incorrect answers
- ✅ Fixed "Show Answer" button functionality
- ✅ Enhanced user experience with hover effects
- ✅ Improved error handling and loading states

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📄 License

This project is open source and available under the MIT License.

## 👥 Author

**Prachi Verma**
- GitHub: [@prachiverma24](https://github.com/prachiverma24)

## 🔗 Related Projects

- [Backend Repository](https://github.com/payal360/youtube-learning-assistant) - Node.js/Express backend with AI integration

## 💡 Future Enhancements

- [ ] Save learning sessions to local storage
- [ ] Export quiz results as PDF
- [ ] Add more question types (true/false, fill-in-the-blank)
- [ ] User authentication and progress tracking
- [ ] Social sharing features
- [ ] Dark mode toggle
- [ ] Multi-language support

---

Made with ❤️ using React and AI
