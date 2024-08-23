---
title: Submitting on arXiV in 2024
description: ""
date: 2024-08-23
tags:
  - english
---
I submitted my first paper[^1] on arXiV yesterday (🎉), alongside submitting it to a journal we want to publish to, and it was way more painful than I thought it would be. I thought I was prepared for everything, I even followed [Trevor Campbell's tutorial](https://trevorcampbell.me/html/arxiv.html) which I found less than two weeks ago.

Alas, it did not go as expected. The reasons were threefold: 
1. I worked with my local LaTeX files and TeXLive installation, 
2. I used `biblatex` for my references,
3. my version of TeXLive is newer than the one on arXiV.
This way, all my references were missing from the generated PDF. It took me quite a while to figure out what to look for, but then the easiest way for me to solve it was to use a [script from StackExchange](https://tex.stackexchange.com/a/723571) that downgrades my version 3.3 `.bbl` file to version 3.2. That fixed it 🙌

Right after that, I talked to one of my group members, who simply suggested to use Overleaf for the final step: Using their [submit to arXiV feature](https://www.overleaf.com/learn/how-to/LaTeX_checklist_for_arXiv_submissions) should do the trick without all of the pain... I'll try that next time!

[^1]: it's here: https://arxiv.org/abs/2408.12582