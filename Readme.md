# TypeScript Node.js Setup Guide 🚀

This repository demonstrates how to initialize and configure a Node.js project with TypeScript, providing a foundation for your TypeScript Node.js applications.

## Prerequisites

- Node.js installed on your machine.
- `npm` as the package manager.

## Quick Start

1. Clone this repository:

```bash
git clone https://github.com/yourusername/typescript-node-setup.git

```

```bash
cd typescript-node-setup
```

2. Install dependencies:


```bash
npm install
```

3. Start development server:

```bash
npm run dev
```

## Step-by-Step Setup Guide

### 1. Initialize the Project and Install Dependencies

 Initialize a new Node.js project

```bash
npm init -y

```
Install necessary dependencies

```bash
npm install -D @types/node tsx typescript

```

### 2. Configure TypeScript

Create and configure `tsconfig.json`:

Generate tsconfig.json

```bash
npx tsc --init
```

Update `tsconfig.json` with the following configuration:

```json
{
  "compilerOptions": {
    "esModuleInterop": true,
    "skipLibCheck": true,
    "target": "ES2020",
    "allowJs": true,
    "resolveJsonModule": true,
    "moduleDetection": "force",
    "isolatedModules": true,
    "verbatimModuleSyntax": true,
    "strict": true,
    "noUncheckedIndexedAccess": true,
    "noImplicitOverride": true,
    "module": "NodeNext",
    "moduleResolution": "NodeNext",
    "outDir": "./dist",
    "rootDir": "./src",
    "sourceMap": true
  }
}
```

### 3. Update package.json

Update your `package.json` to include:

Note: If your project doesn't need .env file then remove .env from scripts.

```json
{
  "type": "module",
  "scripts": {
    "dev": "tsx watch --env-file .env src/index.ts",
    "build": "tsc",
    "start": "node --env-file .env dist/index.js"
  }
}
```

## Project Structure

```
.
├── src/
│   └── index.ts
├── dist/
├── .env
├── .gitignore
├── package.json
├── tsconfig.json
└── README.md
```

## Scripts

- `npm run dev` - Start development server
- `npm run build` - Build the TypeScript project
- `npm start` - Run the built application

## Environment Variables

Create a `.env` file in the root directory for your environment variables:

```env
PORT=6969
NODE_ENV=development
```

## Best Practices

1. Keep source files in the `src` directory
2. Use ES modules (`import`/`export`) syntax
3. Enable strict TypeScript checks
4. Use `.env` file for environment variables


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.