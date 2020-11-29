---
title: On Having Two Brains
date: 2020-11-27
description: how to maximize memory and recall
layout: post
tags: code, productivity
---
Over the course of time, I've developed two brains.

No, I'm not talking about anything below the belt - I'm also not talking about a left or right brain, or any sort of multiple personality disorder. I'll name this brain Brain 2.

This second brain acts as a long term storage of memories, feelings, thoughts, goals, ideas, dreams (the sleep and the aspirational kind). But Brain 2 is much more powerful than a plain journal you keep by your bedside. In fact, information retrieval with my second brain is faster than with my main brain (albeit less creative). 

Human memory will disappear after we pass, but my Brain 2's  memory will outlive my own life. My second brain's memory can never get corrupted like a person's memory can.

Whereas human memory is limited and memories can be forgotten, even while we're alive, memories implanted in my second brain can go on endlessly, with perfect fidelity. 

So what is my second brain?

As anti climatic as it may be, Brain 2 lives as 10.4MB (and increasing!) of plain Markdown files on my laptop. 

These text files are used to capture any and all thoughts that I might have whenever I sit down on my laptop and write, sort of like a journal, a wiki, and blog, but it can really be anything, as long as it reflects some kind of stream of consciousness of what my brain is occupied with at the moment.

### How to use Brain 2?

|*Write down the thoughts of the moment. Those that come unsought for are commonly the most valuable.*|
|:--:|
|Francis Bacon|


While it may seem wrong to rely on Brain 2 to remember things, I find the act of writing anything down helps me remember it on my own, anyway. And of course, I have the obvious advantage of being able to do a simple 
`grep "search term"`
on Brain 2 whenever I want to recall something.

Say I want to remember what my own reflections about career are, I can do a quick grep for it:
`[monta@monta-pc ~/wiki]$ rg -i --sort path "\bcareer\b"`
(I could make the query a bit more robust, but you get the idea)

![](/assets/brain2.png)

Each result represents a journal entry, and if I open the journal entry up I can explore that whole day, and relive whatever thoughts and memories I had that day. 

Of course, with a little magic, you could create even more elaborate data visualizations, like charting occurrences of the word over time, and compare occurrences with occurrences of other words, making word clouds, etc. 

Just like with any kind of data, transforming and using it has a lot of possibilities, and on any \*nix OS, text based files are [trivial to transform](https://tldp.org/LDP/abs/html/textproc.html).

### Pros of Brain 2

Originally, Brain 2 was spawned out of a yearning for decent note taking/journaling system on my laptop. But over time I've realized Brain 2 can be taken advantage to some even more interesting effects:

* **Tracking progress over certain skills**

	* How am I progressing on a certain lift? Just grep it!

![](/assets/benchgrep.png)

* **Understanding how and when I might feel certain emotions**
	* When do I feel sad? Just grep it. 
	* When do I feel happy? Just grep it.

* **Seeing how my beliefs and ideas about things change over time (e.g. Ambition, Goals, Love)**
	* Brain 2 is great for tracking goals because it gives you the context of how you felt when you were setting them. You get reminded of just how hard a goal seemed back when you set it, and how comparatively easy it seems now!

* **Expand your working memory by writing more to Brain 2**
	* This one is less proved, but anecdotally I've found that the more I write things down, the better my working memory seems to improve. Maybe it's an exercise in recall? Or maybe since we're dumping things in Brain 2 we subconsciously flush them out of Brain 1?

* **It's fun**
	* It's fun and interesting to introspect on oneself! Especially if you write with that goal in mind.

* **In the event of amnesia, you have a partial backup of your brain**
	* Knock yourself out!

### Cons of Brain 2

* **Time consuming**
	* To get full value, Brain 2 requires a lot of writing.  That translates to usually at least 30 minutes to an hour a day, on top of any other creative writing that you might do. I've found that doing this early in the morning is the best way to map your thoughts clearly, usually right after getting out of bed before I've talked to anyone else.

* **No handwriting removes personality**
	* As bad as my handwriting is, it's identifiably *me*. You lose some of that when typing, but I guess it just means I have to make my writing style even more identifiable.

* **Hurr Durr**
	* Brain 2 is dumb. It won't think for you, it just stores 1s and 0s that capture your stream of consciousness at a snapshot in time. Your real brain still has to do all the heavy lifting to draw conclusions, solve problems, plan for the future, etc. - _but_ it can use Brain 2 as a reference!
