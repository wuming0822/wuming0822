
const thisYear = new Date().getFullYear()
const startTimeOfThisYear = new Date(`${thisYear}-01-01T00:00:00+00:00`).getTime()
const endTimeOfThisYear = new Date(`${thisYear}-12-31T23:59:59+00:00`).getTime()
const progressOfThisYear = (Date.now() - startTimeOfThisYear) / (endTimeOfThisYear - startTimeOfThisYear)
const progressBarOfThisYear = generateProgressBar()

function generateProgressBar() {
    const progressBarCapacity = 30
    const passedProgressBarIndex = parseInt(progressOfThisYear * progressBarCapacity)
    const progressBar =
      '█'.repeat(passedProgressBarIndex) +
      '▁'.repeat(progressBarCapacity - passedProgressBarIndex)
    return `{ ${progressBar} }`
}

const readme = `\
### Hi there 👋
⏳ Year progress ${progressBarOfThisYear} ${(progressOfThisYear * 100).toFixed(2)} %
---
⏰ Updated on ${new Date().toUTCString()}
---



<div>
  <a href="https://github.com/anuraghazra/github-readme-stats#gh-light-mode-only">
    <img align="center" src="https://github-readme-stats.vercel.app/api?username=wuming0822&count_private=true&show_icons=true" alt="wuming0822's GitHub stats" />
    <!-- <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ZxBing0066&show_icons=true&layout=compact" /> -->
  </a>
  <a href="https://github.com/anuraghazra/github-readme-stats#gh-dark-mode-only">
    <img align="center" src="https://github-readme-stats.vercel.app/api?username=wuming0822&count_private=true&show_icons=true&theme=radical" alt="wuming0822's GitHub stats" />
    <!-- <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=ZxBing0066&show_icons=true&theme=radical&layout=compact" /> -->
  </a>
</div>
