# VideoGo

A peer-to-peer (P2P) video conferencing application built with the MERN stack (MongoDB, Express, React, Node.js). This app provides real-time video communication, chat messaging, and screen sharing using WebRTC, with signaling handled via a Node.js backend.

* **Live App : [ videogo.jayyu.in](https://videogo.jayyu.in)**
* **Demo Video : [Drive Link](https://drive.google.com/file/d/1nu4LbBeY6w_qEdUMHV3ZdlW9BzaW7PeI/view?usp=sharing)**
* **Repository : [ jayesh-verma-code/VideoGo](https://github.com/jayesh-verma-code/VideoGo)**
---
![VideoGo Landing Page](https://res.cloudinary.com/dzhczzqwf/image/upload/v1774531079/Screenshot_2026-03-26_183944_edoxst.png)

## Features

* Peer-to-peer video/audio calling using WebRTC
* Real-time text chat
* Screen sharing
* Room-based conferencing
* Scalable signaling server using WebSockets (Socket.IO)
* Responsive UI built with React
* Deployment-ready setup (Vercel + Render)

## Requirement Gathering Phase
![Requirement Grathering Phase](https://res.cloudinary.com/dzhczzqwf/image/upload/v1774308999/ChatGPT_Image_Mar_24_2026_05_05_52_AM_oqt8nr.png)

## Technologies

|Components|Technologies|
|-|-|
|Database|MongoDB|
|Backend|bcrypt, crypto, Socket.io, ExpressJS/NestJS/Fastify|
|Frontend|ReactJS, CSS3, WebRTC, Axios, Material UI|

> Socket.io smartly switchs between WebRTC to Long polling for reducing system failure.

## Project Structure

```
VideoGo/
│
├── frontend/                # React frontend
│   ├── src/
│   ├── public/
│   └── package.json
│
├── backend/                # Node/Express backend
│   ├── controllers/
│   ├── routes/
│   ├── socket/
│   └── package.json
│
├── README.md
```

## Installation

### Prerequisites

* Node.js (v16+ recommended)
* npm or yarn
* MongoDB (local or cloud instance)

### Clone the Repository

```
git clone https://github.com/jayesh-verma-code/VideoGo
cd VideoGo
```

### Setup Backend

```
cd backend
npm install
```

Create a `.env` file in the `server` directory:

```
PORT=8000
MONGO_URI=your_mongodb_connection_string
```

Start the backend:

```
npm run dev
```

### Setup Frontend

```
cd frontend
npm install
```

Create a `.env` file in the `client` directory:

```
REACT_APP_SERVER_URL=http://localhost:8000
```

Start the frontend:

```
npm start
```


## Known Limitations

* P2P architecture may not scale well for large groups
* Network/firewall restrictions may affect connectivity
* No TURN server may cause issues in restrictive networks
