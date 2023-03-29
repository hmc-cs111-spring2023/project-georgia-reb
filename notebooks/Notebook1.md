# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

After class on Monday, I decided that my goals for the week were to provide feedback to Kate,
create an example program, and decide what language to use as my host language for the project.

Note, I had already decided last week that I am going to write an external DSL when working
on my project proposal. I want to create a new language that is very targeted towards
people writing crochet patterns, and I want full control over how this is converted to different
outputs like markdown and PDFs. I am also excited by the idea of creating my own syntax from
scratch.

### Host language decision:
On Monday afternoon, I spent some time research the pros and cons of using Haskell and Python
for this project. These are the only two languages I considered.

The pros of Haskell include
that it is create for abstract syntax types, and it has the Pandoc library for converting
markdown files to a range of other document types. I also enjoy working with this language in
CS131 and am currently quite comfortable with using it. The cons are that it won't have as
many packages avalible as Python, and it is more difficult to debug than Python.

The pros of Python include that it is very easy to write code in, easy to debug, and has a
large amount of avalible packages. The cons are that I haven't yet worked with Python in a
programming languages class (only Haskell and Scala), but I think that this won't be too
much of a challenge.

These pros and cons are both ideas that I thought about on my own, and discussed with Prof Ben
during class on Wednesday. Based on these pros and cons, I have decided to write my language
in Python.

### Example program:
After class on Monday, I spent some time writing an example program. I wanted to create an
example program that included the range of different implementation possibilities that I want
to allow in my language. While working on this example program, I struggled a bit to decide
how to create consistent and logical syntax for my program. I decided to stop after a little bit,
and come to class on Wednesday ready to discuss my syntax with Prof Ben. *add a link to my
original sample program*.

In class on Wednesday, I discussed my syntax with Prof Ben. I started by question by explaining
that if my syntax is going to look like a different programming language, I want it to be very
logical so that someon with no knowledge could use it, and so that someone with prior knowledge
of the similar language wouldn't be confused. I also expressed by concern that if it is too
similar to an existing language it will be difficult for knowledgeble users to remember what is
the same and what is different to the orignial language. In this conversation we defined my user
to be someone who has crochet experience, but has either limited or minimal experience with programming
and languages like HTML and markdown.

Coming out of this discussion, Prof Ben inspired two ideas that I have since decided to implement.
The first is changing my code to require multiple files instead of just one. Now, a default project
will contain a header file that states which files contain the code for each part of the crochet pattern. 
Then, each file will be one section of the crochet pattern. What I am most excited about is that I can
create default files for each type of section, that way a lot of the syntax can be pre-written for
the user, and they can just fill in their information. Then if they want to make additional changes
they can read the documentation to know additional options available to them.
The second idea is to format my code in a JSON like format. I hadn't thought about this explicitly
(even though my original example program does look very JSONy), but I now feel inspired by this
prospect and think that using ideas from JSON will provide a through structure to my code. *add
a link to my new sample program*

### Starting to code.
Since I was able to finish my original goals by the end of class on Wednesday, I have added an additional
goal to get started on my goals for next week. I have decided to start planning what my parser and
compiler are going to do, and then if I am ambition start coding.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

**What questions do you have for your critique partners? How can they best help
you?**

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**
