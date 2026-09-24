# Generation is Classification

*A conversational agent built from a model that can only choose.*

Lucian Lazar · 2026

**Abstract.** We build a conversational agent whose only model is a classifier: given a text and a set of
described options, it returns one of the options and a probability for each. It cannot emit a token. Every
word the agent says was an option that existed before the reply, and was chosen. The agent holds multi-turn
conversations, keeps a mood and a self-description across turns, says the user's own words back, spells
numbers digit by digit, and uses tools, all through the same primitive. "Thinking" is that primitive asked at
coarser grains (reply, sentence, word, character), with each answer written back into the text that the next
question reads. We report what made this work and what did not, as principles with the experiment behind
each: option descriptions matter and option counts do not; everything on the page is imitated, as meaning,
as words and as form; a repeated decision's winner is sticky while its distribution is not; and a decision
must be asked at the grain where it lives. Against the first working version, the deployed system spends 71%
fewer model calls per generated word, with longer replies and no empty ones. The claim is an existence
proof, not a competitor to language models: the replies are short, simple and slow.

- Demo: https://talktojev.com
- Paper (PDF, citable): https://doi.org/10.5281/zenodo.22940945 (also at https://talktojev.com/paper.pdf)
- Code: https://github.com/xucian/talktojev (archived: https://doi.org/10.5281/zenodo.22895303)
- Jev on X: https://x.com/jevprime
- What is Jev: https://typesafe.ai/blog/introducing-system-one-models-and-jev

This repository holds the paper's source: `paper.tex`, `author.txt`, `refs.bib`, `figures/`, and
`numbers.tex`, which is generated from the experiment runs by `make_numbers.py` in the code repository
(no experimental number is typed by hand). Build: `tectonic -X compile paper.tex`. The PDF is on Zenodo
and served at the demo site, not committed here. MIT license.

```
@misc{lazar2026generation,
  title     = {Generation is Classification: a conversational agent built from a model that can only choose},
  author    = {Lazar, Lucian},
  year      = {2026},
  publisher = {Zenodo},
  doi       = {10.5281/zenodo.22940945},
  note      = {Demo: https://talktojev.com. Code: https://github.com/xucian/talktojev (doi:10.5281/zenodo.22895303)}
}
```
