---
layout: project
type: project
image: img/wordle/wordle-square.jpg
title: "Wordle"
date: 2022
published: true
labels:
  - Python
  - Information Entropy
summary: "Program to give you the best words to use to increase your chances of winning Wordle"
---

<img class="img-fluid" src="../img/wordle/wordle_banner.png">

Wordle is a popular web-based word game.



## How Wordle works

In Wordle you are given a specific number of turns to guess the word that was chosen.  For each consecutive word you are given a different color in each letter block, they will either indicate if that letter exists at all, if it exists but in a different block, or if that letter exists in that specific block.  Assigning values to those three specific states of the blocks, we get a specific pattern.

## How the program works

We use this information from these patterns to deduce which other words may match this pattern and see which word will lower the amount of words left in the "dictionary" the most.  The best first word to reduce the number of possibilities may not be used when you want to use two words to reduce the possibilities as there maybe information overlap.  This program will give you the best word, or words to use, for a given scenario.  What words came before, if any, and how many possibilities you may have left.

## Sample Code
Sample code to give of the quality of the guessed word.

```python
def qualityofguess(guess):
    patterndict={}
    searchspace={}
    #Get the Total number of possible words for the answers
    N=len(answers)
    
    #For each possible Answer we will get the pattern our guess input word creates and store it in the pattern dictionary
    #Similar patterns will increase that specific patterns key count.
    for ans in answers:
        pattern = tuple(compare(guess,ans))
        
        if pattern in patterndict.keys():
            patterndict[pattern]+=1
        else:
            patterndict[pattern]=1
            
    sum=0
    
    #We double check if the number of keys in the pattern dic is equal to the total number of words
    for keys in patterndict.keys():
        sum+=patterndict[keys]
    if(sum)==N:
        entropy=0
        for keys in patterndict.keys():
            entropy+=patterndict[keys]*math.log(patterndict[keys])
            #Normalize it over the total number of available answers to get a number between 0 and 1
        entropy=entropy/N
        return entropy

```

Source: <a href="https://github.com/jogarces/ics-313-text-game"><i class="large github icon "></i>jogarces/ics-313-text-game</a>

