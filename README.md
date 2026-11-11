# Math Pitch — Grade 6 Math (Taiwan 六年級 level)

An offline-capable web app for short daily practice of every core Grade 6 math skill in Taiwan's 108 curriculum, plus the Grade 5 foundations they rest on. Same engine as the other apps: unit checks, spaced repetition, daily sessions, XP and streaks, a parent report, and progress stored on the device. Word problems can be themed soccer, Minecraft, or mixed.

## Coverage

| Unit | 課綱 | Semester* | Skills |
| --- | --- | --- | --- |
| Grade 5 foundations | 五年級先備 | 五年級 | adding/subtracting fractions, multiplying fractions and decimals, percentages, order of operations, triangle and trapezoid area |
| Factors and multiples | 質因數、公因數與公倍數 | 六上 | prime factorization, GCF, LCM, LCM word problems |
| Dividing fractions and decimals | 分數與小數除法 | 六上 | fraction ÷ fraction, fraction-division word problems, decimal ÷ decimal |
| Ratios | 比與比值 | 六上 | ratio value, missing term, sharing in a ratio |
| Circles | 圓周長與圓面積 | 六上 | circumference, area, semicircles and quarter circles (π = 3.14) |
| Proportion and scale | 正比與比例尺 | 六下 | map scale, direct proportion |
| Speed | 速率 | 六下 | speed, unit conversion, distance and time |
| Prisms and cylinders | 柱體體積與表面積 | 六下 | prism and box volume, cylinder volume, box surface area |
| Letters for numbers | 用文字符號表示數 | 六下 | finding the unknown, evaluating expressions, writing equations from words |
| Circle graphs | 圓形圖 | 六下 | percent of a total, section angles |

31 skills, each generating fresh problems. *Publishers (康軒, 南一, 翰林) order a few units differently, so the 六上 / 六下 split is approximate.

## How it works

- **Unit checks first**: one question per skill; right answers are marked known (and reviewed a week later), the rest enter daily practice. Stats lists every gap found.
- **New skill** = key idea + worked example + two tries. **Wrong answer** = full solution, then a similar problem right away; the skill returns tomorrow.
- **Spaced review** 1 → 3 → 7 → 14 → 30 days, new numbers every time. Mastered from box 4.
- **Typed answers**: whole numbers, fractions (write mixed numbers as improper fractions, e.g. 7/2), or decimals. Equivalent forms are accepted.

## Files, deployment, updates, parent report

- `index.html`, `sw.js`, `manifest.json`, icons, `apps-script.gs`. Deploy from the root of a GitHub Pages repository. Don't commit `.env`.
- **Change `VERSION` at the top of `sw.js` on every release.** The installed version shows at the bottom of Setup.
- Progress lives in `localStorage`; on iOS, deleting the home-screen icon deletes it — use **Setup → Export progress** first.
- Parent report: deploy `apps-script.gs` as a Google Apps Script web app (Execute as *Me*, access *Anyone*) and paste the `/exec` URL into **Setup → Parent report** on the student's device. Keep the URL private.
