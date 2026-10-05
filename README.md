# AI Workflow Automation Tool

 AI workflow automation tool built with Next.js, React Flow, and OpenAI. Create visual workflows with drag-and-drop nodes, including powerful AI-powered nodes for text generation, content analysis, and more.

## 🚀 Features

### Visual Workflow Builder

- **Drag & Drop Interface** - Intuitive node placement on canvas
- **Node Connections** - Visual data flow between nodes
- **Real-time Execution** - Watch workflows run with animated feedback
- **Node Configuration** - Double-click to configure each node

### Node Types

#### 🔵 Trigger Nodes

- **Webhook Trigger** - Start workflows from HTTP requests
- **Schedule Trigger** - Run workflows on a schedule

#### 🌟 AI Nodes (Powered by OpenAI)

- **AI Text Generator** - Generate text using GPT models
- **AI Content Analyzer** - Analyze sentiment, extract keywords, or summarize
- **AI Chatbot** - Generate conversational responses
- **AI Data Extractor** - Extract structured data from text

#### 🟢 Action Nodes

- **HTTP Request** - Make API calls to external services
- **Data Transform** - Transform data using JavaScript
- **Send Email** - Send emails (simulated)

#### 🟣 Logic Nodes

- **If/Else** - Conditional branching
- **Delay** - Wait for specified time

## 📦 Tech Stack

- **Next.js 14** - React framework with App Router
- **TypeScript** - Type-safe code
- **React Flow** - Visual workflow canvas
- **Zustand** - State management
- **Tailwind CSS** - Styling
- **Azure OpenAI API** - AI functionality
- **Lucide React** - Beautiful icons

## 🛠️ Installation

1. **Clone the repository**

```bash
git clone <your-repo>
cd minimal-n8n
```

2. **Install dependencies**

```bash
npm install
```

3. **Set up environment variables**

```bash
cp .env.local.example .env
```

Edit `.env` and add your Azure OpenAI credentials:

```
AZURE_OPENAI_ENDPOINT="https://<your-resource-name>.openai.azure.com/"
AZURE_OPENAI_DEPLOYMENT_ID="gpt-4o"
AZURE_OPENAI_API_KEY="your_azure_openai_api_key_here"
```

Get your credentials from [Azure Portal](https://portal.azure.com/)

4. **Run the development server**

```bash
npm run dev
```

5. **Open your browser**
   Navigate to [http://localhost:3000](http://localhost:3000)

## 🎯 Usage

### Creating a Workflow

1. **Drag nodes** from the sidebar onto the canvas
2. **Connect nodes** by dragging from one node's output (right) to another's input (left)
3. **Configure nodes** by double-clicking them
4. **Execute** by clicking the "Execute" button in the sidebar

### Example Workflows

#### AI Content Generator

```
Webhook Trigger → AI Text Generator → Send Email
```

Generate blog posts or content on demand

#### Smart Customer Support

```
Webhook Trigger → AI Content Analyzer → If/Else → AI Chatbot
```

Analyze sentiment and route to appropriate response

#### Data Processor

```
Schedule Trigger → HTTP Request → AI Data Extractor → Data Transform
```

Periodically fetch and structure data

## 📁 Project Structure

```
AI-WORKFLOW-AUTOMATION/
├── app/
│   ├── api/
│   │   └── ai/
│   │       └── execute/
│   │           └── route.ts          # AI execution API
│   ├── page.tsx                      # Main workflow canvas
│   ├── layout.tsx                    # Root layout
│   └── globals.css                   # Global styles
├── components/
│   ├── ui/                           # UI components
│   │   ├── button.tsx
│   │   ├── input.tsx
│   │   ├── textarea.tsx
│   │   ├── label.tsx
│   │   └── select.tsx
│   ├── Sidebar.tsx                   # Node library sidebar
│   ├── CustomNode.tsx                # Custom node component
│   └── NodeConfigPanel.tsx           # Node configuration panel
├── lib/
│   ├── types.ts                      # TypeScript types
│   ├── store.ts                      # Zustand store
│   ├── node-definitions.ts           # Node type definitions
│   ├── executor.ts                   # Workflow execution engine
│   └── utils.ts                      # Utility functions
├── SCRIPT.md                         # YouTube tutorial script
└── README.md
```
