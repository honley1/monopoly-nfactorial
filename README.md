# Monopoly Web Game

## Project Description
This is a web-based implementation of the classic Monopoly board game. The game features a complete Monopoly experience with property trading, auctions, chance and community chest cards, and an AI opponent system. The project includes multiple city editions (Mumbai Edition by default, with New York City Edition available) that customize the game board with location-specific properties.

## Installation and Setup

### Prerequisites
- A modern web browser (Chrome, Firefox, Safari, Edge)
- No server-side installation required (client-side JavaScript only)

### Running the Game
1. Clone the repository or download the source code
2. Open `index.html` in your web browser
3. Select the number of players and customize player settings
4. Click "Start Game" to begin playing

You can also host the files on any web server to make the game accessible online.

## Game Features
- Complete implementation of Monopoly game rules
- Multiple city editions (Mumbai Edition, New York City Edition)
- Support for 2-8 players
- AI opponents with strategic decision-making
- Property trading system
- Auction system for unsold properties
- Mortgage and unmortgage functionality
- House and hotel building
- Chance and Community Chest cards
- Jail mechanics
- Responsive game board design

## Design and Development Process

### Architecture
The game is built using vanilla JavaScript with jQuery for DOM manipulation. The project follows an object-oriented approach with the following main components:

1. **Game Logic (`monopoly.js`)**: Contains the core game mechanics, turn management, and player interactions
2. **AI System (`bot.js`)**: Implements computer player behavior with decision-making capabilities
3. **Game Editions (`editions/`)**: Contains city-specific configurations for the game board
4. **UI Layer**: HTML and CSS for the game board and interactive elements

### Development Approach
The development process focused on creating a faithful recreation of the Monopoly board game while adding digital enhancements like AI opponents. The code structure separates game logic from presentation, allowing for different city editions to be implemented without changing the core mechanics.

## Unique Approaches and Methodologies

### AI Implementation
The bot system uses a combination of rule-based decision-making and a machine learning model to determine property purchases and trading strategies. The AI evaluates:
- Current financial status
- Property ownership patterns
- Strategic value of properties
- Risk assessment for auctions and trades

The machine learning model (found in the `model/` directory) was trained on gameplay data to optimize decision-making for property purchases.

### City Editions System
The game implements a modular approach to city editions, allowing different themed boards to be loaded without changing the core game logic. This is achieved through JavaScript configuration files that define:
- Property names and prices
- Color groups
- Rent values
- Special card text

## Technical Stack and Rationale

### Technologies Used
- **HTML/CSS/JavaScript**: Core web technologies for client-side implementation
- **jQuery**: Used for DOM manipulation and event handling
- **TensorFlow.js**: Machine learning library for AI decision-making (referenced in bot.js)

### Why This Stack?
1. **Accessibility**: The game runs entirely in the browser without requiring server-side components, making it easy to deploy and play
2. **Performance**: Vanilla JavaScript provides excellent performance for the game logic
3. **Compatibility**: The chosen technologies ensure broad browser compatibility
4. **Maintainability**: The object-oriented approach and separation of concerns make the codebase easier to maintain and extend
5. **Learning Curve**: The stack uses widely-known technologies, making it accessible for contributors

## Design Tradeoffs

### Browser-Based vs. Server-Based
- **Chosen Approach**: Fully browser-based implementation
- **Tradeoff**: While this approach makes the game immediately playable without installation, it limits multiplayer capabilities to local play only
- **Rationale**: Prioritized ease of access and deployment over network multiplayer functionality

### AI Complexity vs. Performance
- **Chosen Approach**: Hybrid rule-based and machine learning approach
- **Tradeoff**: Full machine learning implementation would provide more sophisticated AI but would increase complexity and resource usage
- **Rationale**: The current approach balances AI intelligence with performance considerations

### Game Editions vs. Single Version
- **Chosen Approach**: Modular city editions system
- **Tradeoff**: Increases code complexity but provides greater customization
- **Rationale**: The ability to play with different city themes enhances replay value and user engagement

## Known Issues and Limitations

1. **AI Limitations**: The bot AI makes reasonable decisions but may not employ advanced strategies that human players would use
2. **No Online Multiplayer**: The game currently only supports local multiplayer
3. **Mobile Responsiveness**: While playable on mobile devices, the interface is optimized for desktop screens
4. **Browser Compatibility**: Some advanced features may not work in older browsers
5. **TensorFlow Integration**: The TensorFlow.js integration referenced in the bot.js file may require additional setup for full functionality

## Future Improvements

1. Implement online multiplayer functionality
2. Enhance mobile responsiveness
3. Add more city editions
4. Improve AI decision-making with more advanced algorithms
5. Add game statistics and history tracking
6. Implement save/load game functionality

## License
This project is available for educational and personal use.