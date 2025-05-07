# Video Sharing Platform

This is a simple video-sharing platform inspired by YouTube. It allows users to upload, view, and interact with videos.

## Features
- User Authentication
- Video Upload and Streaming
- Comments and Likes
- Search and Discovery

## Tech Stack
- **Frontend**: React.js
- **Backend**: Node.js with Express
- **Database**: MongoDB
- **Storage**: AWS S3

## Setup Instructions

### Backend
1. Navigate to the `backend` folder.
2. Install dependencies: `npm install`
3. Start the server: `npm start`

### Frontend
1. Navigate to the `frontend` folder.
2. Install dependencies: `npm install`
3. Start the development server: `npm start`

## Future Enhancements
- Add video suggestions
- Implement adaptive bitrate streaming
- Enhance security and scalabilityconst express = require('express');
const mongoose = require('mongoose');
const cors = require('cors');
const app = express();

// Middleware
app.use(cors());
app.use(express.json());

// Connect to MongoDB
mongoose.connect('mongodb://localhost:27017/video-platform', {
  useNewUrlParser: true,
  useUnifiedTopology: true,
});

// Routes
app.get('/', (req, res) => {
  res.send('Video Sharing Platform Backend');
});

// Start Server
const PORT = 5000;
app.listen(PORT, () => {
  console.log(`Backend running on http://localhost:${PORT}`);
});import React from 'react';

function App() {
  return (
    <div>
      <h1>Welcome to the Video Sharing Platform</h1>
    </div>
  );
}

export default App;
