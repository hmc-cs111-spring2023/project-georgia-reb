# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

The critique that I received from last week's work was not very helpful, it only
commented on one part of my notebook. The provided suggestion was nice, but I
don't think will be relevant given the way my parser is written.

In our group discussion I asked Kate specifically about how she wrote the rest
of her compiler after writing the parser. While her code was using special parts
of the ANTLR library, listening to her talk about the process made me less
intimidated to work on the rest of my compiler.

Therefore, none of the feedback this week is changing any of my decisions, it is
just motivating me to continue working.

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

This week began in class on Monday, when I asked Kate and Prof Ben for advice on
completing my compiler. I spoke specifically to Prof Ben about implementation
techniques, telling him about my idea to use classes. He agreed with me, and
helped me brainstorm a scenario in which each class produces a LaTeX section
and the compiler is responsible for calling the objects and methods properly.
He explained that my current parser output is what is called a syntax structure.

I liked this idea a lot, and started coding! On Monday afternoon, I worked for
a long time and was able to get a very simple version of my language working!
I implemented the compiler using a Compiler, Sections and GlobalRules class,
where the Compiler class is the overall one which creates Section and GlobalRules
objects. The user can run the Compiler method produceLaTeX to create a LaTeX
file output, or they can run producePDF to create a PDF output (it also currently
creates a LaTeX output too) by creating a LaTeX file and converting it to a PDF.

While coding, I made sure to add comments and build in error messages. For example,
I raise errors if required arguments are missing, or if an invalid argument is
given.

I focused on creating the title page first, using the LaTeX [titlepage](https://www.overleaf.com/learn/latex/How_to_Write_a_Thesis_in_LaTeX_(Part_5)%3A_Customising_Your_Title_Page_and_Abstract).
I was able to include a title, author, image and a hyperlink. I also added in
the bare bones of the project details section implementation.

I also worked on global rules, adding the global rule to create page numbers
in the document. I need to come up with more global rules to add later on! I 
am thinking I could change the font, base size of the text, and maybe text and
background colors? I need to see what I am allowed to customize in LaTeX first!

I then went back and implemented importing files. Essentially, my code creates
a new object while passing in the file to write to and writes LaTeX to that
file without the headers. This ended up working well with suprisingly few bugs.

Then, on Tuesday morning I began working on my documentation. I was in a place
where I was feeling super excited about my code, but also knew that I need to
do a lot more implementation. Looking at it all in VSCode gets overwhelming, so
I decided that if I wrote out my rules in the documentation, it would be easier
to make decisions about what to work on next. I asked Prof Ben on discord what
to use for my documentation, and he suggested using the wiki on GitHub, which I
did. I build out the structure of the [wiki](https://github.com/hmc-cs111-spring2023/artifact-georgia-reb/wiki), and started adding details about how to use the
language.

Then, before and in class on Wednesday, I completed further implementation. I
added more robustness to the title page and made significant progress on the
project details section. I even did the basic implementation of a function! I
also was able to clean up the way that my parser read in strings to simplify the
compilation process. While I was coding, I used the wiki to brainstorm first,
implement, and then make a final confirmation in the wiki once I was done
implementing something.

At this moment, I am planning on continuing to speed through the basic aspects
of this language. In order to finish, I need to finish implementing the abbreviations
of the project details page, create the pattern section implementation, and
the assembly section. The biggest challenge I expect to face here is deciding
how I am going to do list numbers for the pattern section. In crochet you want
to have lists where the list number can either be one value or a range (1 and
1-5 are acceptable). I also want to add more functions, like the code that
automatically generates the instructions for common crochet steps (like a magic
ring). I will also need to go back and fill in some parts of the code that are
empty right now or have TODO comments next to them. And, I will continue to
update my documentation as I go along. Then, at the end I will also need to
figure out how to package my code for a user to run the compiler most easily.

IF I am able to do all of that, then I might go back and add more fancy functions,
but that will all depend on how much time I have!

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I need to just keep on going and finish the parts of a fully functioning
implementation descibed just above.

**What questions do you have for your critique partners? How can they best help
you?**

I want to know what they think about the language is coming along, do they think
it is useable? I also want to hear their thoughts about how to package the
compiler to be most useable to new users.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

I have spent both classes on this project, and 7+ hours of working outside of
that.

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

I think this week has gone great! I have a great implementation of the entire
language overall, as well as the title page and most of the project details
section. So, I have two more sections to go! I think that I will be able to
finish all the necessities next week, leaving me with time to clean up the project,
do a video, and maybe do a few extra fun functions.
