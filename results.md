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
<script>
// Wait until the page and all external scripts are fully loaded
window.addEventListener('load', function() {
  
  // 1. Define the custom sort extension
  Tablesort.extend('rank-with-dash', 
    function(item) {
      item = item.trim();
      return !isNaN(item) || item === '-';
    }, 
    function(a, b) {
      const valA = a.trim() === '-' ? -999999 : parseFloat(a);
      const valB = b.trim() === '-' ? -999999 : parseFloat(b);
      return valA - valB;
    }
  );

  // 2. Initialize your table here as well! 
  // (If this was outside the listener, it would also throw an error)
  new Tablesort(document.getElementById('your-table-id'));

});
</script>

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


| Team                | Rank Track A   | Accuracy Track A (%)  | Rank Track B   | Accuracy Track B (%) |
|:--------------------|:---------------|:-------------------|:---------------|:-------------------|
| COGNAC              | 1              | 78.00              | 1              | 72.00              |
| FactUEP             | 2              | 75.75              | -              | -                  |
| AI-Monitors         | 3              | 75.00              | -              | -                  |
| TeleAI              | 4              | 74.75              | 4              | 69.50              |
| YNU-HPCC            | 5              | 74.25              | 2              | 71.25              |
| JCT Dvori and Rinat | 6              | 73.75              | -              | -                  |
| CuriosAI            | 7              | 73.50              | 15             | 63.00              |
| Yam                 | 8              | 73.00              | -              | -                  |
| CascadeMind         | 9              | 72.75              | -              | -                  |
| Team CV             | 10             | 70.75              | 13             | 64.50              |
| hermeneutic_hools   | 11             | 70.50              | -              | -                  |
| NCL&HKU-NarrSim     | 12             | 70.25              | 8              | 68.50              |
| NarSiL              | 12             | 70.25              | -              | -                  |
| DUTIR               | 14             | 69.75              | -              | -                  |
| CITD@UIT            | 15             | 69.25              | 6              | 68.75              |
| ttda704             | 15             | 69.25              | 6              | 68.75              |
| Narrative Nexus     | 17             | 68.50              | -              | -                  |
| Comhis              | 18             | 68.25              | 10             | 66.00              |
| harapalb            | 18             | 68.25              | -              | -                  |
| SoloSemantics       | 20             | 68.00              | 9              | 66.50              |
| schmerle            | 21             | 67.75              | -              | -                  |
| L3IRIT              | 22             | 65.75              | 19             | 61.00              |
| NLP-FSDM            | 23             | 65.50              | 16             | 62.00              |
| Team UBSE           | 24             | 65.25              | 12             | 64.75              |
| MarSan              | 25             | 65.00              | 11             | 65.50              |
| MoodMetric          | 25             | 65.00              | 16             | 62.00              |
| PEU Lab             | 27             | 64.50              | -              | -                  |
| Narrative Team      | 28             | 64.25              | 5              | 69.25              |
| ChulaNLP            | 29             | 63.50              | 20             | 60.75              |
| blue                | 30             | 62.50              | -              | -                  |
| Team HausaNLP       | 31             | 61.50              | -              | -                  |
| TFB                 | 32             | 61.25              | 18             | 61.50              |
| Spinfo Cologne      | 33             | 60.25              | 23             | 57.75              |
| LIAAD INESCTEC      | 34             | 59.75              | -              | -                  |
| Cryptix             | 35             | 59.50              | 24             | 57.50              |
| CICL26              | 36             | 59.00              | -              | -                  |
| Duluth              | 37             | 58.50              | -              | -                  |
| IIITH Boys          | 38             | 57.75              | 25             | 54.75              |
| Lacuna Inc.         | 39             | 57.25              | 26             | 54.50              |
| Mendel292           | 40             | 56.50              | 22             | 58.00              |
| PLlama              | 41             | 55.50              | -              | -                  |
| VerbaNexAI          | 42             | 53.50              | 21             | 59.25              |
| CUNI                | -              | -                  | 14             | 64.25              |
| hits_team           | -              | -                  | 3              | 70.50              |
