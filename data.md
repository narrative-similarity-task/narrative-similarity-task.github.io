---
layout: article
key: data
title: Data
---
In total, we annotated just over 1000 triples of story summaries. All summaries are sourced from Wikipedia.

- [Sample data](SemEval2026-Task_4-sample.zip): 39 items (with labels)
    - Also available as individual items, simulating Track B


Some data is yet to be released, check the [timeline](/timeline) for information on when it's coming:
- Development set: 200 items (with labels)
    - Also available as individual items, simulating Track B
- Test set: 400 triples + 849 individual stories. Labels will only be released after the completion of the shared task.
- Synthetic training data: We provide 1000 triples that are written using LLMs. They are intended to lower the barrier of entry (making it easy to fine-tune any model you like). Participants are free (and encouraged) to create your own synthetic data.


## Data Format
All data is provided in JSONlines format. In JSONlines, each line is a JSON object.
For Track A, all data takes the form of triples, with a boolean variable indicating whether text A is narratively more similar to the anchor than text B.
A labeled example might look like this:

```json
{
  "anchor_text": "A story about finding love.",
  "text_a": "Another story about finding love.",
  "text_b": "Unrelated text.",
  "text_a_is_closer": true
}
```

For Track B, the data we give out for evaluation is much simpler:
```json
{
    "text": "This is the story."
}
```
