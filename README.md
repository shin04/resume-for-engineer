# Daishin Kajiwara's resume

This repository contains my resume in both Japanese and English.

- [Japanese Version (日本語)](https://shin04.github.io/resume-for-engineer/)
- [English Version](https://shin04.github.io/resume-for-engineer/en)

<p>

<a href="https://github.com/shin04/resume-for-engineer/actions/workflows/lint-text.yml" target="_blank"><img alt="lint_text" src="https://img.shields.io/github/workflow/status/shin04/resume-for-engineer/lint%20text?label=textlint&logo=github&color=yellow" /></a>

<a href="https://github.com/shin04/resume-for-engineer/actions?query=workflow%3A%22build+%22" target="_blank" ><img alt="build_pdf" src="https://img.shields.io/github/workflow/status/shin04/resume-for-engineer/build-pdf?label=build%20pdf&logo=github"/></a>

<a href="https://github.com/shin04/resume-for-engineer/tags" target="_blank" ><img alt="release" src="https://img.shields.io/github/release-date/shin04/resume-for-engineer?color=blue&logo=github"/></a>

</p>

## Data

- [GitHub Pages](https://shin04.github.io/resume-for-engineer/)
- [PDF](https://github.com/shin04/resume-for-engineer/releases/)
- [File](https://github.com/shin04/resume-for-engineer/blob/master/docs/README.md)

## Features

### 💅 Lint text

Automatic proofreading with [textlint](https://github.com/textlint/textlint).

```
$ yarn lint --fix
```

It is also automatically executed when pre-commit by [husky](https://github.com/typicode/husky).  
proofreading rules are set with `.textlintrc`.

### 📝 Convert MD to PDF

You can generate PDF with [md-to-pdf](https://www.npmjs.com/package/md-to-pdf).

```
$ yarn build:pdf
```

The output PDF can be styled as you like with CSS. Edit the `pdf-configs/style.css`.

### 🛠 Create release

When you push with a `v**` tag, GitHub Actions will run the build, generate the PDF, create a Release, and register the PDF to Assets.

```
$ git commit -m "add job"
$ git tag v1.0
$ git push origin --tags
```

### 📆 Remind update

Automatically generate issues every three months with GitHub Actions Schedules triggers to prompt you to update your resume.

To change the duration or stop the job, edit `.github/workflows/create-issue.yml`.  
To change the issue contents, edit `.github/ISSUE_TEMPLATE.md`.
