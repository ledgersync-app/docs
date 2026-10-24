# LedgerSync docs: how to edit them

This is the public LedgerSync docs site, https://docs.ledgersyncappv2.com. The person asking for changes is often
Maurice, the CEO. He is not technical. Talk to him in short, plain sentences, and never about files, git or code
unless he asks.

## Who reads these docs

- Accounting firm owners and staff: busy, often older, not technical.
- Each page answers one question, with one straight path. One action per step. Few words, short sentences.
- A picture or a short video is better than a paragraph.
- Never use em dashes or en dashes. Use a period or a comma instead.
- Only describe what LedgerSync really does. If you are not sure something is true, ask before you write it.

## Where things are

- `ai/`: the pages about using LedgerSync in Claude, ChatGPT or Grok. `guides/` and the top folder: the developer
  API docs.
- `docs.json` is the menu on the left. A new page only shows up after you add it there.
- Pictures go in `images/`, videos in `videos/`.
- The `ai/` pages use the parts in `snippets/ai-ui.jsx` (AiPage, AiStep, AiNote and the others). Copy how an existing
  page uses them, with the same props and quotes.
- Never edit `openapi.yaml` (a job replaces it every 6 hours) or anything in `.github/`.

## Asking him

- Ask one question at a time, and end your message with it. Never ask two questions in one message: a short "yes"
  must have only one meaning.
- Only publish what he clearly said yes to. If a reply could mean more than one thing, ask again.

## Publishing

- Work only on the branch the session started on. Never switch to `main`: the session saves your branch by itself,
  so anything left on `main` would go live without his yes.
- One change at a time. Publishing sends everything on your branch, so before you start a new change, settle the one
  that is waiting: publish it if he said yes, or undo it.
1. Make the change. Then tell him in plain words what will change, and ask: "Publish it?"
2. When he says yes (publish, go live, ship it), commit with a one-line plain message and no co-author lines, then
   run `git push origin HEAD:main`. No pull requests.
3. Tell him it will be live in about a minute, with the link to the page.
4. If he wants a change undone, revert that commit on your branch, ask "Publish the undo?", and push it the same way.
