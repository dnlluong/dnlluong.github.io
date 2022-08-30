---
layout: project
type: project
image: img/cotton/wordle-banner.jpeg
title: "Wordle"
date: 2022
published: true
labels:
  - Python
summary: "Program to give you the best words to use to increase your chances of winning Wordle"
---

<img class="img-fluid" src="../img/cotton/cotton-header.png">

Wordle is a popular web-based word game.



## How to play

In Wordle you are given a specific number of turns to guess the word that was chosen.  For each consecutive word you are given a different color in each letter block, they will either indicate if that letter exists at all, if it exists but in a different block, or if that letter exists in that specific block.  Assigning values to those three specific states of the blocks, we get a specific pattern.

We use this information from these patterns to deduce which other words may match this pattern and see which word will lower the amount of words left in the "dictionary" the most.  The best first word to reduce the number of possibilities may not be used when you want to use two words to reduce the possibilities as there maybe information overlap.  This program will give you the best word, or words to use, for a given scenario.  What words came before, if any, and how many possibilities you may have left.



Source: <a href="https://github.com/jogarces/ics-313-text-game"><i class="large github icon "></i>jogarces/ics-313-text-game</a>

