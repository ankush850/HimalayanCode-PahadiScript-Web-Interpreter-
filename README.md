# 🏔️ HimalayanCode: PahadiScript Web Interpreter

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://python.org)
[![Flask](https://img.shields.io/badge/Flask-2.0%2B-green)](https://flask.palletsprojects.com/)
[![SQLite](https://img.shields.io/badge/SQLite-3.0%2B-yellow)](https://sqlite.org)
[![PLY](https://img.shields.io/badge/PLY-3.11-orange)](https://www.dabeaz.com/ply/)
[![Version](https://img.shields.io/badge/version-1.0.0-blue)](https://github.com/yourusername/HimalayanCode/releases)
[![HimalayanCode](https://img.shields.io/badge/HimalayanCode-PahadiScript_Web_Interpreter-2ea44f)](https://github.com/yourusername/HimalayanCode)
[![Web Ready](https://img.shields.io/badge/Web-Ready-orange)](https://yourusername.github.io/HimalayanCode/)

A web-based interpreter for the PahadiScript programming language, inspired by Himalayan coding traditions.

> **Code in the language of the mountains** - A complete web-based interpreter for PahadiScript, a Himalayan-inspired programming language.

##  Features

###  Core Interpreter
- **Lexical Analysis**: PLY-based lexer recognizing 20+ PahadiScript keywords
- **Syntax Parsing**: Complete CFG implementation with error recovery
- **Symbol Table**: Dynamic variable tracking with scope management
- **Code Execution**: Virtual machine for PahadiScript bytecode execution

###  User Experience
- **Web-based IDE**: Full-featured code editor with syntax highlighting
- **Real-time Execution**: Instant code compilation and execution
- **Program Management**: Save, load, and organize PahadiScript programs
- **Version Control**: Track changes and restore previous versions

###  Community Features
- **Program Sharing**: Generate shareable URLs and QR codes
- **Public Gallery**: Browse and fork community programs
- **Social Engagement**: Like, comment, and rate programs
- **Leaderboard**: Weekly challenges and user rankings

###  Analytics Dashboard
- **Personal Statistics**: Track your learning progress
- **Error Analysis**: Identify common programming mistakes
- **Performance Metrics**: Execution time and memory usage
- **Export Capabilities**: Download your code and data

###  Modern Interface
- **Responsive Design**: Works on desktop, tablet, and mobile
- **Theme Support**: Light, dark, and mountain themes
- **Accessibility**: Screen reader support and keyboard navigation
- **Multi-language**: Support for English and Himalayan languages

## System Architecture
```mermaid
flowchart TD
    Client[Client Layer] --> Presentation[ Presentation Layer]
    Presentation --> Application[Application Layer]
    Application --> Service[ Service Layer]
    Service --> Data[ Data Access Layer]
    Data --> Storage[ Storage Layer]
    
    classDef default fill:#000000,stroke:#ffffff
```

##  Detail Architecture Diagram

```mermaid
graph TD
    User([User])
    Browser[ Browser<br/>Web Interface]
    Flask[ Flask Server<br/>Python Backend]
    Interpreter[PahadiScript Interpreter]
    Lexer[ Lexer<br/>Token Reader]
    Parser[ Parser<br/>Grammar Rules]
    Eval[ Evaluator<br/>_evaluate function]
    SymbolTable[ Symbol Table<br/>Variable Memory]
    
    User --> Browser
    Browser -->|HTTP Request| Flask
    Flask -->|Code String| Interpreter
    
    Interpreter --> Lexer
    Interpreter --> Parser
    Interpreter --> Eval
    Interpreter --> SymbolTable
    
    Lexer -->|Tokens| Parser
    Parser -->|AST| Eval
    Eval -->|Read/Write| SymbolTable
    Eval -->|Results| Flask
    Flask -->|HTTP Response| Browser
    Browser -->|Display| User
```
## Data Flow 

```mermaid
flowchart TD
    Dashboard[Dashboard<br>Type PahadiScript code]
    Lexer[ Lexer<br>Tokenizes code]
    Interpreter[ INTERPRETER<br>Parses & Executes Immediately]
    Memory[ Symbol Table<br>Variable storage]
    Output[ Output Collector]
    Console[ Console Display]

    Dashboard -- "1. Code" --> Lexer
    Lexer -- "2. Tokens" --> Interpreter
    Interpreter -- "3a. Store/Get values" --> Memory
    Memory -- "3b. Variable data" --> Interpreter
    Interpreter -- "4. Execute & Get results" --> Output
    Output -- "5. Final output" --> Console
    Console -- "6. Show results" --> Dashboard
```


