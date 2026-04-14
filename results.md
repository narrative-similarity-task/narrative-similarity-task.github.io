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


| Team                | Rank Track A   | Accuracy Track A   | Rank Track B   | Accuracy Track B   |
|:--------------------|:---------------|:-------------------|:---------------|:-------------------|
| COGNAC              | 1              | 78.00              | 1              | 72.00              |
| FactUEP             | 2              | 75.75              | -              | -                  |
| AI-Monitors         | 3              | 75.00              | -              | -                  |
| TeleAI              | 4              | 74.75              | 4              | 69.50              |
| YNU-HPCC            | 5              | 74.25              | 2              | 71.25              |
| UTD-HLTRI           | 6              | 74.00              | -              | -                  |
| JCT Dvori and Rinat | 7              | 73.75              | -              | -                  |
| CuriosAI            | 8              | 73.50              | 15             | 63.00              |
| Yam                 | 9              | 73.00              | -              | -                  |
| CascadeMind         | 10             | 72.75              | -              | -                  |
| Team CV             | 11             | 70.75              | 13             | 64.50              |
| hermeneutic_hools   | 12             | 70.50              | -              | -                  |
| NCL&HKU-NarrSim     | 13             | 70.25              | 8              | 68.50              |
| NarSiL              | 13             | 70.25              | -              | -                  |
| DUTIR               | 15             | 69.75              | -              | -                  |
| CophiWue            | 16             | 69.50              | 18             | 61.50              |
| CITD@UIT            | 17             | 69.25              | 6              | 68.75              |
| ttda704             | 17             | 69.25              | 6              | 68.75              |
| Narrative Nexus     | 19             | 68.50              | -              | -                  |
| harapalb            | 20             | 68.25              | -              | -                  |
| Comhis              | 20             | 68.25              | 10             | 66.00              |
| SoloSemantics       | 22             | 68.00              | 9              | 66.50              |
| schmerle            | 23             | 67.75              | -              | -                  |
| L3IRIT              | 24             | 65.75              | 20             | 61.00              |
| NLP-FSDM            | 25             | 65.50              | 16             | 62.00              |
| Team UBSE           | 26             | 65.25              | 12             | 64.75              |
| MarSan              | 27             | 65.00              | 11             | 65.50              |
| MoodMetric          | 27             | 65.00              | 16             | 62.00              |
| PEU Lab             | 29             | 64.50              | -              | -                  |
| Narrative Team      | 30             | 64.25              | 5              | 69.25              |
| ChulaNLP            | 31             | 63.50              | 21             | 60.75              |
| blue                | 32             | 62.50              | -              | -                  |
| Team HausaNLP       | 33             | 61.50              | -              | -                  |
| TFB                 | 34             | 61.25              | 18             | 61.50              |
| Spinfo Cologne      | 35             | 60.25              | 24             | 57.75              |
| LIAAD INESCTEC      | 36             | 59.75              | -              | -                  |
| Cryptix             | 37             | 59.50              | 25             | 57.50              |
| CICL26              | 38             | 59.00              | -              | -                  |
| Duluth              | 39             | 58.50              | -              | -                  |
| IIITH Boys          | 40             | 57.75              | 26             | 54.75              |
| Lacuna Inc.         | 41             | 57.25              | 27             | 54.50              |
| Mendel292           | 42             | 56.50              | 23             | 58.00              |
| PLlama              | 43             | 55.50              | -              | -                  |
| VerbaNexAI          | 44             | 53.50              | 22             | 59.25              |
| CUNI                | -              | -                  | 14             | 64.25              |
| hits_team           | -              | -                  | 3              | 70.50              |
