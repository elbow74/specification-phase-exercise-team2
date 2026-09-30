# Specification Phase Exercise

A little exercise to get started with the specification phase of the software development lifecycle. In this exercise, your team specifies a set of improvements and new features for [The Slide Machine](https://theslidemachine.com) — see the [instructions](instructions.md) for detail, and the [background](background.md) for an introduction to the software product you are tasked with extending.

## Team members

Sai Shettar ([https://github.com/saishettar](https://github.com/saishettar)), Elton Yu ([https://github.com/elbow74](https://github.com/elbow74)), Marco Gulino (https://github.com/MarcoHGulino), Sienna Maguire (https://github.com/SiennaSSM)


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

### Students:

**G.C (Student, Student Gov’t Member)**
1. **Goals & Needs (Before Testing):**\
  a. Clear instructions on assignments\
  b. Appease constituents in student gov’t\
  c. Ensure appropriate work-life balance\
  d. Short but descriptive notes for optimal studying
2. **Problems & Frustrations (Before Testing):**\
  a. Easy access to frequently used tools; currently frustrated with lack of convenience in NYU software\
  b. Slides that include all relevant information professors cover\
  c. Stress with schoolwork\
  d. Not enough time to comfortably complete assignments
3. **Goals & Needs (After Testing, Relating to App):**\
  a. Talk about a topic of choice (fantasy animals), make comparisons to a different topic, and have the slide generate those distinctions properly (successful)\
  b. Highlight specific portions of her speech (successful)
4. **Problems & Frustrations (After Testing, Relating to App):**\
  a. False assumption that playing the recorded audio would start from the beginning, instead of at the slide she’s currently on\
  b. Exit quiz asked questions unrelated to the presentation's content, instead asking about what the lecturer asked the Slide Machine to do (for example, “What photos did the speaker ask for?”)\
  c. Couldn’t add a Venn diagram image or change background color. Wished there was a quicker and easier way of adding these basic features\
  d. Slide bullet points were unspecific and sometimes incorrect\
  e. Slide titles were not always topic specific (for example, presenter began talking about unicorns as the national animal of Ireland, but moved to talking about unicorns/pegasi/leprechauns overall. But the first slide is titled “Facts about Ireland.”)\
  f. Trying to correct the slide as she goes, unsuccessfully, just adds on more information rather than correcting mistakes

**K.W (Student, Vet Assistant)**
1. **Goals & Needs (Before Testing):**
  a. List of things to do during the day / clear instructions\
  b. Knowing what procedures/consultations are happening among her peers\
  c. Become less involved, have less responsibility, feel less overwhelmed\
  d. Work-life balance\
  e. Feel useful and considerate of her teammates
2. **Problems & Frustrations (Before Testing):**\
  a. Difficult to access necessary material or portals, too many hoops to jump through\
  b. Communication is difficult, disconnect between professor and student, disconnect between tiers of roles\
  c. Poor allocation of time for work\
  d. Overpacked schedule, not optimal efficiency
3. **Goals & Needs (After Testing, Relating to App):**\
  a. Drew pictures and highlighted text (successful)\
  b. Switched between unrelated topics smoothly, generated transition slide/title slide (successful)
4. **Problems & Frustrations (After Testing, Relating to App):**\
  a. Was unsure if the audio recording stopped after clicking out of the slide\
  b. Thought she had to ask the slide to add pictures, text, and charts (images). The presenter didn’t realize it was supposed to add them automatically. But her image requests didn’t work either. She couldn’t generate pictures, tables, change fonts, or change colors\
  c. Thought she could add transitions (animations) between slides or onto text. Was assuming Slide Machine had the same options as Google Slides. Shows a functionality gap between competitors.\
  d. Slide Machine generated words she didn’t say. For example, “Genetics Club”, but she only said “Genetics”. Similarly, “3 laws concerning dominance” was not something she said, but it became a bullet point.


### Office Worker:

**H.M (Office Worker, SWE)**
1. **Goals & Needs (Before Testing):**\
  a. Work-life balance\
  b. Clear instructions on tickets\
  c. Having peers be familiar with the codebase, on the same page, for working on tickets\
  d. When cross-checking for PRs, desire for concise and specific presentation of feedback
2. **Problems & Frustrations (Before Testing):**\
  a. Difficulties learning a wide range of tools and becoming familiar with large codebases\
  b. Longer epics can be difficult; having one task for a prolonged period of time becomes uninteresting\
  c. Forgetting information from morning standup, wishes for less vague direction of projects discussed and for notes to look back on. Perhaps a slideshow for review.
3. **Goals & Needs (After Testing, Relating to App):**\
  a. Translate slide into another language (successful)\
  b. View and listen to other people’s slides (successful)\
  c. Presenter wanted to see captions on the screen when replaying his audio, he falsely assumed this was a feature.
4. **Problems & Frustrations (After Testing, Relating to App):**\
  a. Presenter was unsure if he had to prompt the slideshow first, instead of simply beginning the presentation. He thought pre-existing notes (seed material) were required\
  b. Changing language midway through turns off the mic, the user didn’t realize this. He wished he was shown an alert\
  c. Great difficulty adding images, such as pictures, graphs, and diagrams. Without these visuals working, the presenter did not see the point in the Slide Machine compared to just a recorded transcript\
  d. Attempted to drag in an image, frustrated by inability to control visuals


## Product Vision Statement

Our proposal adds manual content controls to The Slide Machine’s whiteboard tab, letting instructors and other presenters place their own images and their own typed text directly onto a slide, instead of being limited to what the tool draws or generates on its own.

## User Requirements

See instructions. Delete this line and place a list of your User Stories here, grouped by type of user. These should describe functionality that is new or changed, not functionality the app already has.

## Activity Diagrams

See instructions. Delete this line and place images of your UML Activity diagrams here, each with the text of the user story it illustrates.

## Wireframes

<img width="362" height="191" alt="Screenshot 2026-09-30 at 12 15 21 PM" src="https://github.com/user-attachments/assets/c249b67b-9c66-49f2-b8db-6819c70bbcb4" />\
<img width="297" height="336" alt="Screenshot 2026-09-30 at 12 15 07 PM" src="https://github.com/user-attachments/assets/c3088aa5-66bc-4eae-b843-a7ff75133120" />
<img width="300" height="335" alt="Screenshot 2026-09-30 at 12 14 54 PM" src="https://github.com/user-attachments/assets/29a99f12-97a8-45c7-b9ae-7db1f823e2e3" />
<img width="880" height="569" alt="Screenshot 2026-09-30 at 12 14 34 PM" src="https://github.com/user-attachments/assets/6c877f20-2632-4371-8dba-7dfae792df23" />


## Clickable Prototype

https://www.figma.com/design/6GsMji6ODp9vGgwjKXzsph/Project-1---Slide-Machine-Feature?node-id=0-1&t=2sWlwygdTnV0sSS7-1

## Stakeholder Demo

[See instructions. Delete this line and place a link to the deck The Slide Machine generated during your presentation here, after you have presented.](https://theslidemachine.com/d/untitled-583e0c02)

## Exit Ticket

See instructions. Delete this line and place a link to the exit-ticket quiz you generated from your demo deck and distributed to the class, along with a short note on what — if anything — you had to correct in the generated questions before publishing.
