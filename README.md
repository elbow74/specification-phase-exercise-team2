# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

Sai Shettar ([https://github.com/saishettar](https://github.com/saishettar)), Elton Yu ([https://github.com/elbow74](https://github.com/elbow74)), Marco Gulino (https://github.com/MarcoHGulino)


## Review of the Current Application

1. **Weakness** — The AI often fails to detect when the speaker switches subjects mid-sentence. Example: "I like cats, some people prefer dogs because they're a 'man's best friend'" gets written as "Cats are a 'man's best friend'."
2. **Gap** — No undo (Ctrl+Z) after the AI refines a slide; there's no way to recover the original wording if the change is worse.
3. **Weakness** — Editing Seed Notes in settings kicks focus out of the text box after about a second of not typing, interrupting the flow of writing notes.
4. **Weakness** — Content sometimes bleeds from one slide into the next, producing a redundant bullet point on the current slide.
5. **Weakness** — The exit-ticket quiz doesn't always translate well from the slide material; some answers don't fit their question, others are too obvious to test anything.
6. **Strength** — Import/export supports multiple file types, including importing slide themes that aren't built into the app by default.
7. **Strength** — The translation feature is fast, easy to find (not buried in settings), and can translate the whole interface, not just the slide content.
8. **Strength** — AI customization is in-depth: users can tune how much the system infers versus sticks to the transcript, how much content lands on one slide, and how layouts adapt to the current topic.
9. **Gap** — Users cannot add their own images; only the AI selects and places images.
10. **Gap** — No direct way to share a single slide via a link.

## Prior Art & Originality

We checked the project's roadmap, Future Work, Open Questions, and open GitHub issues and
pull requests for anything covering manual image or text placement on a slide. The
whiteboard tab currently only supports drawing (pen, highlighter, eraser); adding a user's
own image or typed text there isn't specified, scheduled, or proposed elsewhere. The
closest existing feature, seed images, uploads pictures before a lecture to guide AI
generation, a different mechanism than placing a specific image or text on a specific slide
by hand. Our own testing of the live app confirmed this gap independently. What's original
to our proposal is manual image and text placement in the whiteboard tab; what's reused is
the whiteboard's existing rule that content can't shift under what's already there, we
extend that same guarantee to manually added elements.

## Stakeholders

See instructions. Delete this line and replace with the name(s) of the stakeholder(s) you interviewed and lists showing their goals/needs, and problems/frustrations. Note which type of user each stakeholder represents. You may use pseudonyms or partial names to maintain their privacy, but you must privately share their full names and contact information as part of your submission of this exercise

### Students:

**G.C (Student, Student Gov’t Member)**
1. **Goals & Needs (Before Testing):**
  a. Clear instructions on assignments\
  b. Appease constituents in student gov’t\
  c. Ensure appropriate work-life balance\
  d. Short but descriptive notes for optimal studying\
2. **Problems & Frustrations (Before Testing):**
  a. Easy access to frequently used tools; currently frustrated with lack of convenience in NYU software\
  b. Slides that include all relevant information professors cover\
  c. Stress with schoolwork\
  d. Not enough time to comfortably complete assignments\
3. **Goals & Needs (After Testing, Relating to App):**
  a. Talk about a topic of choice (fantasy animals), make comparisons to a different topic, and have the slide generate those distinctions properly (successful)\
  b. Highlight specific portions of her speech (successful)\
4. **Problems & Frustrations (After Testing, Relating to App):**
  a. False assumption that playing the recorded audio would start from the beginning, instead of at the slide she’s currently on\
  b. Exit quiz asked questions unrelated to the presentation's content, instead asking about what the lecturer asked the Slide Machine to do (for example, “What photos did the speaker ask for?”)\
  c. Couldn’t add a Venn diagram image or change background color. Wished there was a quicker and easier way of adding these basic features\
  d. Slide bullet points were unspecific and sometimes incorrect\
  e. Slide titles were not always topic specific (for example, presenter began talking about unicorns as the national animal of Ireland, but moved to talking about unicorns/pegasi/leprechauns overall. But the first slide is titled “Facts about Ireland.”)\
  f. Trying to correct the slide as she goes, unsuccessfully, just adds on more information rather than correcting mistakes\

## Product Vision Statement

Our proposal adds manual content controls to The Slide Machine’s whiteboard tab, letting instructors and other presenters place their own images and their own typed text directly onto a slide, instead of being limited to what the tool draws or generates on its own.

## User Requirements

See instructions. Delete this line and place a list of your User Stories here, grouped by type of user. These should describe functionality that is new or changed, not functionality the app already has.

## Activity Diagrams

See instructions. Delete this line and place images of your UML Activity diagrams here, each with the text of the user story it illustrates.

## Wireframes

See instructions. Delete this line and place your wireframe diagrams here, covering every new screen and every existing screen your proposal changes, for every type of user.

## Clickable Prototype

See instructions. Delete this line and place a publicly-accessible link to your clickable prototype here.

## Stakeholder Demo

See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
