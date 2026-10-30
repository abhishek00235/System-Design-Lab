# Systemcraft

Systemcraft is an interactive system design learning studio for building skills from first principles through interview and implementation practice. Learn a concept, sketch the architecture, then explore how it responds to traffic and bottlenecks.

## Get started

There is no build step or dependency installation. Open `index.html` in a modern browser, or serve the directory locally:

```bash
npx serve .
```

Then open the local URL printed by the server. The app is client-side; progress, preferences, and saved designs are stored in that browser with `localStorage`.

## Learning studio

- **Overview:** Resume your learning path and see your progress.
- **Learning path:** Eight stages with 40+ focused system design topics, short lessons, and knowledge checks. Topics span foundations, APIs, storage, caching, scaling, distributed systems, reliability, security, data platforms, and specialized architectures.
- **Interview gym:** Practice 30+ architecture scenarios. Clarify requirements, record assumptions, choose first-draft components, use the timer, and review your answer against a rubric.
- **Implementation lab:** Work through JavaScript exercises for a token bucket rate limiter, a TTL cache, and retry with backoff. Compare your approach with a reference implementation.
- **System design playground:** Build and explore architectures in a large, full-screen canvas.

## Playground

The playground includes a searchable palette of architecture components, plus support for custom components. Place and arrange nodes, connect flows, set a traffic source and request load, and inspect estimated throughput and bottlenecks. Save multiple designs locally or export one to JSON.

Controls include:

- Drag palette items onto the canvas or click to place them.
- Connect components from their output ports; use flow junctions to branch or join paths.
- Right-click a component for actions such as inspect, connect, set traffic source, add a replica, duplicate, disconnect, or delete.
- Adjust instance counts, component capacity, request load, and payload size.
- Collapse palette, inspector, or simulator panels to make room; use full-screen mode for the canvas.
- Switch between light and dark workspace themes.

## Project structure

```text
system-design-lab/
|-- index.html          # App entry point
|-- README.md
`-- src/
    |-- app.js           # Lessons, practice flows, playground logic, local state
    |-- styles.css       # Shared application styles
    `-- playground.css   # Expanded canvas and full-screen workspace styles
```

## Data and limitations

The app does not require an account or backend. Lesson progress, workspace theme, exercise drafts, and saved architectures remain in the current browser profile. Export a design to JSON if you want to keep or share a separate copy.

The playground is an educational model, not a production capacity planner. It evenly distributes traffic across outgoing connections and estimates queueing delay from utilization. Component capacity and latency are editable assumptions; actual performance depends on workload, implementation, and measurement. The implementation lab provides a lightweight keyword-based review and reference code; it does not execute or prove the correctness of your draft.

The interface uses Google Fonts when online and falls back to system fonts when offline.
