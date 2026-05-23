# Multithreaded Task Scheduler Simulation Engine

An interactive web-based simulation of CPU scheduling algorithms, modeling concepts from C++ multithreaded programming: thread pools, job queues, mutex synchronization, and parallel task distribution.

## Features

- **FCFS** — First Come, First Served (non-preemptive)
- **Round Robin** — Configurable time quantum (preemptive)
- **Priority Scheduling** — Lower number = higher priority (non-preemptive)
- **Multithreaded simulation** — 1–8 parallel threads
- **Animated Gantt chart** — Real-time task execution visualization
- **Thread pool view** — Live status per thread with progress bars
- **Performance metrics** — Avg waiting time, turnaround, response time, CPU utilization, throughput

## Getting Started

### Prerequisites

- **Node.js** 18+ (download from https://nodejs.org)
- **npm** (included with Node.js)

### Install & Run

```bash
# Install dependencies
npm install

# Start the dev server (opens at http://localhost:3000)
npm run dev
```

### Build for Production

```bash
npm run build
npm run preview
```

## How to Use

1. **Choose an algorithm** — FCFS, RR, or Priority using the toggle buttons
2. **Set threads** — increase/decrease the thread pool size (1–8)
3. **Set quantum** — for Round Robin, configure the time slice
4. **Edit tasks** — modify arrival time, burst time, and priority inline
5. **Add/remove tasks** — use the + and trash buttons in the job queue
6. **Run** — click "Run Simulation" and watch the animated visualization
7. **Adjust speed** — 0.5x, 1x, 2x, or 4x playback

## Project Structure

```
src/
├── lib/
│   └── scheduler.ts        # Core scheduling algorithms (FCFS, RR, Priority)
├── components/
│   ├── GanttChart.tsx      # Animated Gantt chart visualization
│   ├── ThreadPool.tsx      # Thread state cards with live progress
│   ├── TaskTable.tsx       # Editable job queue table
│   ├── MetricsPanel.tsx    # Performance metrics + completion table
│   ├── AlgorithmInfo.tsx   # Algorithm details panel
│   └── ui/                 # shadcn/ui component library
├── pages/
│   └── SimulatorPage.tsx   # Main simulation page
└── App.tsx
```

## Tech Stack

- React 19 + TypeScript
- Vite 6
- Tailwind CSS v4
- shadcn/ui components
- Lucide React icons
- Framer Motion
