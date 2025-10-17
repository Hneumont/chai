# Project: Chai (Chat + AI)

This repository contains the source code for the "Chai" command-line AI chat application, developed as part of the DBT230 course.

## Author

**Hector Berumen**

## Lab 1: Flat-File Persistence

This lab focuses on building the foundational persistence layer using a simple flat-file (JSON) system. The goal is to establish a performance baseline for file I/O operations, which will serve as a benchmark for subsequent labs involving more advanced database technologies.

## Questions:
### 1. What are two different designs you contemplated for your multiple conversations implementation?
N/A

### 2. A vibe coder wants to make a quick MVP (minimum viable product) over the weekend that handles chat threads with AI models. Do you recommend using JSON files for persistence? Why?
Considering how the project is a MVP, I would reccomend using JSON files for Persistence; JSON files provide perhaps the easiest to understand balance between human and computer readability, it doesn't take much effort to figure out how data is being stored within a JSON file. Additionally, JSON files tend to be easy to write in/out of, which would help to speed up production and get the MVP out faster.

### 3. You are interviewing at OpenAI. The interviewer asks if you would use raw JSON files to store user chats or if you would use a database or other form of persistence and to explain your choice. How would you reply?
I would not use JSON files, they are bulky, provide little in the way of privacy/security and would cause heavy development debt down the line. Regardless of my opinion, the choice belongs to the project lead, but I would opt for something slightly more efficient like an encrypted BSON to ensure users aren't able to easily leak other chats.

### 4. What did you notice about performance using this file storage method?
N/A
