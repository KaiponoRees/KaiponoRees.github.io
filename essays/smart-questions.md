---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2015-09-08
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

[StackOverflow](https://stackoverflow.com/questions) is a useful resource for programmers because developers can ask questions and receive help from other people in the programming community. However, the people answering these questions are not obligated to help. Because of this, Eric Raymond explains that we should respect their time by researching the problem first and clearly explaining what we need help with.

A good question should explain what you are trying to accomplish, provide the relevant code, show the error or unexpected result, and explain what you have already tried. It should also be specific enough that someone does not have to guess what the problem is. One Stack Overflow question I found demonstrates these ideas well.

## A Question Asked the Smart Way

The question I chose was "[Why does typing the return value of my function make the return value typed unknown?](https://stackoverflow.com/questions/79976653/why-does-typing-the-return-value-of-my-function-make-the-return-value-typed-unkn)" The developer was working with TypeScript and had an asynchronous function that was supposed to return a Promise<TeamType[]>. However, the function called another function named httpRequest, and TypeScript treated the value returned from that function as unknown. This caused an error because an unknown value could not automatically be returned as a TeamType[].

Question that was asked:
<img width="300px" class="rounded float-start pe-4" src="../img/goodQuestion.png">

What made this a smart question was that the developer did not simply say, “My TypeScript code doesn't work.” They provided the relevant code, showed the error TypeScript was giving them, and explained what they had already tried. They discovered that using as TeamType[] made the error disappear, but instead of stopping there, they wanted to understand why TypeScript required them to do that.

This follows Raymond’s guidelines because it shows that the developer had already put effort into solving and understanding the problem. The question also gave other developers enough information to figure out what was happening without having to ask a bunch of follow-up questions.



While the heading of his question could be better, it does convey what he’s trying to figure out. Usually something as brief as “python date of previous month” is what other users would enter in as search terms on Google, making it easily found. Another good thing about the question is that it’s not just a question. The asker shows what he or she has done and that he or she has put in some effort to answer the question. And while it may not be as important as the question itself, the asker shows courtesy, which does increase the chance of getting an answer.

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
