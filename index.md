---
layout: article
title: Narrative Similarity Task
---


In the shared task **SemEval-2026 Task 4: Narrative Story Similarity and Narrative Representation Learning** you (or rather your systems) are asked to identify narratively similar stories.
We define Narrative similarity by three core similarity components: the *abstract theme*, the *course of action* and the *outcomes* of a story.

In simple terms these can be understood as:
- Abstract Theme: The ideas and motives of the story.
- Course of Action: The sequence of central events, turning points etc.
- Outcomes: The results of a story.

For a detailed definition check out our [annotation guidelines](TODO)!


## Example
This sample serves to illustrate similarity judgments required for this task. The actual texts are story summaries from Wikipedia.
Which option, **A** or **B**, is more narratively similar to the anchor story?

![Example Task](img/sample.png)

**Click below** to reveal the answer:
<details>
  <summary>Reveal Answer</summary>
  In the above example story A is considered more similar.
  A, B, and the anchor all tell the story of a lost item that is retrieved. In the case of A, it is found by a third party (as it is in the anchor), while in B it is not found at all.
</details>


## Contact

Join our [mailing list](https://groups.google.com/g/narrative-similarity-task).
If you have any questions directed at the organizers you can reach us [here](mailto:narrative-similarity-task-organizers@googlegroups.com).

## All Submissions Are Welcome!
While we appreciate all submissions we want to especially encourage the submission of **symbolic representation**-based systems for Track A.
Can any story grammar, narrative graph, or schema be used to represent a story for similarity judgements? We would like to know!
As we expect symbolic systems to have a harder time abusing biases in our data we will keep a seperate rankings for symbolic submissions.

## The Two Tracks
In **Track A** your system gets a triple consisting of an anchor story and two choices: A and B.
Your system is asked to identify which of the two choices is more similar.

**Track B** instead asks you to produce a vector representation for an individual story.
These representations should have a cosine similarity that aligns with the underlying stories' narrative similarities.
We, the organizers, will validate your submitted representations against triple-wise similarity ratings.

## Rules
In Track B, embeddings are, at inference time, to be created **on individual story instances only**.
You may, for example, not create embeddings such that they align with Track A-style answers for a full cross-product of triples across the provided dataset.
Be kind, have fun!

## Organizers
- [Hans Ole Hatzel](https://www.inf.uni-hamburg.de/en/inst/ab/lt/people/hans-ole-hatzel.html), University of Hamburg
- Ekaterina Artemova, Toloka AI
- [Haimo Stiemer](https://www.linglit.tu-darmstadt.de/institutlinglit/mitarbeitende/stiemer/stiemer.de.jsp), Technical University of Darmstadt
- Natalia Fedorova, Toloka AI
- [Evelyn Gius](https://www.linglit.tu-darmstadt.de/institutlinglit/mitarbeitende/gius/), Technical University of Darmstadt
- [Chris Biemann](https://www.inf.uni-hamburg.de/en/inst/ab/lt/people/chris-biemann.html), University of Hamburg

## Acknowledgments

The work was supported by the German Research Foundation (DFG) under grant BI 1544/11-2 as part of the project ``Unitizing Plot to Advance Analysis of Narrative Structure (PLANS)''.
