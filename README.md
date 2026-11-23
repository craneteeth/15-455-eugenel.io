# Grover's Algorithm — CS455 GitHub Pages site

A static, multi-page learning site built around **CS455 Lectures 7–9** and the provided **Reductions & Completeness** notes. Written in English for a CS455 audience. The structure follows the project's rubric: course context, substantial theorem proofs, precise statements, intuition, and clear navigation.

## Open the site

The homepage is `index.html`. It links to:

- `lecture1.html`: course-to-vector translation, unstructured search, Grover iteration, rotation lemma, the exact success-probability formula, examples, and upper bound.
- `lecture2.html`: the BQP complexity class, quantum search for NP, the **BBBV Ω(√N) query lower bound** with a complete hybrid proof, and oracle consequences. The lower-bound theorem is the centerpiece.
- `reference.html`: generated index of results, notation, course sources and research references.

Interactive amplitude, rotation, success-probability, and lower-bound visualizations work without a backend. Proofs collapse, cross-references have hover previews, and a responsive contents panel helps navigation.

### Publish on GitHub Pages

1. Make a **public** GitHub repository, for example `grover-cs455`.
2. Upload **all the contents of this folder** into the repository root, including `.nojekyll`. In particular, `index.html` should be at the root; do **not** upload only the zip file.
3. Under the GitHub repository's **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. The site will appear at `https://YOUR-USERNAME.github.io/grover-cs455/` (replace both placeholders).

If you prefer Git commands:

```bash
git init
git add .
git commit -m "Create CS455 Grover's algorithm site"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/grover-cs455.git
git push -u origin main
```

Create the empty repository first; the `remote` command alone does not create it. In GitHub's Settings → Pages, enable branch deployment after the push.

### Local preview

```bash
python3 -m http.server 8000
```

Open `http://localhost:8000/`. `reference.html` needs HTTP(S) because it loads page metadata for the index. Open every page using the local server rather than `file://` for the full navigation experience.

### Dependencies

The site's JavaScript and KaTeX rendering engine are bundled in `assets/`. **KaTeX math fonts are loaded at runtime from jsDelivr** instead of being included in the archive. The page therefore needs an internet connection for properly typeset equations. Body text uses system fonts. No build process, Node package installation, or server-side programming is required.

### Course and research sources

- Lecture 7: Bias-Busting (quantum instructions, amplitudes and Hadamard normalization)
- Lecture 8: The Hadamard Transform (XOR sign patterns)
- Lecture 9: Grover's Algorithm I (ReflectAcrossAverage and Unique-SAT)
- CS455, Reductions & Completeness 1 (why conditional lower bounds matter)
- Cited literature for material **beyond** the attached lectures: Grover (1996), Bennett et al. (1997), Boyer et al. (1998), Zalka (1999), and others, all listed in `reference.html`.

### Before coursework submission

- **Add your own name** to the metadata in `index.html`, `lecture1.html`, and `lecture2.html`, if required by the instructor.
- Read the centerpiece BBBV proof carefully enough to explain the hybrid argument and why the conclusion concerns **queries**, not SAT's unconditional running time.
- Review the `Acknowledgements` on `index.html` for consistency with your course policy.
- Open all the pages, click the interactive figures, and verify internal references.

This project includes JavaScript and source files; editing the text requires only an ordinary code editor. The **ZIP is a ready-to-publish source package**, not a link to an already deployed GitHub site.
