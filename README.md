# Professor-Office-Hours-Simulator
# Overview
This project simulates a professor’s shared office hours and explores challenges in parallel programming using threads and synchronization in C. I built it as a fun and practical way to improve my understanding of race conditions, fairness policies, and deadlock avoidance.

The scenario? A professor teaching two classes (Class A and Class B) opens his door to students—but with rules. Think of it as building a little real-time system where access control, fairness, and exhaustion management all collide.

# 🧠 Why I Built This
I wanted to sharpen my skills in multithreaded programming and dive into real-world synchronization problems. Instead of textbook exercises, I thought it’d be more fun to simulate a quirky professor's office and explore:

How to control shared access with semaphores and mutexes

How to prevent deadlocks while preserving progress

How to fairly schedule competing student groups

How to manage a system where resources (in this case, energy and office chairs) are limited

# 💡 Key Features
Limited Capacity: Only 3 students allowed in the office at a time.

Class Mutual Exclusion: Students from Class A and B can’t mix during a session.

Fairness Rule: After helping 5 students from the same class, the professor must help one from the other class (if available).

Professor Break Time: The professor takes a break after every 10 students.

Progress Without Starvation: Ensures no student waits unnecessarily when it's safe to enter.

# 🔧 Tech Stack
C (GCC)

POSIX Threads (pthreads)

Mutexes and Semaphores for synchronization

# 🔍 What I Learned
Designing thread-safe access policies

Handling thread scheduling and fairness constraints

Debugging race conditions

Structuring readable and maintainable concurrent C code

# 🛠️ How to Run

gcc officehours.c -o officehours -lpthread
./officehours
