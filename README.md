# Better OBS

A modern Vue.js application built with TypeScript and Radix Vue components.

## Project Structure

```
better-obs/
├── frontend/           # Vue.js frontend application
│   ├── src/            # Source code
│   │   ├── components/ # Vue components
│   │   │   └── ui/     # Reusable basic UI components
│   │   ├── layouts/    # Layout components
│   │   └── App.vue     # Root component
│   └── package.json    # Frontend dependencies and scripts
└── backend/            # Backend application (WIP)
```

## Technology Stack

- **Frontend Framework**: Vue 3 with TypeScript
- **Build Tool**: Vite
- **UI Components**: Radix Vue
- **Styling**: TailwindCSS
- **Code Quality**: Prettier, TypeScript

## Getting Started

### Prerequisites

- Bun
- Python

or simply

- Docker

### Installation

1. Clone the repository
2. Install frontend dependencies:

```bash
cd frontend
npm install
```

### Development

To start the development server:

```bash
cd frontend
bun dev
```

This will start the Vite development server with hot module replacement (HMR).

### Building for Production

To create a production build:

```bash
cd frontend
bun build
```

The built files will be in the `frontend/dist` directory.

To preview the production build locally:

```bash
cd frontend
bun preview
```

## Features

- Modern Vue 3 Composition API with TypeScript
- Custom UI components including tooltips
- Responsive layouts
- Type-safe development experience
- Fast development with Vite
- Consistent code style with Prettier

## Development Tools

- **TypeScript**: For type safety and better developer experience
- **Vite**: Fast development server and build tool
- **Prettier**: Code formatting
- **TailwindCSS**: Utility-first CSS framework

## Scripts

- `bun dev`: Start development server
- `bun run build`: Build for production
- `bun run preview`: Preview production build locally

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

MIT
