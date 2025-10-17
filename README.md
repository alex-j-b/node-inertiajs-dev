# Node Inertia.js Development Repository

This repository is a development workspace for testing and developing the Node Inertia.js adapter packages.

## 📦 Packages

This repo contains three interconnected packages:

### Core Package

- **`node-inertiajs/`** - Framework-agnostic core library

### Framework Adapters

- **`express-inertia/`** - Express.js adapter
- **`fastify-inertia/`** - Fastify adapter

## 🔗 Local Development

The packages are linked using relative file paths, allowing for seamless local development and testing without publishing to npm.

### Package Dependencies

Both `express-inertia` and `fastify-inertia` can reference the local `node-inertiajs` package for development purposes:

```json
{
  "dependencies": {
    "node-inertiajs": "file:../node-inertiajs"
  }
}
```

## 🚀 Getting Started

### Install Dependencies

```bash
# Install dependencies for each package
cd node-inertiajs && npm install
cd ../express-inertia && npm install
cd ../fastify-inertia && npm install
```

### Build Core Package

The framework adapters depend on the built version of `node-inertiajs`:

```bash
cd node-inertiajs
npm run build
```

### Test Framework Adapters

```bash
# Test Express adapter
cd express-inertia
npm run dev

# Test Fastify adapter
cd fastify-inertia
npm run dev
```
