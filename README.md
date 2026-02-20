# Real-Time Location Tracker

A real-time location tracking application that allows multiple users to share their live location on an interactive map. Built with Node.js, Express, Socket.io, and Leaflet.js.

## 🌟 Features

- **Real-Time Location Tracking**: Track multiple users' locations simultaneously using WebSocket connections
- **Interactive Map**: Visualize locations on an interactive map powered by Leaflet.js and OpenStreetMap
- **Live Updates**: See location updates in real-time as users move
- **User Management**: Automatically handles user connections and disconnections
- **High Accuracy**: Uses browser's geolocation API with high accuracy settings
- **Responsive Design**: Full-screen map interface that works on desktop and mobile devices

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Real-Time Communication**: Socket.io
- **Frontend**: HTML5, CSS3, JavaScript
- **Mapping**: Leaflet.js
- **Templating**: EJS
- **Maps Provider**: OpenStreetMap

## 📋 Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (v14 or higher)
- npm (Node Package Manager)

## 🚀 Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/realtimetracker_project.git
cd realtimetracker_project
```

2. Install dependencies:
```bash
npm install
```

## 💻 Usage

1. Start the server:
```bash
node app.js
```

2. Open your browser and navigate to:
```
http://localhost:3000
```

3. Allow location permissions when prompted by your browser

4. Your location will be tracked and displayed on the map in real-time

5. Open multiple browser windows/tabs or share the URL with others to see multiple users on the map simultaneously

## 📱 How It Works

1. **Location Detection**: The application uses the browser's Geolocation API to continuously track the user's position
2. **WebSocket Communication**: Location data is sent to the server via Socket.io WebSocket connections
3. **Real-Time Broadcasting**: The server broadcasts location updates to all connected clients
4. **Map Visualization**: Each user's location is displayed as a marker on the interactive map
5. **Dynamic Updates**: Markers automatically update their position as users move
6. **Cleanup**: When a user disconnects, their marker is automatically removed from the map

## 🔧 Configuration

The server runs on port `3000` by default. To change the port, modify the `server.listen()` call in `app.js`:

```javascript
server.listen(3000); // Change 3000 to your desired port
```

## 📁 Project Structure

```
realtimetracker_project/
├── app.js              # Main server file
├── package.json        # Dependencies and project metadata
├── views/
│   └── index.ejs       # Main HTML template
├── public/
│   ├── css/
│   │   └── style.css   # Stylesheet
│   └── js/
│       └── script.js   # Client-side JavaScript
└── README.md           # Project documentation
```

## 🔒 Privacy & Security

- Location data is only shared with other users connected to the same server instance
- No location data is stored persistently
- All communication happens in real-time via WebSocket connections
- Users must explicitly grant location permissions in their browser

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## 📝 License

This project is licensed under the ISC License.

## 🙏 Acknowledgments

- [Leaflet.js](https://leafletjs.com/) for the mapping library
- [OpenStreetMap](https://www.openstreetmap.org/) for map tiles
- [Socket.io](https://socket.io/) for real-time communication

## 📧 Contact

For questions or suggestions, please open an issue on GitHub.

---

**Note**: This application requires HTTPS or localhost to access geolocation features in modern browsers. For production deployment, ensure you use HTTPS.

