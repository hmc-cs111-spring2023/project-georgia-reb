# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

This past week we were introducted to our critique groups. We shared our project
ideas and then went through the questions provided for us. Within our group
we found some aspects of our project to be in common. We are all creating
external DLSs, and we all plan to use pre-existing libraries in our work. Additionally,
none of us had made a decision on our host language when we met. Regarding our
project ideas, all three of us are working with domains we have prior experience
with, and Kate and Ryder are also both going to be working with visualizations.

In our discussion, we talked about our evaluation and timeline plans. We all
had similar goals for our evaluation, and contributed to each other's goals.
I suggested adding documentation, and Kate and Ryder discussed having other
people also be excited our final results. For our timeline, we all have different
details in goals for next week, but all are hoping to have made decisions about
host languages.

Ryder did not leave me addition feedback this week, so I do not have further
feedback on my project idea to reflect on, so I can't answer the questions
written above.

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
and come to class on Wednesday ready to discuss my syntax with Prof Ben.
Original sample program: https://github.com/hmc-cs111-spring2023/artifact-georgia-reb/tree/main/Example%20Try%201

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
prospect and think that using ideas from JSON will provide a through structure to my code.
New sample program: https://github.com/hmc-cs111-spring2023/artifact-georgia-reb/tree/main/Example%20Try%202

### Starting to code.
Since I was able to finish my original goals by the end of class on Wednesday, I have added an additional
goal to get started on my goals for next week. I have started to plan what my parser and
compiler are going to do. To do this, I looked at my notes from this course
and CS131, written out general information about what parsers and compilers
should do, and matched up my project idea with these guidelines.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

My most pressing issue at the moment is deciding if I should code the parser
or the compiler first. It seems like I could start with either of them, but I
want to figure out which one will make the process of working on the project
an easier experience.

I think further pressing issues will appear
as I being to code. The questions that I expect to appear will have to do
with my syntax choices as I am expecting to have to change the syntax a little
bit to make the parsing work properly.

**What questions do you have for your critique partners? How can they best help
you?**

Are they going to write the compiler or the parser first? I need to get started
with one, and I am not sure which is better to start with, but I am thinking
the parser?

I might also want to show them my example program and see what they think. I
would love to hear other people's thought on if the program is intuitive or not.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

I spent 2.5 hours after class on Monday working on example programs, and I spent
all of class on Wednesday as well as 1.5 hours afterwards re-creating new
example programs and starting to think about the parser and compiler. I also
have spent probably another hour working on this notebook reflection.

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

This week went great! I did more than exepcted as I have started to work on
the parser and compiler planning. I feel well prepaired for next week.
