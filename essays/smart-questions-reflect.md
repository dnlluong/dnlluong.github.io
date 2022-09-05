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
Question:how can I achieve multiple conditional inheritance?

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

While the question does not give us enough specific information, it gives us enough information once we open the link and see the intial information provided about the problem.  He provides his code that is easily able to be copied and pasted to reproduce the result he posted.  He also informs us what the code should intend to do.  This elicits more than a couple solutions to his problem from multiple people willing to help, with their own code that can be copy and pasted to try their "fix" of the problem.  While this is not the "best" question, it hits most of the check marks of being specific enough about their problem, provided easy examples to be reproduced, what his output is, and what his desired output is.

## The Opposite end of the Spectrum

Stack Overflow is loaded with a bunch of great, amazing, smart questions.  The same can be also said about the other end.  There are also a bunch of questions of Stack Overflow that may not have any responses or few that may not even solve the question.  It may not be because the question is insolvable but more in a way that it is hard to infer what they are asking or they made it too inconvenient to even try to attempt to help them.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

Like Steve Jobs said,  people are willing to help if you ask.  If you're gonna ask though, you better not be wasting their time.  When they go and view your question, they should be spending more time trying to help you solve your problem than spending time trying to see what your problem is in the first place, or even understand what problem you are having.
