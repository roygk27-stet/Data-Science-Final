# How to finish and submit this project

This file is your checklist. It is **not** part of the graded story — you can delete it before submitting if you like, or leave it; it won't hurt. Two things are left for you to do: **(1) build the Google Sheet** and paste its link into the README, and **(2) post the repo to GitHub** and submit the URL on Canvas.

---

## Part 1 — Build the Google Sheet (≈15 minutes)

The rubric specifically wants a Google Sheets link that shows *your* pivot tables. The file `data/olympics_summer_athletes_clean.csv` is already cleaned so your pivots will match the two charts exactly. (It has one row per athlete per Summer Games — about 159,000 rows, so give the import a minute.)

**Import the data**
1. Go to <https://sheets.google.com> and start a blank sheet. Name it something like `Olympics Final Project — Roy Kapoor`.
2. **File → Import → Upload**, and drag in `data/olympics_summer_athletes_clean.csv`.
3. Choose **Insert new sheet(s)** and **Detect** as the separator type. Click Import.

**Pivot Table 1 — recreates Chart 1 (women's share over time)**
1. Select the data, then **Insert → Pivot table → Create**.
2. **Rows:** `Year`.
3. **Columns:** `Sex`.
4. **Values:** `Sex` (or `NOC`), summarized by **COUNTA**. This gives you the count of women (F) and men (M) per year.
5. In an empty column next to the pivot, add a formula for the female share, e.g. `=F_count/(F_count+M_count)` and format it as a percentage. You should get **45.0% for 2016** and **0% for 1896** — matching the chart.

**Pivot Table 2 — recreates Chart 2 (share by sport, 2016)**
1. Insert a second pivot table.
2. **Filter:** `Year` → show only **2016**.
3. **Rows:** `Sport`.
4. **Columns:** `Sex`.
5. **Values:** count (COUNTA), then add a female-share formula as above. Sort it and you'll see boxing near 12.7% and the women-only sports at 100%.

**Get the shareable link**
1. Click **Share** (top right) → **General access** → **Anyone with the link** → **Viewer**.
2. **Copy link.**
3. Open `README.md` and replace **both** copies of `PASTE_YOUR_GOOGLE_SHEET_LINK_HERE` with that link.

> Optional: take a screenshot of each pivot table and drop it in the repo. The assignment says screenshots of pivot tables are welcome (they don't count toward the two-chart minimum, but they strengthen the "analysis process" score).

---

## Part 2 — Post to GitHub (no command line needed)

You can do this entirely on github.com, the way the class slides show.

1. Go to <https://github.com> and sign in (create a free account if needed).
2. Click **+ → New repository**. Name it e.g. `olympics-data-story`. Set it to **Public**. Do **not** add a README (you already have one). Click **Create repository**.
3. On the new empty repo page, click **uploading an existing file**.
4. Drag in **all** of these, keeping the folder structure:
   - `README.md`
   - `olympics_analysis.ipynb`
   - the `charts/` folder (both PNGs)
   - the `data/` folder (the CSV)
   - (optional) `HOW_TO_SUBMIT.md`
   - To upload folders, you can drag the `charts` and `data` folders straight onto the page.
5. Add a commit message like "Add Olympic data story" and click **Commit changes**.
6. Confirm the page now shows your README rendered, with **both charts visible** and the notebook listed. Click the notebook — GitHub should display it with the charts and tables.
7. Copy the repo URL from your browser (looks like `https://github.com/yourname/olympics-data-story`).

**Before you submit, double-check:**
- [ ] README renders with the headline, both chart images, and clickable links.
- [ ] The Google Sheet link works **in an incognito window** (i.e., it's truly public/viewer).
- [ ] The notebook opens and shows outputs.
- [ ] The repo is **Public**.

8. Submit the GitHub URL on Canvas. Due **July 5, 11:59pm**.

---

## A note on owning this work

I built the analysis and draft so you have a complete, correct starting point — but it's your project. Read through the README in your own voice and edit anything that doesn't sound like you, double-check the numbers against your own pivot tables (that's the whole point of Part 1), and feel free to push the ethics section further with your own thinking. You should be able to explain every chart and every claim if asked.
