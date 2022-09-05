---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2022-09-04
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

Steve Jobs:  “I've never found anybody that didn't want to help me if I asked them for help.”

## Do we think how we ask questions?

When I ask a question do I really think how I ask the question.  Most of the times, not really.  I just ask the question the best I can to be able to get a response to a question.  When I actually think about how I ask questions, I do realize there could be better ways and worse ways than the things I already do.  People are willing to help if you ask, to have respect for their time, we should try make their time helping us the shortest and easiest that we possibly can.  We can do this be asking smarter questions, Smart Questions.

## What’s a smart question?

Stack Overflow, a question and answer site for programmers, is an amazing resource.  I'd like to say that 99% of programmers, at least from the U.S, have used or at least heard of Stack Overflow.  With it having so many questions we can see good and bad of examples of people asking questions.  The Good ones tend to get the responses that they wanted, while the bad ones might take a while to navigate what they want from the questions, or even being ignored entirely.


In the following example, we examine the components of a decent question that gets the response wanted.

```
I have a type build that has a flag template, and according to the active flag bits, it inherits from those types. this allows me to "build" classes from many subclasses with a great number of configurations:

Code:
truct empty {};

template<std::uint8_t flags> 
using flag_a_type = std::conditional_t<(flags & FLAG_BIT_A), A, empty>;
template<std::uint8_t flags> 
using flag_b_type = std::conditional_t<(flags & FLAG_BIT_B), B, empty>;
template<std::uint8_t flags> 
using flag_c_type = std::conditional_t<(flags & FLAG_BIT_C), C, empty>;
template<std::uint8_t flags> 
using flag_d_type = std::conditional_t<(flags & FLAG_BIT_D), D, empty>;

template<std::uint8_t flags>
struct build : 
    flag_a_type<flags>, flag_b_type<flags>, flag_c_type<flags>, flag_d_type<flags> {

};

int main() {
    build<FLAG_BIT_A | FLAG_BIT_C> foo;
}

so build<FLAG_BIT_A | FLAG_BIT_C> should result in a class that inherits from A and from C.

but it doesn't compile, saying empty is already a direct base class:

error C2500: 'build<5>': 'empty' is already a direct base class
how can I achieve this without having to make 4 different empty structs to avoid the clash?

```



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
