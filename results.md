---
layout: article
permalink: /results/
title: Results
---
<style>
  /* Quick CSS for the Wikipedia-style indicators */
  th[role="columnheader"] { cursor: pointer; }
  th[role="columnheader"]:after {
    content: ' \2195'; /* Up/Down Arrow */
    font-size: 0.8em;
    opacity: 0.3;
    margin-left: 5px;
  }
  th[aria-sort="ascending"]:after { content: ' \2191'; opacity: 1; }
  th[aria-sort="descending"]:after { content: ' \2193'; opacity: 1; }

  .flex-container {
    display: flex;
    flex-direction: row;
    gap: 2rem; /* Creates space between the two columns */
    align-items: flex-start; /* Aligns text and images to the top */
  }

  .flex-item {
    flex: 1; /* Ensures both columns take up equal width (50% each) */
  }

  .flex-item img {
    max-width: 100%; /* Ensures the images don't overflow their containers */
    height: auto;
  }

  /* Responsive adjustment for mobile screens */
  @media (max-width: 768px) {
    .flex-container {
      flex-direction: column;
    }
  }
</style>

The shared task has concluded; we are waiting for the review process of all papers to take its course. We thank all participating teams and especially those who have created system description papers for us all to learn from!
This page captures the results for all teams; beside the final scores, you can also explore the decisions of each system on individual instances.

Once available, we will link all papers on this page.

## Result Exploration
We offer two views for exploring the decisions all teams made for individual examples.

<div class="flex-container" markdown="1">

<div class="flex-item" markdown="1">

[![Dataset Browser](/img/decision_browser.png)](/browse_dataset/)

For all teams and the complete test split, you can [explore the predictions here](/browse_dataset/).

</div>

<div class="flex-item" markdown="1">

[![Embedding Browser](/img/embedding_browser.png)](/browse_embeddings/)

For Track B, you can [explore all embeddings here](/browse_embeddings/). We use a patched version of the TensorBoard embedding projector; you can check out their [documentation](https://www.tensorflow.org/tensorboard/tensorboard_projector_plugin).

</div>

</div>

## Scores
You can sort this table by the results in Track A or Track B. For more details, see the papers once they are released (some time in summer 2026).


| Team                | Accuracy Track A (%)  | Accuracy Track B  (%) |
|:--------------------|:-------------------|:-------------------|
| COGNAC              | 78.00              | 72.00              |
| FactUEP             | 75.75              | -                  |
| AI-Monitors         | 75.00              | -                  |
| TeleAI              | 74.75              | 69.50              |
| YNU-HPCC            | 74.25              | 71.25              |
| JCT Dvori and Rinat | 73.75              | -                  |
| CuriosAI            | 73.50              | 63.00              |
| Yam                 | 73.00              | -                  |
| CascadeMind         | 72.75              | -                  |
| Team CV             | 70.75              | 64.50              |
| hermeneutic_hools   | 70.50              | -                  |
| NCL&HKU-NarrSim     | 70.25              | 68.50              |
| NarSiL              | 70.25              | -                  |
| DUTIR               | 69.75              | -                  |
| CITD@UIT            | 69.25              | 68.75              |
| ttda704             | 69.25              | 68.75              |
| Narrative Nexus     | 68.50              | -                  |
| Comhis              | 68.25              | 66.00              |
| harapalb            | 68.25              | -                  |
| SoloSemantics       | 68.00              | 66.50              |
| schmerle            | 67.75              | -                  |
| L3IRIT              | 65.75              | 61.00              |
| NLP-FSDM            | 65.50              | 62.00              |
| Team UBSE           | 65.25              | 64.75              |
| MarSan              | 65.00              | 65.50              |
| MoodMetric          | 65.00              | 62.00              |
| PEU Lab             | 64.50              | -                  |
| Narrative Team      | 64.25              | 69.25              |
| ChulaNLP            | 63.50              | 60.75              |
| blue                | 62.50              | -                  |
| Team HausaNLP       | 61.50              | -                  |
| TFB                 | 61.25              | 61.50              |
| Spinfo Cologne      | 60.25              | 57.75              |
| LIAAD INESCTEC      | 59.75              | -                  |
| Cryptix             | 59.50              | 57.50              |
| CICL26              | 59.00              | -                  |
| Duluth              | 58.50              | -                  |
| IIITH Boys          | 57.75              | 54.75              |
| Lacuna Inc.         | 57.25              | 54.50              |
| Mendel292           | 56.50              | 58.00              |
| PLlama              | 55.50              | -                  |
| VerbaNexAI          | 53.50              | 59.25              |
| CUNI                | -                  | 64.25              |
| hits_team           | -                  | 70.50              |