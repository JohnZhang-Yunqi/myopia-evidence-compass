# Myopia Evidence Compass / 近视证据罗盘

An independent, bilingual (English / 中文) evidence-based web tool about myopia
progression in university students. It grades the eye-care advice students usually
receive by the quality of the published evidence, lets a visitor record their own daily
eye-use time, and exports a personal PDF report.

一个独立的双语（英文 / 中文）循证工具，主题是大学生近视的进展。它按已发表证据的质量
给常见建议分级，允许访客记录自己每天的实际用眼时间，并可导出个人 PDF 报告。

## Deploying to GitHub Pages

1. Create a new **public** repository on GitHub.
2. Upload every file in this folder to the root of that repository
   (`index.html`, `robots.txt`, `.nojekyll`, `README.md`).
3. Open **Settings -> Pages**.
4. Under *Build and deployment*, set **Source** to `Deploy from a branch`.
5. Choose branch **main** and folder **/ (root)**, then save.
6. Wait one to two minutes. The site appears at
   `https://<your-username>.github.io/<repository-name>/`.

## Notes

- No build step, no dependencies, no external network requests. The whole site is one static file.
- Visitor data (the eye-use log) is stored in the browser's `localStorage` and never leaves the device.
- The PDF report is produced through the browser's own print pipeline
  (**Export PDF report -> Destination: Save as PDF / 导出 PDF 报告 -> 目标位置：另存为 PDF**),
  so no PDF library is required.
- Language choice is remembered in `localStorage` under the key `mec.lang`.
