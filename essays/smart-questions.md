---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2026-09-10
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="500px" class="rounded float-start pe-4" src="../img/badQuestion.png">

## Questions That Will Get Answers

When learning how to program or during programming, getting stuck on a problem is bound to happen. There are going to be a lot of times when I’m not going to be able to figure out why my code is not working or why a different programming language is giving me errors I didn't expect. That's where asking someone else for help can be a really helpful way to solve the problem that I'm stuck on, but the key is how I ask that question is where a lot of people mess up on. After reading Eric Raymond’s [How to Ask Questions the Smart Way](http://www.catb.org/esr/faqs/smart-questions.html), I learned that asking a good question requires more than just saying that something does not work or how do I fix this. A smart question should show that I have already put effort into solving the problem while also giving someone enough information to understand what I am struggling with.

## What Makes a Question Smart?

[StackOverflow](https://stackoverflow.com/questions) is a useful resource for programmers like myself because developers can ask questions and receive help from others in the programming community. The only problem with this is that the people answering these questions do not need to help. Thus, Eric Raymond explains that we should respect their time by researching the problem first and clearly explaining the problem you need help with.

A good question should explain what you are trying to accomplish, the relevant code behind it, show the error, errors, or unexpected result, and explain what you did to try and fix it. This should be specific enough that someone does not have to guess what the problem is.

## A Question Asked the Smart Way

The question I chose was "[Why does typing the return value of my function make the return value typed unknown?](https://stackoverflow.com/questions/79976653/why-does-typing-the-return-value-of-my-function-make-the-return-value-typed-unkn)" The developer was working with TypeScript and had an asynchronous function that was supposed to return a Promise<TeamType[]>. However, the function called another function named httpRequest, and TypeScript treated the value returned from that function as unknown. This caused an error because an unknown value could not automatically be returned as a TeamType[].

Question that was asked:
<img width="500px" class="rounded float-start pe-4" src="../img/goodQuestion.png">

What made this a smart question was that the developer did not simply say, “My TypeScript code doesn't work.” They provided the relevant code, showed the error TypeScript was giving them, and explained what they had already tried. They discovered that using as TeamType[] made the error disappear, but instead of stopping there, they wanted to understand why TypeScript required them to do that.

This follows Raymond’s guidelines because it shows that the developer had already put effort into solving and understanding the problem. The question also gave other developers enough information to figure out what was happening without having to ask a bunch of follow-up questions.

The responses show why asking a smart question can lead to better help. One answer explained that the httpRequest function was using a generic type, but TypeScript did not have enough information to determine what that type should be. Because of this, the returned value became unknown. The answer showed that the developer could specify the type when calling the function, such as httpRequest<TeamType[]>(). The response did more than just provide working code because it explained why the problem was happening.

Answer to the Question:
<img width="500px" class="rounded float-start pe-4" src="../img/goodAnswer.png">

The developer received an answer and confirmed that the solution helped them understand the problem. I think this is a good example of what Raymond means by asking questions the smart way. Since the question was clear, concise, and included the necessary information, the people answering focused on solving and explaining the actual problem instead of trying to figure out what the developer was trying to ask.

## How Not to Ask for Help

A not-so-smart question I found on Stack Overflow was [“ReactQuery + Typescript how to type query.”](https://stackoverflow.com/questions/75262215/reactquery-typescript-how-to-type-query) The developer was having a problem with TypeScript while using React Query, but they provided little to no explanation about what was actually going wrong. Their main description was "hello why i have typescript error?." They did not clearly explain what they expected the code to do, how they thought it should work, or what they did to try to fix the problem. They just asked a very poorly written question with pictures of their code, no background, no nothing, which is probably the reason why no one responded to this question.

Poorly Written Question:
<img width="500px" class="rounded float-start pe-4" src="../img/badQuestion2.png">

This goes against many of Raymond’s recommendations because the developer did not make it easy for other people to understand the problem. Although some information and code were provided, there was not enough explanation to show that they had researched the issue or attempted different solutions before asking for help. Someone trying to answer the question had to figure out what the developer was trying to accomplish instead of being able to focus directly on the problem.

The responses also show how asking a question this way can make getting help less effective. Someone was still able to provide a possible solution, but they had to make assumptions about what the developer was trying to do. This could have been avoided if the developer had included the exact problem, what they expected to happen, and what they had already tried. Overall, this question shows how providing too little information can make it harder for other developers to give quick and useful answers.

## My Takeaways

Comparing these two types of questions helped me understand that asking a programming question is a skill on its own. Before asking someone for help, I should first research the problem and try different solutions myself. Even if I cannot figure it out, doing that research gives me more information that I can include when I eventually ask my question.

I also learned that simply saying “my code doesn't work” is not enough. If I want someone to help me, I should make their job as easy as possible. Including my code, the exact error, what I expected to happen, what actually happened, and what I have already tried gives someone a much better starting point.

The TypeScript question especially showed me that a smart question does not only help someone find a solution. It can also help them understand why the solution works. The developer had already found a way around their error by using as TeamType[], but they still asked why it was necessary. Because of that, they learned more about TypeScript generics instead of simply copying a solution and moving on.

## Conclusion

Overall, this experience showed me that communication is just as important in software engineering as knowing how to write code. There will always be problems that I cannot immediately solve on my own, so knowing how to ask for help is something that I will continue to need throughout my career. Asking a smart question means respecting the time of the people helping me while also giving myself the best chance of receiving a useful answer.

Moving forward, I want to make sure that I research my problem first, explain exactly what I am struggling with, and include only the information that is necessary to understand the problem. I may not always ask the perfect question, but following Raymond’s guidelines can help me ask questions that lead to faster, clearer, and more useful answers.
