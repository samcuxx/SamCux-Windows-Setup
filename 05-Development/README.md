# 🛠️ Development Environment Setup

## Overview

Complete development environment configuration for software engineers working with modern web technologies, mobile development, and various programming languages.

## 🎯 Tech Stack Coverage

### Frontend Development

- **HTML/CSS/JavaScript** - Web fundamentals
- **React/Vue/Angular** - Modern frameworks
- **TypeScript** - Type-safe JavaScript
- **Tailwind CSS** - Utility-first CSS

### Backend Development

- **Node.js** - JavaScript runtime
- **Python** - Data science and web development
- **Java** - Enterprise applications
- **C#/.NET** - Microsoft stack

### Mobile Development

- **React Native** - Cross-platform mobile
- **Flutter** - Google's mobile framework
- **Android Native** - Kotlin/Java development

### Database & DevOps

- **MongoDB** - NoSQL database
- **PostgreSQL** - Relational database
- **Docker** - Containerization
- **Git** - Version control

## 📋 Environment Setup Checklist

### Essential Development Tools

#### ✅ Code Editors & IDEs

- [ ] **Visual Studio Code** - Primary editor
  - [ ] Essential extensions installed
  - [ ] Settings synchronized
  - [ ] Theme configured
- [ ] **Android Studio** - Mobile development
- [ ] **IntelliJ IDEA** (optional) - Java/Kotlin development

#### ✅ Version Control

- [ ] **Git for Windows** - Version control system
- [ ] **GitHub Desktop** - Git GUI client
- [ ] SSH keys configured for GitHub
- [ ] Global Git configuration set

#### ✅ Runtime Environments

- [ ] **Node.js LTS** - JavaScript runtime
- [ ] **Python 3.11+** - Programming language
- [ ] **Java JDK 17+** - Java development kit
- [ ] **.NET 8** - Microsoft development platform

#### ✅ Package Managers

- [ ] **npm/yarn** - Node.js packages
- [ ] **pip** - Python packages
- [ ] **Chocolatey** - Windows package manager
- [ ] **winget** - Windows Package Manager

#### ✅ Database Tools

- [ ] **MongoDB Compass** - MongoDB GUI
- [ ] **PostgreSQL** - Database system
- [ ] **MySQL Workbench** - MySQL administration
- [ ] **Redis** - In-memory data store

#### ✅ API Development

- [ ] **Postman** - API testing and documentation
- [ ] **Insomnia** - Alternative API client
- [ ] **Thunder Client** - VS Code extension

## 🔧 Detailed Configuration

### Visual Studio Code Setup

#### Essential Extensions

**General Development**

```
# Install via VS Code Extensions or command line
code --install-extension ms-vscode.vscode-typescript-next
code --install-extension esbenp.prettier-vscode
code --install-extension ms-vscode.vscode-eslint
code --install-extension bradlc.vscode-tailwindcss
```

**Frontend Development**

- **ES7+ React/Redux/React-Native snippets**
- **Auto Rename Tag**
- **Bracket Pair Colorizer**
- **Live Server**
- **HTML CSS Support**

**Backend Development**

- **Python**
- **Java Extension Pack**
- **C#**
- **REST Client**

**Productivity**

- **GitLens**
- **Path Intellisense**
- **Auto Import - ES6, TS, JSX, TSX**
- **IntelliSense for CSS class names**

#### VS Code Settings Configuration

Create or update `settings.json`:

```json
{
  "editor.fontSize": 14,
  "editor.fontFamily": "JetBrains Mono, Consolas, 'Courier New', monospace",
  "editor.tabSize": 2,
  "editor.insertSpaces": true,
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "emmet.includeLanguages": {
    "javascript": "javascriptreact",
    "typescript": "typescriptreact"
  },
  "prettier.singleQuote": true,
  "prettier.semi": false,
  "workbench.colorTheme": "One Dark Pro",
  "terminal.integrated.defaultProfile.windows": "Git Bash"
}
```

### Node.js Development Environment

#### Installation & Configuration

```powershell
# Install Node.js LTS
winget install OpenJS.NodeJS.LTS

# Verify installation
node --version
npm --version

# Configure npm
npm config set init-author-name "SamCux"
npm config set init-author-email "your.email@example.com"
npm config set init-license "MIT"

# Install global packages
npm install -g @angular/cli
npm install -g create-react-app
npm install -g typescript
npm install -g ts-node
npm install -g nodemon
npm install -g live-server
```

#### Project Structure Template

```
project-name/
├── src/
│   ├── components/
│   ├── pages/
│   ├── utils/
│   ├── styles/
│   └── index.js
├── public/
├── tests/
├── docs/
├── .gitignore
├── package.json
├── README.md
└── .env.example
```

### Python Development Environment

#### Installation & Setup

```powershell
# Install Python
winget install Python.Python.3.11

# Verify installation
python --version
pip --version

# Create virtual environment template
python -m venv env
env\Scripts\activate

# Essential packages
pip install requests
pip install flask
pip install django
pip install pandas
pip install numpy
pip install jupyter
```

#### Python Project Structure

```
python-project/
├── src/
│   └── main.py
├── tests/
├── docs/
├── requirements.txt
├── .gitignore
├── README.md
└── setup.py
```

### Git Configuration

#### Global Git Setup

