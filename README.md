# Kahoot Replica - Interactive Quiz Game Platform 🎮

A real-time, interactive quiz game platform inspired by Kahoot, built with **Spring Boot**, **WebSockets**, and **The Movie Database (TMDB) API**. Features live multiplayer sessions, real-time scoring, and movie-based quizzes.

## 📋 Overview

**Kahoot Replica** is a full-featured quiz game platform that enables:
- Real-time multiplayer quiz sessions
- Live scoring and leaderboards
- Movie-based question generation
- WebSocket-based real-time communication
- Session management and user tracking

Perfect for learning WebSockets, real-time applications, and game development patterns.

## ✨ Features

- 🎮 **Real-Time Multiplayer** - Join quiz sessions with WebSocket support
- 🎬 **Movie-Based Quizzes** - Questions generated from TMDB API
- 📊 **Live Leaderboard** - Real-time scoring and rankings
- 👥 **Session Management** - Create and join quiz sessions
- ⚡ **WebSocket Communication** - Instant updates and responses
- 🎯 **Multiple Question Types** - Various quiz formats supported
- 📈 **User Rankings** - Track player performance

## 🛠️ Technology Stack

- **Java** - Core programming language
- **Spring Boot** - Application framework
- **WebSockets** - Real-time communication
- **Spring WebSocket** - WebSocket support
- **The Movie DB API** - Movie data source
- **Maven** - Build and dependency management

## 🚀 Getting Started

### Prerequisites

- Java 8+
- Maven 3.x
- TMDB API key (optional, for movie quizzes)

### Installation

1. **Clone the repository:**
```bash
git clone https://github.com/bhanuchaddha/Kahoot-Replica.git
cd Kahoot-Replica
```

2. **Build the project:**
```bash
mvn clean install
```

3. **Run the application:**
```bash
mvn spring-boot:run
```

The application will start on `http://localhost:8080`

## 📡 API Endpoints

### Quiz Management

```http
GET  /api/quiz          # Get available quizzes
POST /api/quiz          # Create new quiz
GET  /api/quiz/{id}     # Get quiz details
```

### Session Management

```http
POST /api/session/join      # Join a quiz session
POST /api/session/answer    # Submit answer
GET  /api/session/rankings  # Get current rankings
```

### WebSocket Endpoints

- `/ws/session` - WebSocket connection for real-time updates

## 🏗️ Project Structure

```
Kahoot-Replica/
├── src/main/java/com/bhanuchaddha/gtmg/
│   ├── quiz/              # Quiz logic
│   │   ├── model/         # Quiz models
│   │   ├── dto/           # Data transfer objects
│   │   └── QuizService.java
│   ├── movies/            # Movie integration
│   │   ├── integration/   # TMDB API client
│   │   └── model/         # Movie models
│   ├── session/           # Session management
│   │   ├── service/       # Session services
│   │   ├── repository/    # Data repositories
│   │   └── WebSocketController.java
│   └── GuessTheMovieGameApplication.java
└── src/main/resources/
    └── public/            # Frontend HTML files
        ├── Dashboard.html
        └── User.html
```

## 🎮 How It Works

1. **Create/Join Session** - Host creates a quiz session, players join
2. **Question Display** - Questions are displayed to all participants
3. **Answer Submission** - Players submit answers via WebSocket
4. **Real-Time Scoring** - Scores calculated and broadcast instantly
5. **Leaderboard** - Rankings updated in real-time

## 🔧 Configuration

### Application Properties

```properties
server.port=8080
# Add TMDB API key if using movie quizzes
tmdb.api.key=your-api-key-here
```

### WebSocket Configuration

WebSocket is configured in `WebSocketConfig.java`:
- STOMP messaging protocol
- Message broker for broadcasting
- Session management

## 🧪 Testing

```bash
# Run tests
mvn test

# Run specific test
mvn test -Dtest=QuizServiceTest
```

## 📚 Key Features Demonstrated

- **WebSocket Communication** - Real-time bidirectional communication
- **Session Management** - Multi-user session handling
- **External API Integration** - TMDB API integration
- **Real-Time Scoring** - Instant score calculation
- **Leaderboard System** - Live rankings

## 🎓 Learning Objectives

This project demonstrates:
- WebSocket implementation with Spring
- Real-time application patterns
- Session management strategies
- Game development concepts
- API integration patterns

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is open source and available for educational purposes.

## 🔗 Resources

- [Spring WebSocket Documentation](https://docs.spring.io/spring-framework/reference/web/websocket.html)
- [The Movie Database API](https://www.themoviedb.org/documentation/api)
- [Kahoot Platform](https://kahoot.com/)

## 🌟 Use Cases

- **Learning WebSockets** - Real-time communication tutorial
- **Game Development** - Quiz game patterns
- **Educational Platform** - Interactive learning tools
- **Event Hosting** - Live quiz sessions
- **Team Building** - Corporate quiz activities

---

**Built with Spring Boot & WebSockets ❤️**
