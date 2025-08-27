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

The task is currently running [here on CodaBench](https://www.codabench.org/competitions/10273/).

## Baselines
We provide [baseline systems](https://github.com/narrative-similarity-task/semeval-2026-task-4-baselines) for both tracks for you to build upon.
The output format of the baselines is suitable for uploading to CodaBench.
The baselines in the CodaBench leaderboard are the GPT-4o-mini prompting approach for Track A and a sentenceBERT approach (specifically "all-MiniLM-L6-v2") for Track B.

## Rules
In Track B, embeddings are, at inference time, to be created **on individual story instances only**.
You may, for example, not create embeddings such that they align with Track A-style answers for a full cross-product of triples across the provided dataset.

Embeddings for Task B may be anywhere from 10 to 8192 in length.

Be kind, have fun!

## How To Submit to CodaBench
You will need to upload a zip file with the following structure:
```
.
├── track_a.jsonl
└── track_b.{npy,jsonl}
```

Make sure to fulfill all these requirements:
- Have a file for each track you are participating in (you can deselect either one on the upload page)
- Each file needs to be at the root level of the zip file
- The order in the files must correspond to the order in the provided data
- For Track A, your labels need to be in the "text_a_is_closer" property of each line
- For Track B, you may either place your embeddings as a list of floats in the `embeddings` property or provide a numpy serialized file.

The [baseline systems](https://github.com/narrative-similarity-task/semeval-2026-task-4-baselines) showcase a possible way to create the data.

In the upload form, make sure to specify:
1. the type of method your system is using in each track.
2. which of the tracks (either one or both) you are submitting to.

![Make sure to select the methodology and correct track](/img/upload_codabench.png)
