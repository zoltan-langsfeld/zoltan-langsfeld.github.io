---
layout: post
title:  "Why does writing good documentation matter?"
date:   2023-11-20 15:36:55 +0200
---
## Motivation

When I joined idealo in 2019, my first task was to set up my team's project on my local computer. I followed the instructions in the readme file, but the application did not start. I was unsurprised as I had a similar situation on most projects I had worked on before. Finally, I had to turn to my peers for help. After a few hours, the application was eventually running on my local machine. This example was one of the first signs that our documentation needed to become more reliable. 

As time passed, I wanted to understand why the team made certain decisions, e.g., why they picked a specific framework or library. Finding answers to these questions was difficult as, in most cases, the information was not easily accessible. In some cases, the answers to my questions were buried in our commit or chat history. In some others, the answers only existed in my team member's memory. 

Questions from our stakeholders and new team members also had to be answered, and due to the lack of trustworthy documentation, it involved a lot of labor. We ran the numbers and realized that if we multiply the time it takes to answer all these questions by the number of times people asked them, we can quickly lose days, if not weeks, in a year. On top of that, some of our answers were not accurate, as we didn't always have the time to gain a complete understanding of the topic.

As an engineering team, we had to understand that we're not only responsible for fulfilling the functional and non-functional requirements but also for documenting our work accurately.
* We're responsible for making our team as productive as possible. We only maximize productivity if we spend less time answering system-specific questions.
* We're responsible for accelerating the speed and accuracy of communication between teams/stakeholders. Having precise documentation can help achieve this goal.
* We must ensure people will use our product. Lacking proper documentation could lead to potential customers deciding to use a different product instead or implement their custom solution.

After realizing that we had to improve the current state of our documentation, we researched how engineers record information at other companies and open-source projects. We explored how documentation is written at Google by reading the corresponding chapter in the book [Software Engineering at Google](https://abseil.io/resources/swe-book/html/ch03.html##documentation-id00039). We also researched how engineers record the necessary information on the [Django Python project](https://docs.djangoproject.com/en/4.2/).

After doing all our research, we concluded that before you start writing or changing existing documentation, you should always ask the following questions.
* WHO? You need to know the audience, and each document should have a dedicated owner; otherwise, they'll quickly become stale.
* WHAT? What category does the document belong to? Is it a tutorial, a reference doc, a how-to guide, or a design doc?
* WHY? What's the purpose of the document? What kinds of questions will it answer?
* WHEN? When was the document created, reviewed, or updated?
* WHERE? Where should the document live? In Confluence, Miro, Word, or version control?

## Questions


### Who is the target audience?

One of the mistakes engineers sometimes make is not considering the wide range of an audience that will read the documentation they wrote. If the target audience is not well-defined, you could quickly end up in a situation where people will approach you with questions. This way, you will lose time, and your productivity will drop, which you wanted to avoid by writing proper documentation.


The team behind Google recommends targeting your audience based on the following dimensions:

* Experience level: Expert programmers <-> Non-technical people

* Domain knowledge: Team members <-> Other people in the organization who are not familiar with your product

* Purpose: End users who might need your API to do a specific task and need to find that information quickly <-> Software gurus who need to gain a deep understanding of the internals of the library


### Who is the owner of the document?

Documents without explicit owners can quickly become stale. An owner can be a team or an individual. With dedicated owners, you can apply the processes you already have for writing code (i.e., ticketing system, bug tracking, code reviews).


### What is the category of the document?

The team behind Django uses the following four classes to categorize documentation:


#### Tutorials

Tutorials are lessons with the primary goal of quickly onboarding someone to the library/technology. Readers of the tutorials can be novices with little previous technical expertise.


_Analogy_

If you want to teach a child to cook, focus less on the what and more on the how. I.e., what you cook is less important than teaching the child how to use the utensils properly. Your goal is to motivate your students by giving them a chance to succeed. The main focus is on learning by doing.

_Best practices_

* Allow the user to learn by doing.

* Make sure that your tutorial works across systems.

* If it does not work, you risk losing users.

* Ensure that the user sees results immediately.

_Example_

How to set up a simple CRUD Spring Boot app with Mongo.


#### How-to guides

Goal-oriented. Answers a specific question that only people with some experience can ask. The target audience is not a complete beginner like for a tutorial. 

_Analogy_

A recipe.

_Best practices_

* Provide a series of steps.

* Focus on results.

* Solve a particular problem.

_Example_

Readme.md in a project.


#### Reference guides

Reference guides are technical descriptions of the machinery and how to operate it. To-the-point reference material is information-oriented.

_Analogy_

An encyclopedia article of an ingredient.

_Best practices_

* Structure the documentation around the code.

* Be consistent.

* Do nothing but describe.

_Example_

API documentation.


#### Explanation

Understanding-oriented.

_Analogy_

A book about how cuisine has evolved.

_Best practices_

* Provide context.

* Discuss alternatives and opinions.

* Don't instruct or provide technical reference.

_Example_

Architectural decision records.



### Why are you writing this document?

Do you want to teach someone? Do you want to record why certain decisions were made? If you can answer this question, it's also easier to find the category that fits your document (tutorials, how-to guides, reference documentation, explanation).


### When was the document written, reviewed, or updated?

This information can increase the readers' trust in your document. Some of the tools (e.g., [Confluence](https://www.atlassian.com/software/confluence) can automatically record this information.


### Where do you want to store the document?

We have many options where to store information, but our freedom comes with responsibility. E.g., [Miro](https://miro.com/) is an excellent tool for collaboration and brainstorming. Still, if you want to record why the team made specific architectural decisions, it's better to store your document in version control and assign a dedicated owner. Collaboration tools like Miro can come and go, but code often lives for decades. If you store your technical documents next to your code, it's less likely that they will get lost.


## Conclusion

The idea that we must write proper documentation can be daunting, especially since we have many responsibilities as software engineers. Most of us are not native speakers or technical writers. Most of us -including myself- learned to program not because I wanted to spend my time writing documentation. However, the bigger your project, the more people read its documentation. If it's inaccurate or incomplete, people will have more questions you'll need to answer, leading to decreased productivity and miscommunication. As we're responsible for making the business successful, we must reconsider our documentation strategy.


The following actions can help you improve your documentation:

* Set specific rules in the team and revise them frequently.

* Categorize existing docs.

* Always ask the questions mentioned in this blogpost before you touch existing docs/start writing new ones.

* Keep the number of docs to the minimum and clean up legacy docs.

## References
* [Software Engineering at Google](https://www.oreilly.com/library/view/software-engineering-at/9781492082781/)
* [Writing documentation at Django](https://docs.djangoproject.com/en/dev/internals/contributing/writing-documentation/)