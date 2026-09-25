# Add `growth.community_question_radar`

## What this workflow does

`growth.community_question_radar` finds fresh, public conversations where a company's target
buyer is already asking about a problem the company's product can genuinely help solve. It
turns the strongest conversations into a small posting queue: URL, evidence, fit score, a
ready-to-edit helpful reply, and a clear next action for the founder.

The workflow is deliberately about conversations rather than channels. It does not tell a
founder "do Reddit" or "post on LinkedIn"; it identifies the actual question worth answering
and gives the founder something useful to do next.

## Who would run it

A small-company founder or growth operator would run it on demand when they want a lightweight
community acquisition pass, especially after a launch, new feature, change in positioning, or
before starting a new acquisition push.

## Why it is missing today

Tin already covers SEO/organic visibility, keyword planning, content production, cold email
shortlists, speaking opportunities, campus events, marketplace listings, and other outbound
paths. Those workflows can identify channels, pages, or contacts, but this workflow starts
from a different unit: a live buyer question in a public conversation where the company can
contribute immediately.

It also deliberately stops before the external action. The founder gets the evidence and draft,
then decides whether and how to post.

## How it works

1. Read the existing project context so the agent knows the buyer, actual product capabilities,
   writing style, and constraints.
2. Convert product problems into buyer-language search hooks.
3. Search several public discussion surfaces for fresh questions.
4. Capture the URL, question, date/freshness, buyer evidence, and posting viability.
5. Score candidates on intent, product fit, freshness, and helpfulness.
6. Keep only strong candidates and draft a 60-120 word answer that is useful without requiring
   a product pitch.
7. Produce `reports/COMMUNITY_QUESTION_RADAR.md` with a prioritized posting queue, evidence,
   drafts, near-misses, and limitations.

The workflow never posts, comments, sends messages, creates accounts, or fabricates customer
proof.

## Where the idea came from

The idea is based on the principle that community marketing works through participation and
useful answers rather than broadcasting. HubSpot's 2026 community-marketing guidance emphasizes
meeting audiences where they already participate, observing what customers are talking about,
and using specific problems as the basis for community activity. It also distinguishes
participation and conversation from generic social-media distribution.

Source:
https://blog.hubspot.com/marketing/community-marketing

The Tin-specific design choice is to operationalize that idea as a repeatable "find the
question -> qualify it -> draft the answer -> hand off to founder" workflow, rather than as
generic advice to be active in communities.

## Testing

The package includes a qualification case file covering an ordinary result, a thin-search
result, and a no-fit boundary. Static validation should be run with:

    uv sync --frozen
    uv run tin-lite validate-community

The package is on-demand and writes only the declared report artifact. No external publishing
action is performed by the workflow.
