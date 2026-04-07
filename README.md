# 🍝 philosophers

> *Eating, thinking, and sleeping—without starving or deadlocking. A deep dive into multithreading at 1337 Coding School.*

## 💡 About The Project

`philosophers` is an algorithmic project based on the classic "Dining Philosophers problem" formulated by Edsger Dijkstra. The objective is to learn the fundamentals of concurrent programming by managing multiple threads and sharing resources safely.

In this simulation, a set number of philosophers sit at a round table. They alternate between three states: eating, thinking, and sleeping. To eat, a philosopher needs two forks (one on their left, one on their right). Because the forks are shared among them, the program must strictly coordinate who gets to hold a fork and when, preventing scenarios where philosophers starve, deadlock each other, or overwrite each other's memory.

> **Note on Timeline:** I completed this project roughly one year ago as I advanced into the concurrent programming branch of the 42 curriculum. I am pushing it to this new GitHub profile to consolidate my projects and highlight my lower-level understanding of system architecture.

## 🧠 Key Concepts Learned

* **Multithreading:** Using the `<pthread.h>` library to create and join multiple execution threads that run simultaneously in the same memory space.
* **Mutexes (Mutual Exclusion):** Protecting shared resources (like the forks and the console output) from being accessed by multiple threads at the exact same time.
* **Data Races & Deadlocks:** Identifying and avoiding situations where the timing of threads causes undefined behavior or permanent freezing.
* **Time Management:** Using `gettimeofday()` and highly optimized `usleep()` loops to ensure philosophers die at the exact millisecond they are supposed to if they fail to eat.

## 🚀 Getting Started

### Prerequisites
* A C compiler (e.g., `gcc` or `clang`)
* `make`
* The `pthread` library (standard on most Unix systems)

