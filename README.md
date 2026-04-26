---
title: "RTOS Programming - Collaboration Guide"
description: "Contributing guide for RTOS Programming course content"
tableOfContents: true
sidebar:
  order: 999
---

# RTOS Programming

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Contributors Welcome](https://img.shields.io/badge/contributors-welcome-orange)

**Read this course at:** [https://siliconwit.com/education/rtos-programming/](https://siliconwit.com/education/rtos-programming/)

A course on real-time operating systems covering scheduling, synchronization, and memory management. You will work through FreeRTOS fundamentals and finish with an introduction to Zephyr RTOS.

## Lessons

| # | Title |
|---|-------|
| 1 | Real-Time Systems Concepts |
| 2 | Tasks Scheduling and Context Switching |
| 3 | Queues and Inter-Task Communication |
| 4 | Semaphores Mutexes and Synchronization |
| 5 | Memory Management and Safety |
| 6 | Software Timers and Interrupt Management |
| 7 | Debugging and Profiling RTOS Applications |
| 8 | Zephyr RTOS Introduction |

## File Structure

```
rtos-programming/
├── lesson-0.mdx        # Course introduction
├── lesson-1.mdx        # Real-Time Systems Concepts
├── lesson-2.mdx        # Tasks Scheduling and Context Switching
├── lesson-3.mdx        # Queues and Inter-Task Communication
├── lesson-4.mdx        # Semaphores Mutexes and Synchronization
├── lesson-5.mdx        # Memory Management and Safety
├── lesson-6.mdx        # Software Timers and Interrupt Management
├── lesson-7.mdx        # Debugging and Profiling RTOS Applications
├── lesson-8.mdx        # Zephyr RTOS Introduction
└── README.md
```

## How to Contribute

All commands below work on Linux, macOS, and Windows (using Git Bash, PowerShell, or Command Prompt with Git installed).

### For Team Members (with push access)

**First time setup (clone the repo once):**

```bash
git clone https://github.com/SiliconWit/rtos-programming.git
cd rtos-programming
```

**Every time you start working:**

```bash
git pull origin main
```

Always pull before making changes. This avoids conflicts with other contributors.

**After making your changes:**

```bash
git add .
git commit -m "Brief description of what you changed"
git push origin main
```

**If you get a push error** (someone pushed before you):

```bash
git pull origin main
```

Git will merge the changes automatically in most cases. If there is a conflict, Git will mark the conflicting lines in the file. Open the file, choose which version to keep, then:

```bash
git add .
git commit -m "Resolve merge conflict"
git push origin main
```

**Tips to avoid conflicts:**

- Always `git pull origin main` before you start working
- Push your changes as soon as you are done, do not hold onto uncommitted work for long
- Coordinate with other contributors so two people are not editing the same file at the same time

### For External Contributors (without push access)

1. Fork the repository: [SiliconWit/rtos-programming](https://github.com/SiliconWit/rtos-programming)
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/rtos-programming.git
   cd rtos-programming
   ```
3. Make your changes and commit:
   ```bash
   git add .
   git commit -m "Brief description of what you changed"
   git push origin main
   ```
4. Open a Pull Request against `main` on the original repository
5. Describe what you changed and why in the PR description

## Content Standards

- All lesson files use `.mdx` format
- Do not use `<BionicText>` in this course
- Code blocks should include a title attribute:
  ````mdx
  ```c title="task_example.c"
  xTaskCreate(vTaskFunction, "Task1", 128, NULL, 1, NULL);
  ```
  ````
- Use Starlight components (`<Tabs>`, `<TabItem>`, `<Steps>`, `<Card>`) where appropriate
- Keep paragraphs concise and focused on practical application
- Include working code examples that readers can run directly

## Local Development

Clone the main site repository and initialize submodules:

```bash
git clone --recurse-submodules <main-repo-url>
cd siliconwit-com
npm install
npm run dev
```

To test a production build:

```bash
npm run build
```

## License

This course content is released under the [MIT License](LICENSE).
