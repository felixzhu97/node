# Node.js TOGAF Enterprise Architecture Diagrams

This directory contains TOGAF (The Open Group Architecture Framework) enterprise architecture diagrams for Node.js in PlantUML format.

## Directory Structure

```
doc/togaf/
├── README.md              # Chinese README
├── README-en.md          # English README
├── zh/                   # Chinese version diagrams
│   ├── business-architecture.puml
│   ├── application-architecture.puml
│   ├── data-architecture.puml
│   └── technology-architecture.puml
└── en/                   # English version diagrams
    ├── business-architecture-en.puml
    ├── application-architecture-en.puml
    ├── data-architecture-en.puml
    └── technology-architecture-en.puml
```

## Architecture Diagram Overview

### 1. Business Architecture

**File Locations:**
- Chinese: `zh/business-architecture.puml`
- English: `en/business-architecture-en.puml`

**Overview:**
- **Business Capability Layer**: JavaScript runtime service, package management ecosystem, developer community support, cross-platform support capability
- **Business Process Layer**: Application development process, package publishing process, issue handling process, release process
- **Business Role Layer**: Developers, maintainers, TSC technical committee, collaborators, triagers, release team
- **Business Value Layer**: Cross-platform JavaScript execution, ecosystem support, long-term support guarantee, open governance model

### 2. Application Architecture

**File Locations:**
- Chinese: `zh/application-architecture.puml`
- English: `en/application-architecture-en.puml`

**Overview:**
- **Application Interface Layer**: HTTP/HTTPS, file system, crypto, stream processing, network, process management modules
- **Core Application Layer**: Module system (CommonJS/ESM), event system, async hooks, buffer management
- **Application Service Layer**: DNS, TLS/SSL, child process management, REPL, debugger, performance monitoring, test framework
- **Application Integration Layer**: N-API interface, native addons, Web API compatibility, WASI support

### 3. Data Architecture

**File Locations:**
- Chinese: `zh/data-architecture.puml`
- English: `en/data-architecture-en.puml`

**Overview:**
- **Data Source Layer**: JavaScript source code, C++ binding code, configuration files, package metadata
- **Data Entity Layer**: Code data, configuration data, runtime data, metadata
- **Data Flow Layer**: Module loading flow, data serialization, stream processing pipeline, data transformation
- **Data Storage Layer**: File system, memory management, cache mechanism, snapshot storage

### 4. Technology Architecture

**File Locations:**
- Chinese: `zh/technology-architecture.puml`
- English: `en/technology-architecture-en.puml`

**Overview:**
- **Application Technology Layer**: Node.js core, JavaScript API, built-in modules
- **Runtime Technology Layer**: V8 JavaScript engine, libuv event loop, N-API binding layer
- **System Technology Layer**: Operating system interfaces (Linux/Windows/macOS), network protocol stack, file system interface
- **Infrastructure Layer**: Build systems (GYP/GN/CMake), test framework, CI/CD system
- **Technology Standard Layer**: ECMAScript, HTTP, TLS, Web standards

## How to Use

### Rendering PlantUML Diagrams

These `.puml` files can be rendered as images using various methods:

#### Method 1: Using PlantUML Online Server

1. Visit the [PlantUML Online Server](http://www.plantuml.com/plantuml/uml/)
2. Copy the content of a `.puml` file
3. Paste it into the editor
4. Click "Submit" to generate the diagram

#### Method 2: Using Local PlantUML Tools

**Install PlantUML:**

```bash
# Install using npm
npm install -g node-plantuml

# Or using Java (requires Java installed)
# Download plantuml.jar
wget http://sourceforge.net/projects/plantuml/files/plantuml.jar/download -O plantuml.jar
```

**Render Diagrams:**

```bash
# Using node-plantuml
puml generate en/business-architecture-en.puml -o output.png

# Or using Java
java -jar plantuml.jar en/business-architecture-en.puml
```

#### Method 3: Using VS Code Extension

1. Install the "PlantUML" extension in VS Code
2. Open a `.puml` file
3. Press `Alt+D` (Windows/Linux) or `Option+D` (macOS) to preview the diagram
4. Right-click on the diagram to export as PNG, SVG, etc.

#### Method 4: Using IntelliJ IDEA / WebStorm

1. Install the PlantUML plugin
2. Open a `.puml` file
3. Right-click and select "PlantUML" -> "Preview Diagram"
4. Export to various formats

### Editing Architecture Diagrams

All diagrams use standard PlantUML syntax and can be edited directly by modifying the `.puml` files.

**Main Syntax Elements:**
- `package`: Define a package/layer
- `[Component Name] as Alias`: Define a component
- `-->`: Define relationships between components
- `note right of Component`: Add explanatory notes

## Architecture Diagram Relationships

These four diagrams follow TOGAF's four core architecture domains:

```
Business Architecture → Application Architecture → Data Architecture → Technology Architecture
        ↓                      ↓                      ↓                      ↓
   Business Needs         Application          Data Entities        Technical
                          Components                                  Implementation
```

- **Business Architecture** defines business capabilities and values
- **Application Architecture** defines application components and interactions
- **Data Architecture** defines data entities and flows
- **Technology Architecture** defines technical components and standards

## Update Notes

These diagrams are based on the actual structure of the Node.js project (`src/`, `lib/`, `deps/` directories) and reflect the core architectural design of Node.js.

To update the diagrams to reflect new Node.js features or architectural changes:
1. Edit the corresponding `.puml` files
2. Keep Chinese and English versions synchronized
3. Update relevant descriptions in this README

## Reference Resources

- [TOGAF Official Documentation](https://www.opengroup.org/togaf)
- [PlantUML Official Documentation](https://plantuml.com/)
- [Node.js Official Documentation](https://nodejs.org/docs/)

## Contributing

Pull Requests to improve these architecture diagrams are welcome. Before submitting, please ensure:
- Chinese and English versions remain synchronized
- PlantUML syntax is correct
- Diagram content accurately reflects Node.js's actual architecture

