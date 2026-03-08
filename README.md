# Professional Trajectory Intelligence Prompt

This repository contains a prompt for GPT or Claude that reviews a person’s professional trajectory starting from their name.

It is meant for people whose work does not fit one neat title. Someone may be an engineering manager today, have been a software engineer earlier, and still publish research or maintain technical projects. Most career prompts flatten that. This one tries to reconstruct the actual shape of the person’s work.

## What it does

The prompt asks the model to build a structured review of a person’s public professional signal. It looks for evidence across roles, artifacts, feedback, and visible public material, then turns that into a report.

The report is designed to answer questions like these:

- What does this person appear to be, based on what others can actually see?
- What strengths show up repeatedly across time?
- Which technical or research threads have stayed constant?
- Do the public materials tell one coherent story, or a scattered one?
- Where do different sources contradict each other?
- What strengths are real but under-signaled?
- What is the clearest path to improve the person’s positioning?

## Who this is for

This works best for people with mixed or evolving careers, for example:

- AI researchers
- software engineers
- engineering managers
- program managers
- architects
- research engineers
- open-source maintainers
- technical writers or speakers
- senior ICs moving into management
- managers with deep technical history
- researchers with strong engineering output

## Basic idea

The prompt does not treat a person as a single job title. It treats them as a trajectory.

That means looking at:

- role changes over time
- recurring practice areas
- technical and non-technical artifacts
- feedback or review patterns
- public reception
- narrative coherence

This is the central point of the prompt. The goal is not to decide whether somebody is "really" an engineer or a manager or a researcher. The goal is to see how those parts connect.

## Starting point

The prompt starts from a person’s name.

Example:

```text
Materials:

[James Bond]
use above name to search stuff.
```

In other words, the model begins with the name, gathers relevant public material, and then produces a full review.

## What material may be used

Depending on what is available, the model may draw from sources such as:

- LinkedIn
- personal website
- CV or resume
- publication lists
- Google Scholar, DBLP, arXiv, or OpenReview
- GitHub or Hugging Face
- talks, slides, and interviews
- blog posts
- project pages
- official employer, lab, or conference pages
- public feedback or review text

## Output structure

The prompt is designed to produce a report with sections such as:

1. Executive Summary
2. Current Signal
3. Composite Identity
4. Role Timeline and Practice Threads
5. Evidence Assessment
6. Feedback and Reception Patterns
7. Narrative Coherence
8. Enduring Strengths
9. Underused Assets
10. Contradictions and Signal Gaps
11. Highest-Leverage Improvements
12. Repositioning Suggestions
13. Suggested Future Positioning
14. 30-60-180 Day Improvement Plan
15. Evidence Appendix

That structure is deliberate. It separates diagnosis from advice, and it keeps evidence close to the claims.

## Good use cases

This prompt is useful when you want to:

- review your own public profile
- understand how your career reads from the outside
- see whether your website, LinkedIn, papers, and repos support the same story
- find technical or research strengths that are getting buried
- check whether a mixed background reads as differentiated or confused
- prepare for a role transition
- sharpen positioning for Staff, Principal, EM, Architect, Research Engineer, or similar roles

## Example use

A minimal usage pattern looks like this:

```text
You are a professional trajectory intelligence analyst.

[full prompt here]

Materials:

[James Bond]
use above name to search stuff.
```

Replace the name with the person you want to analyze.

## Why this is different from a generic career prompt

Most career prompts do one narrow thing. They summarize a resume, rewrite a LinkedIn profile, produce generic advice, or hand out praise with little evidence.

This prompt is trying to do something harder. It treats professional identity as a synthesis problem. The model has to piece together visible evidence, interpret recurring themes, detect gaps, and decide whether the overall story makes sense.

That makes it more useful for people whose careers cut across research, engineering, management, architecture, or writing.

## Working assumptions

The prompt is built on a few assumptions.

First, people are usually more complex than their current title.

Second, mixed identities are common at senior levels.

Third, public signal matters. However strong someone is internally, they are often judged by what can be found and understood externally.

Fourth, contradictions are not noise. If one source says manager and another shows deep builder or researcher evidence, that is useful information.

Fifth, the point is not praise. The point is to make the strongest truthful story easier to see.

## Suggested workflow

A practical way to use the prompt is:

1. Choose the person.
2. Start with their name in the `Materials` section.
3. Run the prompt in GPT or Claude.
4. Read the report.
5. Follow up with narrower prompts for specific rewrites or comparisons.

Useful follow-ups include:

- turning the report into a short positioning memo
- writing LinkedIn headline options
- drafting a homepage headline and bio
- comparing fit for Staff vs Principal vs EM vs Architect
- identifying the most under-signaled strengths
- suggesting what to add to a website or portfolio

## Example follow-up prompts

### Condense to a short memo

```text
Condense the report into a one-page professional positioning memo.
Preserve the main evidence, the key contradictions, and the highest-leverage improvement path.
```

### Write LinkedIn positioning

```text
Based on the report, write five LinkedIn headline options, one About section, and one short positioning statement.
```

### Write website framing

```text
Based on the report, suggest a homepage headline, short bio, selected work structure, and framing for research, engineering, and leadership.
```

### Compare future role fit

```text
Based on the report, compare this person's fit for Staff Engineer, Principal Engineer, Engineering Manager, Research Engineer, and Architect. Be explicit about why.
```

## Limits

This prompt is only as good as the material the model can find and interpret.

Public information may be incomplete, stale, or uneven in quality. Private impact may not show up. Some people have rich external evidence; others do not. Name-based discovery also requires judgment, especially if multiple people have similar names.

So the output should be treated as a serious analytical synthesis, not as a perfect biography.

## Repository layout

A simple layout for the repository:

```text
professional-trajectory-intelligence-prompt/
├── README.md
├── prompt.md
├── examples/
│   ├── example-followups.md
│   └── names-to-analyze.md
└── LICENSE
```

## Suggested files

### `prompt.md`

Store the main prompt here.

### `examples/example-followups.md`

Store follow-up prompts for things like:

- website rewrite
- LinkedIn rewrite
- resume summary rewrite
- role-fit comparison
- short memo generation

### `examples/names-to-analyze.md`

Store simple example inputs that begin with a name.

Example:

```text
Materials:

[James Bond]
use above name to search stuff.
```

## Good fit for this prompt

This prompt is a good fit when the person:

- has worked across more than one role family
- has a visible public technical or research footprint
- wants sharper career positioning
- has a broad background that is hard to summarize cleanly
- is preparing for a transition or promotion
- wants an outside-in reading of their visible professional story

## License

MIT

## Summary

This repository contains a prompt for doing a full professional review starting from a person’s name.

It is designed for multidimensional careers. Instead of reducing someone to a title, it tries to recover the structure of their work, the consistency of their story, and the strongest direction for improvement.
