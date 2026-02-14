# Octave Tutor — Web-Based Code Execution Visualizer

A web-based debugging and execution visualizer for GNU Octave / MATLAB-style code.

Inspired by Python Tutor, this project provides:

- Line-by-line execution stepping
- Breakpoints (clickable gutter)
- Call stack visualization
- Frame switching (dbup/dbdown)
- Workspace inspection per frame
- Console output tracking
- Plot snapshots per execution step
- Monaco-based modern code editor
- Dockerized backend with Octave runtime

---

## Tech Stack

Frontend:
- React + Vite
- Monaco Editor
- Modern UI

Backend:
- FastAPI
- GNU Octave (debug mode)
- Docker containerized execution

---

## How It Works

The backend launches Octave in interactive debug mode.
Each step captures:
- Current execution line
- Call stack (dbstack)
- Workspace variables (whos + eval)
- Plot images (saved as PNG and encoded base64)
- Console output (via diary)

The frontend replays these steps similar to Python Tutor.

---

## Run Locally

```bash
docker compose up --build
