# Sports Players Hub 🏀⚽🎾

A React-based web application that showcases sports players information using interactive cards with dynamic data loading.

## 🌟 Features

- **Player Cards**: Beautiful card layout displaying player information
- **Dynamic Data Loading**: Uses JavaScript mapping to render players from data file
- **Props Utilization**: Efficient data passing between components
- **Responsive Design**: Works on desktop, tablet, and mobile devices
- **Clean UI**: Modern and user-friendly interface

## 🛠️ Technologies Used

- React.js
- JavaScript (ES6+)
- JSX
- CSS3
- HTML5

## 🚀 Getting Started

### Prerequisites
- Node.js installed on your machine
- npm or yarn package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/sports-players-hub.git
   cd sports-players-hub
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   ```

4. **Open your browser**
   Navigate to `http://localhost:3000`

## 📊 Data Structure

The application uses `playerData.js` which contains an array of player objects:

```javascript
const playerData = [
  {
    id: 1,
    name: "Player Name",
    sport: "Sport Type",
    team: "Team Name",
    position: "Player Position",
    stats: {
      goals: 0,
      assists: 0,
      // other statistics
    },
    image: "player-image-url",
    description: "Player bio description"
  },
  // ... more players
];
```

## 🎯 How It Works

### 1. Data Flow
- `playerData.js` contains all player information
- `MainPage.js` imports the data and maps through it
- `PlayerCard.js` receives data via props and displays it

### 2. Component Structure
```javascript
// MainPage.js
import playerData from '../data/playerData';

const MainPage = () => {
  return (
    <div className="main-page">
      {playerData.map(player => (
        <PlayerCard key={player.id} player={player} />
      ))}
    </div>
  );
};
```

```javascript
// PlayerCard.js
const PlayerCard = ({ player }) => {
  return (
    <div className="player-card">
      <img src={player.image} alt={player.name} />
      <h3>{player.name}</h3>
      <p>{player.sport} • {player.team}</p>
      {/* Additional player info */}
    </div>
  );
};
```

## 🎨 Customization

### Adding New Players
Edit `src/data/playerData.js`:
```javascript
{
  id: 10,
  name: "New Player",
  sport: "Basketball",
  team: "Lakers",
  position: "Forward",
  stats: {
    points: 25.6,
    rebounds: 7.8,
    assists: 10.2
  },
  image: "new-player.jpg",
  description: "Description of the new player"
}
```

### Styling Changes
Modify CSS files in respective component folders to change the appearance.

## 📱 Responsive Design

The application is fully responsive and will adapt to:
- Desktop screens (1200px+)
- Tablets (768px - 1199px)
- Mobile devices (< 768px)

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🙏 Acknowledgments

- React team for the amazing framework
- Unsplash for player images
- Sports data sources for player information

---

**Enjoy exploring sports players!** ⚽🏀🎾🏈
