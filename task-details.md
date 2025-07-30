---
layout: article
key: data
title: Task Details
---

In **Track A**, your system gets a triple consisting of an anchor story and two choices: A and B.
Your system is asked to identify which of the two choices is more similar.

**Track B** instead asks you to produce a vector representation for an individual story.
These representations should have a cosine similarity that aligns with the underlying stories' narrative similarities.
We, the organizers, will validate your submitted representations against triple-wise similarity ratings.

The task will be run on Codalab.

## Baselines
We provide [baseline systems](https://github.com/narrative-similarity-task/semeval-2026-task-4-baselines) for both tracks for you to build upon.

Our output formats for your submission to Codalab are yet to be defined but will be integrated into the baseline systems.

## Rules
In Track B, embeddings are, at inference time, to be created **on individual story instances only**.
You may, for example, not create embeddings such that they align with Track A-style answers for a full cross-product of triples across the provided dataset.
Be kind, have fun!
