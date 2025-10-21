# Project: Chai (Chat + AI)

This repository contains the source code for the "Chai" command-line AI chat application, developed as part of the DBT230 course.

## Author

**Hector Berumen**

## Lab 1: Flat-File Persistence

This lab focuses on building the foundational persistence layer using a simple flat-file (JSON) system. The goal is to establish a performance baseline for file I/O operations, which will serve as a benchmark for subsequent labs involving more advanced database technologies.

## Questions:

### Question 1: Performance test:

- How append times changed as the number of messages gew for flat files vs MongoDB?
  - N/A
- The difference in read times for retrieving the full conversation?
  - N/A

### Question 2: Atomic Operations:

-In MongoDBManager, we use the $push operater in append_message(). Research what "atomic operations" means in the context of databases. Why is this important for a chat application where multiple messages might be added rapidly?
  - Atomic Operations in databases mean that operations are completed either all at once or not completed at all;
  When dealing with multiple rapidly adding messages, this is important as you want to be able to see all messages both from the chat bot and from the user.

### Question 3: Scalability:

Imagine your chat application goes viral and now has 1 million users, each with an average of 10 convesation threads containing 500 mesages each.

Compare how FlatFileManager and MongoDBManager would handle:

- Finding all threads for a specific user
  - N/A
- Loading a specific conversation
  - N/A
- Storage organization and file system limits
  - N/A

### Question 4: Data Modeling Design Challenge:

Currently, each conversation is stored as a single document wiht an embedded array of messages:

An Alternative design would be to store each **message** as its own document;

Describe:
- One advantage of the embedded messages design (what we currently use)
  - TBD
- One advantage of the seperate message documents design
  - TBD
- A scenario where you would choose the seperate messages design instead
  - TBD
*(This is a real design decision MongoDB developers face. There's no single "right" answer because it depends on your access patterns and scale.)*
