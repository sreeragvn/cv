# Sreerag V Naveenachandran — Online CV

Personal CV site for Applied ML / Data Scientist work.

Live: <https://sreeragvn.github.io/cv/>

## Local preview

```sh
docker compose up
```

Site is served at <http://localhost:4000/cv/>. Edit `_data/data.yml` to update content.

## Private CV PDFs

The CV and cover letter are built locally from the nested `resume/` repository:

```sh
cd resume
latexmk -xelatex resume.tex
latexmk -xelatex coverletter.tex
```

Both PDFs are written to `resume/build/` and are excluded from the website.

## Optional public document downloads

Keep the generated PDFs private by default. Once you have phone-free copies that you want
to publish:

1. Add the files as `assets/documents/resume.pdf` and/or
   `assets/documents/cover-letter.pdf`.
2. In `_data/data.yml`, uncomment the corresponding `resume_pdf` and/or
   `cover_letter_pdf` setting.
3. Preview the site locally with `docker compose up` and confirm each download link opens
   the intended document.
4. Review the files and changes, then commit and push when ready.

## Credits

Built on the [Orbit](http://themes.3rdwavemedia.com/) theme by Xiaoying Riley (3rd Wave Media),
ported to Jekyll by [sharu725/online-cv](https://github.com/sharu725/online-cv).
