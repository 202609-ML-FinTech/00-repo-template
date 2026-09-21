# Student repository — Machine Learning & FinTech (115-1)

Template for your personal course repository.
Course information, slides and exercises: [202609-ML-FinTech/00-course-info](https://github.com/202609-ML-FinTech/00-course-info)

Your repository is **private**. Only you and the teaching team can see it.

---

## Where things go

```
homework/<mmdd>/              one folder per homework, named by the date it was assigned
in-class-exercise/<mmdd>/     one folder per class
replicating-a-paper/
    data/rawdata/             the data exactly as you downloaded it — never edit these files
    data/processed-data/      what your code produces from rawdata
    coding/                   notebooks and scripts
    _snapshots/               a dated PDF of your report at each milestone
```

Create the next dated folder yourself when work is assigned. Keep the names as
`mmdd` (e.g. `1005`), so the folders sort in order.

---

## Deadlines

| Work | Due |
|---|---|
| In-class exercise | Day of class, **12:10** |
| Homework | 7 days after it is assigned, **23:59** |

Push before the deadline. **The commit timestamp is the submission time** — a file
saved on your laptop but not pushed has not been submitted.

### Individual project milestones

| | What | Due |
|---|---|---|
| R1 | Topic: the paper, its motivation, why it interests you | Mon **10/05**, 23:59 |
| R2 | Data | Mon **10/19**, 23:59 |
| R3 | Benchmark model and experiment design | Mon **11/09**, 23:59 |
| R4 | Empirical analysis and conclusion | Mon **11/30**, 23:59 |

Each milestone is presented in class and written up in your report. Keep a PDF of
the report as it stood at each milestone in `_snapshots/`, named `R1.pdf`, `R2.pdf`
and so on, so your progress is visible.

---

## Working rules

**Raw data is immutable.** Anything in `data/rawdata/` stays exactly as downloaded.
Every change happens in code, writing to `data/processed-data/`. This is what makes
your work reproducible: a reader can delete `processed-data/`, run your notebooks,
and get it back.

**Do not commit large files.** GitHub rejects anything over 100 MB and warns above
50 MB. If your raw data is larger, commit a small sample plus the script that
downloads the full file, and say so in your report.

**Restart & Run All before you push.** A notebook that only runs in the order you
happened to click is not reproducible. Check it runs top to bottom in a fresh kernel.

**Commit as you work**, not once at the deadline. Small commits with plain messages
("add data cleaning", "fix scaling bug") are easier to recover from than one large one.

**AI tools are allowed**, and you do not need to hide it. What is graded is your
judgement — whether you checked the output, noticed what was wrong, and can defend
the decision when asked in class. Code an AI wrote that you cannot explain will not
earn marks.

---

## Getting started

```bash
git clone https://github.com/202609-ML-FinTech/<your-repo-name>.git
cd <your-repo-name>
```

Then, each time you work:

```bash
git add .
git commit -m "what you did"
git push
```

If `git push` is rejected, run `git pull` first, then push again.
