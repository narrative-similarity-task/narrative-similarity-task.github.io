---
layout: article
key: data
title: Task Data
---
In total we annotated just above 1000 triples of story summaries. All summaries are sourced from Wikipedia.


- Sample data: 39 items (with labels)
    - Also available as individual items simulating Track B


Some data is yet to be released, check the [timeline](/timeline) for information on when its coming:
- Development set: 200 items (with labels)
    - Also available as individual items simulating Track B
- Test set: 400 triples + 849 individual stories. Labels will only be released after the completion of the shared task.
- Synthetic training data: we provide 1000 triples that are written using LLMs. They are intended to lower the barrier of entry (making it easy to fine-tune any model you like). You are free (and encouraged) to create your own synthetic data.


## Data Format
All data is provided in jsonlines format. In jsonlines each line is a json object.
For Track A all data takes the form of triples, with a boolean variable indicating if text A is narratively more similar to the anchor than text B.
A labeled example might look like this:

```json
{
  "anchor_text": "A story about finding love.",
  "text_a": "An other story about finding love.",
  "text_b": "Unrelated text.",
  "text_a_is_closer": true
}
```

For Track B the data we give out for evaluation is much simpler:
```json
{
    "text": "This is the story."
}
```
