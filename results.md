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

The shared task has concluded; the system description papers have now been published in the ACL Anthology. We thank all participating teams and especially those who have created system description papers for us all to learn from!
This page captures the results for all teams; beside the final scores, you can also explore the decisions of each system on individual instances.

All system papers are now available in the ACL Anthology; team names below link to each paper. See our [task paper](https://aclanthology.org/2026.semeval-1.429/) for a full overview of all systems.

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
You can sort this table by the results in Track A or Track B. Team names link to each team's system description paper in the ACL Anthology.


| Team                | Rank Track A   | Accuracy Track A (%)  | Rank Track B   | Accuracy Track B (%) |
|:--------------------|:---------------|:-------------------|:---------------|:-------------------|
| [COGNAC](https://aclanthology.org/2026.semeval-1.290/)           | 1              | 78.00              | 1              | 72.00              |
| [FactUEP](https://aclanthology.org/2026.semeval-1.147/)          | 2              | 75.75              | -              | -                  |
| [AI-Monitors](https://aclanthology.org/2026.semeval-1.271/)      | 3              | 75.00              | -              | -                  |
| [TeleAI](https://aclanthology.org/2026.semeval-1.164/)           | 4              | 74.75              | 4              | 69.50              |
| [YNU-HPCC](https://aclanthology.org/2026.semeval-1.63/)          | 5              | 74.25              | 2              | 71.25              |
| [UTD-HLTRI](https://aclanthology.org/2026.semeval-1.433/)        | 6              | 74.00              | -              | -                  |
| [JCT](https://aclanthology.org/2026.semeval-1.387/)              | 7              | 73.75              | -              | -                  |
| [CuriosAI](https://aclanthology.org/2026.semeval-1.62/)          | 8              | 73.50              | 15             | 63.00              |
| [Yam](https://aclanthology.org/2026.semeval-1.421/)              | 9              | 73.00              | -              | -                  |
| [CascadeMind](https://aclanthology.org/2026.semeval-1.204/)      | 10 | 72.75              | -              | -                  |
| [Team CV](https://aclanthology.org/2026.semeval-1.374/)          | 11             | 70.75              | 13             | 64.50              |
| [hermeneutic_hools](https://aclanthology.org/2026.semeval-1.230/)| 12 | 70.50 | - | - |
| [NCL&HKU-NarrSim](https://aclanthology.org/2026.semeval-1.188/)  | 13             | 70.25              | 8              | 68.50              |
| [NarSiL](https://aclanthology.org/2026.semeval-1.381/)           | 13             | 70.25              | -              | -                  |
| [DUTIR](https://aclanthology.org/2026.semeval-1.378/)            | 15             | 69.75              | -              | -                  |
| [CophiWue](https://aclanthology.org/2026.semeval-1.430/)         | 16             | 69.50              | 18             | 61.50              |
| [CITD@UIT](https://aclanthology.org/2026.semeval-1.158/)         | 17             | 69.25              | 6              | 68.75              |
| [ttda704](https://aclanthology.org/2026.semeval-1.353/)          | 17             | 69.25              | 6              | 68.75              |
| [Narrative Nexus](https://aclanthology.org/2026.semeval-1.352/)  | 19             | 68.50              | -              | -                  |
| [harapalb](https://aclanthology.org/2026.semeval-1.283/)         | 20             | 68.25              | -              | -                  |
| [Comhis](https://aclanthology.org/2026.semeval-1.118/)           | 20             | 68.25              | 10             | 66.00              |
| [SoloSemantics](https://aclanthology.org/2026.semeval-1.201/)    | 22             | 68.00              | 9              | 66.50              |
| [schmerle](https://aclanthology.org/2026.semeval-1.257/)         | 23             | 67.75              | -              | -                  |
| [L3IRIT](https://aclanthology.org/2026.semeval-1.234/)           | 24             | 65.75              | 20             | 61.00              |
| [NLP-FSDM](https://aclanthology.org/2026.semeval-1.88/)          | 25             | 65.50              | 16             | 62.00              |
| [Team UBSE](https://aclanthology.org/2026.semeval-1.258/)        | 26             | 65.25              | 12             | 64.75              |
| [MarSan](https://aclanthology.org/2026.semeval-1.33/)            | 27             | 65.00              | 11             | 65.50              |
| [MoodMetric](https://aclanthology.org/2026.semeval-1.336/)       | 27             | 65.00              | 16             | 62.00              |
| [PEU Lab](https://aclanthology.org/2026.semeval-1.136/)          | 29             | 64.50              | -              | -                  |
| [Narrative Team](https://aclanthology.org/2026.semeval-1.22/)    | 30             | 64.25              | 5              | 69.25              |
| [ChulaNLP](https://aclanthology.org/2026.semeval-1.341/)         | 31             | 63.50              | 21             | 60.75              |
| [blue](https://aclanthology.org/2026.semeval-1.305/)             | 32             | 62.50              | -              | -                  |
| [Team HausaNLP](https://aclanthology.org/2026.semeval-1.7/)      | 33             | 61.50              | -              | -                  |
| [TFB](https://aclanthology.org/2026.semeval-1.367/)              | 34             | 61.25              | 18             | 61.50              |
| [Spinfo Cologne](https://aclanthology.org/2026.semeval-1.299/)   | 35             | 60.25              | 24             | 57.75              |
| [LIAAD INESCTEC](https://aclanthology.org/2026.semeval-1.277/)   | 36             | 59.75              | -              | -                  |
| [Cryptix](https://aclanthology.org/2026.semeval-1.168/)          | 37             | 59.50              | 25             | 57.50              |
| [CICL26](https://aclanthology.org/2026.semeval-1.310/)           | 38             | 59.00              | -              | -                  |
| [Duluth](https://aclanthology.org/2026.semeval-1.127/)           | 39             | 58.50              | -              | -                  |
| [IIITH Boys](https://aclanthology.org/2026.semeval-1.420/)       | 40             | 57.75              | 26             | 54.75              |
| [Lacuna Inc.](https://aclanthology.org/2026.semeval-1.296/)      | 41             | 57.25              | 27             | 54.50              |
| [Mendel292](https://aclanthology.org/2026.semeval-1.324/)        | 42             | 56.50              | 23             | 58.00              |
| [PLlama](https://aclanthology.org/2026.semeval-1.337/)           | 43             | 55.50              | -              | -                  |
| [VerbaNexAI](https://aclanthology.org/2026.semeval-1.392/)       | 44             | 53.50              | 22             | 59.25              |
| [CUNI](https://aclanthology.org/2026.semeval-1.274/)             | -              | -                  | 14             | 64.25              |
| [hits_team](https://aclanthology.org/2026.semeval-1.338/)        | -              | -                  | 3              | 70.50              |
