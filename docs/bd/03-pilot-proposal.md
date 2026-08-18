# Canva/Pexels pilot proposal

## Goal

Validate whether a retrieval-first layer can:

- reduce unnecessary generation requests
- increase reuse of existing assets
- strengthen the enterprise asset workflow

## Pilot thesis

Many prompts that look like generation requests are actually attempts to find or
adapt assets that already exist.

If the platform can identify a suitable existing asset quickly enough, it can:

- satisfy more requests without invoking generation
- reduce compute spend on avoidable AI calls
- improve reuse of customer-owned and Canva-owned libraries

## Pilot shape

Run the engine against a narrow, representative content slice that includes:

- a curated set of Pexels assets
- a customer-like enterprise asset library
- optional associated metadata, tags, campaign folders, and documents

The pilot should be limited enough to evaluate quickly but broad enough to test
real retrieval behavior across different request types.

## Example corpus

A practical pilot corpus could include:

- 10,000 to 50,000 image and video assets from a selected Pexels subset
- a sample brand library with logos, product imagery, campaign files, templates,
  and supporting documents
- a prompt set derived from realistic design or asset search workflows

## Test scenarios

Measure the product against scenarios such as:

1. "Find me something like the hero image from our summer campaign."
2. "Give me an approved product image for a social post about [theme]."
3. "Suggest an asset that matches our brand look before generating a new one."
4. "Find a Pexels asset we can use that looks like our existing campaign style."
5. "Search for the best existing asset across our library and Canva-owned stock."

## Success metrics

### Primary metrics

- **retrieval hit rate**: how often the system finds an acceptable existing asset
  before generation is needed
- **avoided generation rate**: percentage of requests that would otherwise have
  triggered generation but can be satisfied with an existing asset
- **asset reuse rate**: increase in reuse of customer-owned or Canva-owned assets

### Secondary metrics

- time to satisfactory first result
- query-to-selection conversion rate
- search refinement count before a usable asset is found
- satisfaction score from internal evaluators or pilot users

### Economic metrics

- estimated avoided generation calls
- estimated reduction in AI inference spend for tested workflows
- increased utilization of existing owned or uploaded inventory

## Evaluation method

For each prompt in the test set:

1. run the current or baseline workflow
2. run the retrieval-first workflow
3. record whether an acceptable asset was found without generation
4. record latency, quality, and any generation that still occurred

At the end of the pilot, summarize:

- where retrieval-first clearly wins
- where generation remains necessary
- what classes of request are best suited to the engine

## Recommended deliverable to Canva

Offer a short proof, not a broad technical integration.

Suggested framing:

> We would love to run a small proof on a representative content slice and show
> where an existing asset could satisfy the request before generation.

## Commercial paths if the pilot works

If the pilot is positive, the next step could be one of:

- infrastructure licensing
- native embedding in Canva workflows
- an enterprise retrieval feature or premium add-on
- deeper strategic partnership discussions

Do not lead with acquisition or a large strategic process. Lead with measurable
proof.
