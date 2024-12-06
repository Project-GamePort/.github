# We Are Project 🎮 Gameport ⚓




GamePort is an online multiplayer gaming system for the web. A vertically scalable system, that allows the vinculation of one or more game-servers to a core backend. 

The core backend handles basic business logic such as managing sessions, users, game-rooms, and monitoring game hosts. Through it's API, users can register and login. Additionally, it communicates with game hosts, allowing logged-in players to select and join an available game-room. An instance of the core backend is called a "central-server". Multiple central-servers can constitute a escalable monolith, allowing load-balancing using NGINX as proxy.

Game-servers host and run online multiplayer games. Data syncronization among players is achieved using web-sockets. Each server can run one or more games concurrently, thanks to worker-threads. Access control is token-based; there is a whitelist for each game: a list of tokens generated for each player that requests joining in; only those players whose tokens match the whitelist's will be granted access. Each worker-thread corresponds to a game-room, which follows a cycle: wait, match, gameover, repeat. 
<!--
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
