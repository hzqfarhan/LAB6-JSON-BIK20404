# BIK20404 – Lab 06: Client-Side Scripting (JSON)

This is a complete solution to **Lab 06 - JSON.docx**, using the lecturer's `students.json` and `students.html` as references.

## Files

| File | Purpose |
| --- | --- |
| `books.json` | Q1: JSON collection with the two specified books. |
| `bookDetails.html` | Q2: Fetch the JSON asynchronously and print the first title, second author and all genres on screen and in Console. |
| `displayBook.html` | Q3: Asynchronous `fetch()` from GitHub, select a title and display its full book record. |

The JavaScript uses `async` / `await`, explicitly uses the `response` object, and **does not use nested `.then()` callbacks or nested loops**. The `Books` array and `genres` arrays are still present because the required JSON structure naturally contains objects and arrays.

## Step 1: Open files in VS Code

1. Extract the ZIP archive and open the `Lab06_JSON_Complete` folder in VS Code using **File > Open Folder**.
2. Check `books.json`: it contains both book records required in Q1.
3. Install **Live Server** in VS Code (if you don't have it).
4. Right-click `bookDetails.html` and select **Open with Live Server**. Note: `fetch()` usually cannot load local JSON when opened via a `file:///` address.

## Step 2: Verify Q2

1. In your browser, confirm four results are visible:
   - `(a) First book title: The Great Gatsby`
   - `(b) Second book author: Harper Lee`
   - `(c) Book 1 genres: Fiction, Classics`
   - `(c) Book 2 genres: Fiction, Coming-of-Age`
2. Press **F12 > Console** and verify these lines are printed there too.
3. Screenshot the webpage / Console and paste into your Word report if you need more evidence.

## Step 3: Test Q3 with LOCAL DATA (optional preview)

1. Right-click `displayBook.html` and select **Open with Live Server**.
2. Add `?preview=local` to its URL. Example: `http://127.0.0.1:5500/displayBook.html?preview=local`.
3. Select each title and check that its author, publication year and genres appear.
4. This mode is **only for preview**, not a submission demonstration of fetching from GitHub.

## Step 4: Upload your code to GitHub

1. Sign in at <https://github.com> and create a new **Public** repository (for example, `BIK20404-Lab06-JSON`). Use `main` as your branch name.
2. On your repository page, choose **Add file > Upload files**.
3. Upload `books.json`, `bookDetails.html`, and `displayBook.html`, then commit the files.
4. Your raw JSON URL will have this format:
   `https://raw.githubusercontent.com/YOUR_USERNAME/YOUR_REPOSITORY/main/books.json`
5. Edit the `GITHUB_JSON_URL` variable in `displayBook.html` to use your real GitHub username and repository name.
6. Upload/commit the updated `displayBook.html` again.
7. Open the raw JSON URL in a browser. You should see JSON content directly (not a GitHub HTML page).

**Use a `raw.githubusercontent.com` link for `fetch()`; do not use the normal GitHub `/blob/` link.** If your default branch is not `main`, change the URL accordingly.

## Step 5: Final Q3 GitHub test

1. Open `displayBook.html` via Live Server, **without** `?preview=local`.
2. You should see: `Successfully fetched 2 books from GitHub.`
3. Select **The Great Gatsby**, then **To Kill a Mockingbird**. Verify their records.
4. Capture screenshots of these **real GitHub-backed results** and replace/add them in your Word report. The included Q3 images are clearly labelled local previews, not proof of a live GitHub fetch.

## Step 6: Submission

1. Fill in your **name and matric number** in `Lab06_Answer_Report.docx`.
2. Paste the final GitHub-fetch screenshots into the Word report.
3. Submit the Word report plus source files in a ZIP via **Author** (per the lab instructions).
4. Submit the **GitHub repository URL** requested by Question 3.

## Troubleshooting

- `Error: Change GITHUB_JSON_URL...`: replace the placeholder URL with your actual raw link.
- `HTTP 404`: confirm the repo is public, the file is in its root folder, and the branch name and path are correct.
- `Failed to fetch`: use Live Server; verify internet access and the raw URL.
- No books in dropdown: press F12 > Console, check errors and confirm JSON uses `"Books"` with a capital `B`.

**Expected Q3 book details:**

- **The Great Gatsby** — F. Scott Fitzgerald, 1925, Fiction and Classics.
- **To Kill a Mockingbird** — Harper Lee, 1960, Fiction and Coming-of-Age.
