# Mission Reflection

## 1. Why is automation critical when managing hundreds of cloud servers?
Doing tasks by hand on hundreds of servers would be slow, inconsistent, and
full of human error. Automation lets one script do the same job everywhere,
the same way, every time. It also keeps running when nobody is online, like
a nightly backup at 2:00 AM.

## 2. What are the potential dangers of automation?
Automation repeats mistakes as fast as it repeats good work. If a script has a
destructive typo, such as a wrong path in a delete command, and it is
scheduled on 1,000 servers, it could wipe out data everywhere before anyone
notices. That is why scripts should be tested on a small sample first,
reviewed by another person, and protected by backups.

## 3. How did writing a Bash script differ from a Docker Compose YAML file?
A Bash script is a step-by-step list of commands that tells the system
exactly how to do something, in order. A Docker Compose YAML file is
declarative: it describes the end result I want, such as which containers,
ports, and networks, and Docker works out the steps. Bash is more flexible,
while YAML is simpler and more predictable.

## 4. How has my understanding of Cloud Computing transformed?
At the start of the semester, I [describe how you saw cloud computing in
Laboratory 1, e.g. "thought of it as just renting someone else's computer"].
Over the labs I moved from running single commands to building, packaging,
and now automating systems. I now see cloud computing as many small tools
that work together, and automation is what makes them manageable at scale.
[Mention one specific lab that changed your thinking.]

## 5. Which role did I enjoy most, and why?
I enjoyed the [Infrastructure Engineer / Cloud-Native Engineer / Security
Engineer / Cloud Automation Engineer] role the most because [give your real
reason, e.g. "seeing my script work on its own felt rewarding" or "I liked
solving problems step by step"]. [Add one sentence about a moment in that
lab that stood out.]
