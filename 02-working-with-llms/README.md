# Working With LLMs — Notes

## Tokenizer Experiment

- English: "The weather today is sunny and I feel great." → X tokens
- Arabic: "الجو النهاردة حلو وأنا حاسس إني تمام" → Y tokens

## Observation

- In english it costs 9 tokens
- In arabic it costs 13 tokens

## Sampling Parameters — takeaways

- Temperature: reshapes distribution (low=deterministic, high=creative)
- Top-K: fixed-size cutoff
- Top-P: adaptive cutoff by cumulative probability (usually preferred)
- Repetition penalty: discourages loops

## Rule of thumb for my projects

- RAG/structured output → low temp (0–0.3), top-p ~0.5–0.8
- Creative/chat features → higher temp (0.7–1), top-p ~0.9
