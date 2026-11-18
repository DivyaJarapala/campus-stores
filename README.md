# Campus Stores

## My submission: what to review

- **Prototype:** open `index.html` and play the shift. The change is in the **Loan register** (`app.js`, plus small additions to `styles.css` and `index.html`).
- **Screenshots:** [`docs/friday-update-holder.png`](docs/friday-update-holder.png) and [`docs/saturday-register.png`](docs/saturday-register.png).

### One moment the product handles well: issuing the kit at 3:45 pm

I opened RQ-214 and issued the projector, speaker and adapter to Kabir Sen on three separate slips. I then tried to add a wireless microphone to the same request, and the slip refused it ("outside the approved request"). The broken projector, PR-06, never appeared as an option. These guardrails stop the two most expensive counter mistakes, which are handing out unapproved kit and handing out broken kit, without the staff member having to remember anything. One slip per physical unit is also what makes a partial return possible later.

### One moment I would change: the partial return at 7:30 pm

Kabir returned the projector and speaker and said "Leela still has the adapter, she'll bring it at nine." I closed two slips, but the adapter slip still said **issued to Kabir, due Fri 8 pm**. The register had nowhere to record that Leela had the unit or when it was coming back, so I wrote a free-text note in the Desk book.

At 9 am the next shift had to piece together the Desk book note, the register and the inventory to work out which adapter was out, AD-12 or AD-15, both in bin C4. Leela's name was not on any loan record. The slip was overdue, but nothing said so. "Record return" closes a slip in one click with no undo, and Tara's microphone slip sits right next to it.

The real problem is that a key handover fact lived outside the record the morning shift actually acts on.

### My change: put the handover on the slip

1. **Update holder** on every open slip records who has the unit now and when it is expected back. The update also writes a dated entry to the Desk book automatically, so the history stays in one place.
2. **Partly returned callout** at the top of the register, for example: "RQ-214 · 2 of 3 units back. Still out: AD-12 (USB-C → HDMI adapter) with Leela Das." If no holder has been recorded it says "holder not confirmed", which nudges the Friday shift to record one.
3. **Slips show the item type** (e.g. "AD-12 · USB-C → HDMI adapter") and **Overdue / Due now** tags based on desk time. The inventory shows who has each unit on loan.
4. **Undo return** in the status bar after a return, in case the wrong slip is closed.

**What I kept:** one slip per physical unit, the issue guardrails, the Desk book for genuinely free-form messages, and the existing layout and visual style. I added no new screens.

### The same job with the change

- **Fri 3:45 pm:** Unchanged. Issue three slips to Kabir.
- **Fri 7:30 pm:** Record return on the projector and speaker. The status bar and the callout say AD-12 is still out with "holder not confirmed". Click **Update holder** on L-404 and choose Leela Das, expected Sat 9 am. That takes one form, and there is no note to write.
- **Sat 9:00 am:** Open the Loan register. The top line reads "Still out: AD-12 … with Leela Das", and the slip shows **Due now · Now with Leela Das**. Check that the tag on her adapter says AD-12, then click Record return. If the wrong slip is closed, click Undo. The Desk book never has to be opened.

### One observation at a real counter

When the person returning a unit is not the person it was issued to, **does the morning staff member close the correct slip without opening the Desk book or asking a colleague, and how long does that take?** If they still go to the Desk book, or call the evening shift, the change did not help. I would also count how many slips stay "holder not confirmed" at close of shift. That number shows whether the evening shift is actually using Update holder.

---

Campus Stores is a Product Engineer work sample set at a fictional campus media equipment desk. Work through a club’s screening, from equipment pickup to a partial return and the next morning’s handover. Open **Candidate brief** in the app for the assignment.

## Run the app

Open `index.html` in a modern browser. The app includes its scripts, styles, and icons and can run offline.

To serve it over local HTTP, run this from the repository folder and visit `http://localhost:8000`.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Each browser stores its own sample shift locally when browser storage is available. **Restart sample shift** restores the fictional starting records.

## Source

- `index.html` contains the desk layout, candidate brief, and bundled icons.
- `app.js` contains the sample records and interactions.
- `styles.css` defines the desktop and mobile layouts.

Icon license notices are in [third-party/lucide-LICENSE.txt](third-party/lucide-LICENSE.txt).


## Submit your work

1. [Fork Campus Stores](https://github.com/virinchi-healthcare/campus-stores/fork) into your GitHub account. Complete the candidate brief and push your changes to your public fork. In your README, point reviewers to your work and explain the decision you made.
2. In your fork, open **Commits**, select the final commit you want reviewed, and copy the page URL. It should look like `https://github.com/YOUR-USERNAME/campus-stores/commit/COMMIT-SHA`.
3. [Submit your work through the Google Form](https://docs.google.com/forms/d/e/1FAIpQLScvzoh1R4WS-SkiwAVBQbMvniieJYSoOEfLMyVo5CyjOvYUgQ/viewform). Your **roll number**, **email ID**, and **final commit link from your public fork** are required. Enter your roll number and email ID in the form only.
