# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [April 1, 2026, 2:30 PM]
**What I did**: Forked the repository and set up my student ID

**Details**: 
- Created GitHub account with university email
- Forked the starter repository
- Changed student ID on line 92 to my actual ID (441234567)
- Compiled and ran the program successfully

**Challenges**: Had to install JDK first because javac wasn't recognized

**Solution**: Downloaded JDK 17 from Oracle website and set PATH variable

**Time spent**: 30 minutes

---

## Your Development Log:

### Entry 1 - [Mar 26, 2026, 1:30 PM]
**What I did**: 
Created the GitHub repository and set up the project.
**Details**: 
• Forked the starter repository for OS-Assignment1.
• Cloned the project to my local VS Code environment.
• Configured my GitHub account with the university email.
• Verified that Java and JDK are properly installed.
**Challenges**: 
 The javac command was not working in the terminal.
**Solution**: 
Added the JDK path to the system environment variables.
**Time spent**: 
45 minutes
---

### Entry 2 - [Mar 26, 2026, 4:00 PM]
**What I did**: 
 Feature 1: Added the priority field and implemented random priority generation.
**Details**: 
• Added priority field(1-5)
• generated random priority
• displeyed priority
**Challenges**: 
The code was generating priority values that were too high or zero, which didn't match the required priority range (1 to 5).
**Solution**: 
Used the nextInt(5) + 1 method from the Random class to strictly limit the priority levels to a valid range.
**Time spent**: 
1.5 hours
---

### Entry 3 - [Mar 27, 2026, 10:00 AM]
**What I did**: 
 Feature 2 :Added the Context Switch Counter.
**Details**: 
• Created a variable to count the switches.
• Made the counter increase every time a process starts.
• Printed the total number of switches at the end of the program.
**Challenges**: 
Deciding where exactly to increase the counter in the code.
**Solution**: 
Put the increment line right after the process is taken from the queue (polling).
**Time spent**: 
2 hours
---

### Entry 4 - [Mar 28, 2026, 11:00 AM]
**What I did**: 
Feature 3 : Waiting time calculation
**Details**: 
• Added new variables to track when each process was created.
• Used System.currentTimeMillis() to measure the time difference.
•printed the final waiting time results
**Challenges**: 
Figuring out how to correctly subtract the start time from the end time.
**Solution**: 
Applied a simple formula to calculate the delay for each process before it finished.
**Time spent**: 
1 hour
---

### Entry 5 - [[Mar 28, 2026, 12:10 PM]
**What I did**: 
Final testing and completing the documentation.
**Details**: 
• Ran the simulation multiple times to ensure all outputs are consistent.
• Finished all the required answers in the documentation file.
• Verified that the final results match the project requirements.
**Challenges**: 
Organizing the answers to be clear and easy to follow.
**Solution**: 
Re-structured the document sections to match the simulation flow.
**Time spent**: 
2.5 hours
---

### Entry 6 - [Optional - Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

## Summary

**Total time spent on assignment**: [3 days]

**Most challenging part**: 
Understanding the CPU scheduling logic and making sure the context switches are calculated correctly.
**Most interesting learning**: 
How Round Robin gives every process a fair turn to run.
**What I would do differently next time**: 
Improve the code structure from the beginning to make it easier to test.
