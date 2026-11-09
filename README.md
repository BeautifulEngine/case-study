# Case Study

Turn the raw material of a project (notes, images, a deck, links, a client email) into a case study that shows how the person thinks and what changed because of their work. One story, three formats: a web page, a PDF, and Markdown.

**What you get:** Turns project notes, images, a deck or links into a portfolio case study - a responsive web page, a PDF and Markdown ready to paste into a portfolio site, Behance, Notion or LinkedIn - covering the challenge, insight, idea, process, craft, results and credits. Can tailor the story to a target company or role. Never invents results or quotes.

Made by Beautiful Engine · [beautifulengine.com](https://www.beautifulengine.com) · [Questions or ideas? Open an issue](https://github.com/BeautifulEngine/case-study/issues/new)

## Install

### Claude app (web or desktop)

1. Download **[case-study.zip](case-study.zip)** from this repo (open the file, then use the download button). Don't unzip it.
2. Turn on **Settings > Capabilities > "Code execution and file creation"**.
3. Go to **Customize > Skills**, click **+**, then **+ Create skill > Upload a skill**, and upload the zip.
4. Start a new chat and ask in plain words. Claude picks the skill up on its own.

> GitHub's green "Code > Download ZIP" button won't work for this; it wraps everything in an extra folder. Use `case-study.zip`.

### Claude Code

As part of the Beautiful Engine collection (you get updates and the other skills):

```bash
claude plugin marketplace add BeautifulEngine/skills
claude plugin install beautiful-engine@beautiful-engine
```

Then use `/beautiful-engine:case-study`, or ask in plain words. Or install just this one:

```bash
git clone https://github.com/BeautifulEngine/case-study.git
mkdir -p ~/.claude/skills && cp -r case-study/case-study ~/.claude/skills/
```

Then use `/case-study`.

## Usage

```
/case-study <project name> [for <company or role>] [short | long]
```

Attach whatever exists: images, a PDF deck, notes, press links, results. Plain requests work too:

- "Write a case study for the Sphere partnership launch. Notes and images attached."
- "Turn this deck into a portfolio case study, short version."
- "Case study for my art car project, aimed at experiential agency roles."
- "Rewrite this case study for a Netflix design lead application." (attach the existing one)

**Length.** Default is about 600–900 words with 6–10 images. "short" is a 150–250 word card for a portfolio grid or LinkedIn post. "long" adds process detail for a design-team audience.

## When Claude uses it

Someone asks for a case study, portfolio write-up, project page, project story, or help presenting past work for a job or a pitch.

## How it works

```
case-study/
├── SKILL.md
├── assets/  base.css, case-study-template.html, deck.css
├── scripts/  audit.js, contact_sheet.py, fonts.py, render.cjs, render.py, tokens.py
├── references/  rendering.md
```

PDFs are built from HTML templates, colored and typeset with the right brand, rendered by headless Chrome, then checked for fonts, text contrast and leftover blanks before delivery. Anything with numbers in it is calculated by a script, not estimated.

## Works well with

- [Application Kit](https://github.com/BeautifulEngine/application-kit)
- [Company Brief](https://github.com/BeautifulEngine/company-brief)
- [All Beautiful Engine skills](https://github.com/BeautifulEngine/skills)

## Made by Beautiful Engine

Case Study is made by [Beautiful Engine](https://www.beautifulengine.com), a creative studio in Los Angeles working across brand, experiential and interactive design.

- **Website:** [beautifulengine.com](https://www.beautifulengine.com)
- **Questions, ideas, or something broke?** [Open an issue](https://github.com/BeautifulEngine/case-study/issues/new) and describe what you asked for and what happened.

This repo is published from [BeautifulEngine/skills](https://github.com/BeautifulEngine/skills); changes are made there and copied here.

## License

MIT. See [LICENSE](LICENSE).