```bash
# Set global configuration
git config --global user.name "SamCux"
git config --global user.email "your.email@example.com"
git config --global init.defaultBranch main

# Set up SSH key for GitHub
ssh-keygen -t ed25519 -C "your.email@example.com"
# Add to GitHub: Settings > SSH and GPG keys

# Common aliases
git config --global alias.st status
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.cm commit
```

#### Git Workflow Templates

**Feature Branch Workflow**

```bash
# Start new feature
git checkout -b feature/new-feature

# Work on feature
git add .
git commit -m "Add new feature"

# Push and create PR
git push origin feature/new-feature
```

### Docker Development Environment

#### Installation

```powershell
# Install Docker Desktop
winget install Docker.DockerDesktop
```

#### Essential Docker Commands

```bash
# Build image
docker build -t app-name .

# Run container
docker run -p 3000:3000 app-name

# Docker Compose
docker-compose up -d
docker-compose down
```

#### Dockerfile Templates

**Node.js Application**

```dockerfile
FROM node:18-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["npm", "start"]
```

## 🔨 Development Workflow

### Daily Development Routine

1. **Start the day**

   - Pull latest changes: `git pull origin main`
   - Check for dependency updates
   - Review project board/issues

2. **Feature Development**

   - Create feature branch
   - Write tests first (TDD)
   - Implement feature
   - Run tests and linting

3. **Code Quality**

   - Format code with Prettier
   - Fix ESLint warnings
   - Run type checking
   - Update documentation

4. **End of day**
   - Commit changes with meaningful messages
   - Push to remote branch
   - Update project status

### Project Templates

#### React TypeScript Project

```bash
# Create project
npx create-react-app my-app --template typescript
cd my-app

# Additional dependencies
npm install @types/node @types/react @types/react-dom
npm install tailwindcss autoprefixer postcss
npm install -D eslint-config-prettier prettier
```

#### Node.js Express API

```bash
# Initialize project
mkdir api-project && cd api-project
npm init -y

# Install dependencies
npm install express cors helmet morgan
npm install -D nodemon typescript @types/express @types/node ts-node

# Create basic structure
mkdir src routes middleware controllers models
```

## 📊 Performance Optimization

### Development Machine Optimization

#### System Configuration

- **RAM:** 16GB minimum, 32GB recommended
- **Storage:** SSD for OS and development projects
- **CPU:** Multi-core processor for build processes

#### VS Code Performance

```json
{
  "files.watcherExclude": {
    "**/node_modules/**": true,
    "**/.git/**": true,
    "**/dist/**": true,
    "**/build/**": true
  },
  "search.exclude": {
    "**/node_modules": true,
    "**/dist": true,
    "**/build": true
  }
}
```

### Build Optimization

#### Webpack Configuration

- Code splitting for better performance
- Tree shaking to eliminate dead code
- Proper source maps for debugging

#### Development Server

- Hot module replacement for faster development
- Proxy configuration for API calls
- Environment-specific configurations

## 🧪 Testing Setup

### Testing Frameworks

#### Frontend Testing

- **Jest** - JavaScript testing framework
- **React Testing Library** - React component testing
- **Cypress** - End-to-end testing

#### Backend Testing

- **Jest** - Node.js testing
- **Supertest** - API testing
- **Pytest** - Python testing

### Testing Configuration

```javascript
// jest.config.js
module.exports = {
  testEnvironment: "jsdom",
  setupFilesAfterEnv: ["<rootDir>/src/setupTests.js"],
  moduleNameMapping: {
    "\\.(css|less|scss)$": "identity-obj-proxy",
  },
  collectCoverageFrom: ["src/**/*.{js,jsx,ts,tsx}", "!src/index.js"],
};
```

## 🔒 Security Best Practices

### Environment Variables

- Use `.env` files for configuration
- Never commit sensitive data
- Use different environments (dev, staging, prod)

### Dependency Management

- Regular security audits: `npm audit`
- Keep dependencies updated
- Use lockfiles (`package-lock.json`)

### Code Security

- Input validation and sanitization
- Proper error handling
- Authentication and authorization

## 📱 Mobile Development Setup

### React Native Environment

```bash
# Install React Native CLI
npm install -g react-native-cli

# Create new project
npx react-native init MyApp
cd MyApp

# Run on Android
npx react-native run-android

# Run on iOS (macOS only)
npx react-native run-ios
```

### Android Development

#### Android Studio Configuration

- Install Android SDK
- Configure virtual devices (AVD)
- Set up device debugging

#### Environment Variables

```bash
# Add to .bashrc or .zshrc
export ANDROID_HOME=%LOCALAPPDATA%\Android\Sdk
export PATH=%PATH%;%ANDROID_HOME%\tools;%ANDROID_HOME%\platform-tools
```

## 🎯 Next Steps

After setting up your development environment:

1. **Create a sample project** in your preferred technology stack
2. **Set up continuous integration** with GitHub Actions
3. **Configure deployment pipelines** for your projects
4. **Join developer communities** and contribute to open source
5. **Take screenshots** of your setup for documentation

## 📸 Development Environment Showcase

**📁 Location:** [`../06-Screenshots/development/`](../06-Screenshots/development/)

- `vscode-setup.png` - VS Code with extensions and theme
- `terminal-development.png` - Terminal with development tools
- `project-structure.png` - Example project organization
- `debugging-session.png` - Debugging workflow demonstration

---

**💡 Pro Tip:** Document your development workflow and configurations for easy setup on new machines!
