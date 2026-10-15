---
title: WebSSH Pro
emoji: 💻
colorFrom: blue
colorTo: gray
sdk: docker
pinned: false
---

# WebSSH Pro

[![Preact](https://img.shields.io/badge/Preact-10.19-673AB8?style=flat-square&logo=preact&logoColor=white)](https://preactjs.com/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.4-3178C6?style=flat-square&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Vite](https://img.shields.io/badge/Vite-5.3-646CFF?style=flat-square&logo=vite&logoColor=white)](https://vitejs.dev/)
[![Express](https://img.shields.io/badge/Express-4.21-000000?style=flat-square&logo=express&logoColor=white)](https://expressjs.com/)
[![Node.js](https://img.shields.io/badge/Node.js-18+-339933?style=flat-square&logo=nodedotjs&logoColor=white)](https://nodejs.org/)
[![Vercel](https://img.shields.io/badge/Deploy-Vercel-000000?style=flat-square&logo=vercel&logoColor=white)](https://vercel.com/)
[![Railway](https://img.shields.io/badge/Deploy-Railway-0B0D0E?style=flat-square&logo=railway&logoColor=white)](https://railway.app/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)

WebSSH Pro is a modern, lightweight, browser-based SSH client and web terminal. It provides direct, secure shell access to remote servers and local environments through an intuitive, tabbed interface.

## Features

- Real-Time SSH2 Sessions: Connect to remote hosts with password, private key, passphrase, and TOTP authentication.
- Local Shell Terminal: Built-in local pseudo-terminal session powered by a Python PTY bridge.
- Multi-Tab Workspace: Run multiple concurrent sessions with automated operating system identification and official badges.
- Accelerated Rendering: Powered by xterm.js with WebGL hardware acceleration, 256 colors, and truecolor support.
- Quick Connect: Fast connection parsing supporting standard syntax such as `user@hostname` or `ssh -p 22 user@hostname`.
- Responsive Controls: Touch and desktop context menu for copy, paste, clear, and terminal selection.
- Zero External Telemetry: Completely self-contained execution with credentials kept strictly in memory.

## Architecture

- Frontend: Preact 10, TypeScript 5, xterm.js 5, SCSS, Vite 5
- Backend: Node.js 18+, Express 4, WebSocket (`ws`), SSH2
- PTY Bridge: Python 3 pseudo-terminal master/slave bridge

## Getting Started

### Prerequisites

- Node.js 18+
- Python 3

### Installation

```bash
npm install
```

### Environment Configuration

Configure optional environment variables in `.env`:

```env
PORT=3000
HOST=0.0.0.0
```

### Running in Development

```bash
npm run dev
```

### Building for Production

```bash
npm run build
npm start
```

### Deployment

Fully compatible with **Vercel**, Docker, Railway, and VPS:

- **Vercel**: Import your repository into Vercel and deploy instantly (configured via `vercel.json` with serverless API and routing).
- **Docker**: Build and run with the included `Dockerfile`.
- **Railway / VPS**: Binds to `0.0.0.0:$PORT` automatically.

## Security

All credentials entered in the client (passwords, private keys, TOTP tokens) are used solely to establish the direct SSH2 connection tunnel and are never persisted to disk or external databases.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
