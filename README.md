# AI Operations Portfolio Samples

> These are synthetic portfolio demonstrations created for this repository. They are not employer, client, or production work, and they contain no real user data or media.

This repository demonstrates two structured workflows related to AI operations: evaluating model responses and documenting multimodal annotations.

## 1. AI response evaluation

### Rubric

Score each dimension from 1 (serious issue) to 5 (strong performance), and support the score with evidence from the response.

| Dimension | Review question |
| --- | --- |
| Accuracy | Are factual claims and calculations correct? |
| Relevance | Does the response address the user’s request? |
| Consistency | Does the explanation agree with its conclusion? |
| Instruction adherence | Does it follow the requested scope and format? |
| Clarity | Is it easy to understand and free of ambiguity? |

### Synthetic example

**Prompt:** A notebook costs £24 after a 20% discount. What was its original price? Show the calculation.

**Response A:** The original price was £28.80 because 20% of £24 is £4.80, then £24 + £4.80 = £28.80.

**Response B:** The original price was £30. The discounted price is 80% of the original, so £24 ÷ 0.8 = £30.

| Response | Accuracy | Relevance | Consistency | Instruction adherence | Clarity | Evidence note |
| --- | ---: | ---: | ---: | ---: | ---: | --- |
| A | 1 | 4 | 2 | 5 | 4 | It calculates 20% from the discounted amount rather than the original price. |
| B | 5 | 5 | 5 | 5 | 5 | It correctly treats £24 as 80% of the original and shows the calculation. |

## 2. Multimodal annotation

The records below are fictional text descriptions; no image, audio, or video files are included.

| ID | Modality | Observable content | Example labels | Quality note |
| --- | --- | --- | --- | --- |
| IMG-001 | Image | A red ball resting on short grass. | object: ball; color: red; setting: outdoors | Record visible attributes only. |
| VID-001 | Video | A person opens a door and walks into a room. | action: opening door; action: entering room | Add timestamps when footage is available; do not infer identity. |
| AUD-001 | Audio | One speaker says, “Turn left at the next street.” | speech: present; speaker_count: 1; transcript: provided sentence | Mark unclear words as uncertain instead of guessing. |

Suggested fields: `sample_id`, `modality`, `description`, `labels`, `timestamp`, `confidence`, and `notes`.

## Quality workflow

1. Read the task instructions and label definitions before reviewing data.
2. Check claims, calculations, labels, and transcripts against available evidence.
3. Apply each evaluation criterion or annotation label consistently.
4. Note ambiguity and uncertainty; do not fill gaps with assumptions.
5. Run a final check for omissions, duplicates, formatting issues, and guideline compliance.

## Scope

These examples illustrate a documentation approach for AI response evaluation and multimodal data annotation. They do not represent production accuracy, project volume, or work performed for a named client or employer.
