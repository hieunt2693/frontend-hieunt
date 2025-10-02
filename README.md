# React TypeScript Project with Vite

This project is a modern React TypeScript application built with Vite, featuring ESLint and Prettier for code quality and formatting.

## Available Scripts

In the project directory, you can run:

### `npm run dev`

Runs the app in development mode with hot module replacement (HMR).\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.\
Note: If port 3000 is in use, Vite will automatically use the next available port.

### `npm run build`

Builds the app for production to the `dist` folder.\
The build is optimized and ready for deployment.

### `npm run preview`

Previews the production build locally.

### `npm run lint`

Runs ESLint to check for code style and potential errors in `.js`, `.jsx`, `.ts`, and `.tsx` files.\
ESLint is configured with TypeScript and React specific rules.

### `npm run format`

Formats all source files using Prettier.\
This will format `.js`, `.jsx`, `.ts`, `.tsx`, `.css`, and `.md` files according to the project's style guide.

### `npm run format:check`

Checks if all files are properly formatted without making changes.\
Useful in CI/CD pipelines or before committing.

## Code Style and Quality

### ESLint Configuration

The project uses ESLint with the following key configurations:

- TypeScript support via @typescript-eslint
- React and React Hooks specific rules
- Integration with Prettier for consistent code formatting

Key rules include:

- Semicolons required
- Single quotes for strings
- No unused variables (warning)
- React Hooks dependencies checking
- And more (see `eslint.config.js`)

### Prettier Configuration

Code formatting is handled by Prettier with these settings:

- Tab Width: 2 spaces
- Print Width: 100 characters
- Single Quotes: true
- Trailing Comma: es5
- Bracket Spacing: true
- Arrow Function Parentheses: avoid when possible
- End of Line: LF

## Development with Vite

Vite is configured for optimal development experience:

- Fast hot module replacement (HMR)
- TypeScript support out of the box
- Automatic port assignment if default is in use
- Source maps in development
- Path aliases (@/ points to src/)

## Project Structure

```
├── public/          # Static assets
├── src/            # Source code
├── .gitignore      # Git ignore rules
├── .prettierrc     # Prettier configuration
├── eslint.config.js # ESLint configuration
├── index.html      # Entry HTML file
├── package.json    # Project dependencies and scripts
├── tsconfig.json   # TypeScript configuration
└── vite.config.ts  # Vite configuration
```

## Getting Started

1. Install dependencies:

   ```bash
   npm install
   ```

2. Start development server:

   ```bash
   npm run dev
   ```

3. Before committing code:
   ```bash
   npm run lint    # Check for code style issues
   npm run format  # Fix formatting
   ```

## Git Hooks and Commit Convention

This project uses Husky and Commitlint to maintain code quality and consistent commit messages.

### Pre-commit Hook

Before each commit, the following checks are automatically run:

- ESLint will check and fix possible issues
- Prettier will format changed files
- TypeScript compilation errors will be caught

### Commit Message Convention

Commits must follow the [Conventional Commits](https://www.conventionalcommits.org/) specification. Each commit message must be structured as follows:

```
<type>: <description>

[optional body]

[optional footer]
```

Types available:

- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `build`: Build system or external dependency changes
- `ci`: CI configuration changes
- `chore`: Other changes that don't modify src or test files

Examples:

```
feat: Add user authentication
fix: Resolve memory leak in useEffect
docs: Update deployment instructions
```

### Commit Best Practices

1. Run tests before committing:

   ```bash
   npm test
   ```

2. Stage your changes:

   ```bash
   git add .
   ```

3. Commit with a conventional message:
   ```bash
   git commit -m "type: Description starting with capital letter"
   ```

The commit will only succeed if:

- The code passes ESLint checks
- All files are properly formatted
- The commit message follows the conventional format
