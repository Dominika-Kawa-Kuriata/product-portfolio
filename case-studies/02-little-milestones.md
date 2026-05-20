# Little Milestones

A parent companion app prototype built with Figma Make and v0, using prompting only on free tiers. The point was not to ship a product, but to compare two AI prototyping tools across a real product brief plus reflect on what each does well.

## The problem

I wanted an honest stress-test of AI prototyping tools as a product person. The marketing around these tools shows polished demos. I wanted to know what happens when you treat them as discovery instruments: how quickly can they get from a problem to something testable, and where do they break.

I picked a brief I understood well from direct experience: a companion app for parents tracking child development by age. The domain was familiar enough that I could validate content quality against WHO developmental guidelines rather than guessing.

## What I built

Two working prototypes of the same concept, one in Figma Make, one in v0. Same prompt structure, same target user, same content scope: developmental milestones month-by-month with simple parent-facing guidance.

I worked entirely through prompting, no manual UI edits, no custom code. Free tiers only. The goal was to see what each tool produces if you treat it as a design partner rather than a paintbrush.

## What I compared

**Design quality out of the box.** Figma Make produced cleaner visual hierarchy from the first prompt, with sensible default typography plus spacing. v0 needed more iterations to get the visual language right but gave me cleaner component structure underneath.

**Structural control.** v0 made it easier to think in components plus reuse patterns across screens. Figma Make defaulted to “this is one screen”, which meant I had to be more explicit about reusing patterns in prompts.

**User flow trade-offs.** When I tried to simplify the flow (fewer taps to get to the daily milestone view), Figma Make handled the visual reflow well but lost some structural consistency. v0 kept structure but needed more careful prompting on the visual side.

**Content validation.** Both tools generated placeholder content that sounded plausible but was developmentally inaccurate when checked against WHO guidelines. The takeaway: AI prototyping tools are good at structure and visual scaffolding, not at domain-specific content. That has to come from a verified source or a domain expert.

## What I learned

**Design-first vs structure-first is a real trade-off, not just a tooling preference.** If you’re prototyping to test visual concepts with users, Figma Make gets you there faster. If you’re prototyping to test flows plus component logic, v0 is the better starting point. The choice depends on what hypothesis you’re testing, not which tool is “better”.

**Prompting is a product skill, not a technical one.** The quality difference between my first prompts and my fifth was bigger than the difference between the two tools. Specifying user state, success criteria plus what NOT to include produced better outputs faster than describing the screen visually.

**Validation has to be built in from the start.** Both tools confidently produced plausible-looking developmental content that didn’t match WHO guidance. Without a quick cross-check against the WHO source, the prototypes would have looked credible while being wrong. This generalises: any AI prototype targeting a domain needs a domain check before user testing.

## The sneakers analogy

When I shared this on LinkedIn, I framed the user mindset using a running analogy. A parent opening a developmental milestone app is in a similar mindset to a runner picking shoes for a long run: low tolerance for friction, high tolerance for paying for quality, looking for something that disappears into the activity rather than demanding attention. That framing shifted my design decisions toward fewer screens, less branding, more “get in, get out”.

## Outcome

Two working prototypes, a public LinkedIn post that generated engagement plus discussion with other product people, plus a clearer personal framework for when to reach for which AI prototyping tool. The artefacts themselves are less interesting than the process plus reflection — which is the point.
