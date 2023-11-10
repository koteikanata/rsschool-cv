### About me
Nataly
#### Contact Information: 
Russia  
telegram @koteikanata

I am looking for a job as a junior frontend developer.
At the moment I have experience in developing single-page websites, solving algorithmic problems and other small projects, examples of which you can find on my github.
Now I am actively studying js, ts, react.

### Skills
- js/ts
- html/css
- Git
- SQL
- java

### Code examples
<details>
  <summary>Code examples for solving the problem of finding the shortest path from point A to point B</summary>
  
   ```javascript

const { readFileSync, writeFileSync } = require('fs');
const { resolve, join } = require('path');

const path = resolve(__dirname, '..');

const [x1, y1, x2, y2] = readFileSync(join(path, 'input.txt'), 'utf-8').toString().trim().split(' ').map(Number);

const result = calculateDistance(x1, y1, x2, y2).toFixed(9);

writeFileSync(join(path, 'output.txt'), minLength.toString());

function calculateDistance(x1, y1, x2, y2) {
    // расстояния от точек до начала координат
    const distA = Math.hypot(x1, y1);
    const distB = Math.hypot(x2, y2);

    const distDifference = Math.abs(distB - distA);

    // если какая-то из точек лежит а начале координат
    if ((x1 === 0 && y1 === 0) || (x2 === 0 && y2 === 0)) {
        return distA + distB;
        // если точки лежат на одной прямой, проходящей через начало координат и при этом они в одной четверти
    } else if ((x1 / y1 === x2 / y2) && ((x1 * x2 > 0) && (y1 * y2 > 0))) {
        return distDifference;
    } else {
        // углы между точками и началом координат
        const angleA = Math.atan2(y1, x1);
        const angleB = Math.atan2(y2, x2);

        // путь по прямой
        const byLine = distA + distB;

        // разница углов 
        const angleDifference = Math.abs(angleB - angleA);

        // длина дуги окружности
        const arcPathLength = Math.min(distA * angleDifference, distB * angleDifference);

        // путь по дуге + прямой
        const circlePathLength = arcPathLength + distDifference;

        // Находим минимальную длину пути из трех вариантов
        const minLength = Math.min(byLine, distA === distB ? arcPathLength : Infinity, circlePathLength);

        return minLength;
    }
}

module.exports = calculateDistance;

```

</details>


### Work experience
Simple web applications, participation in the development of browser extensions

### Education
Various online courses at html academy, stepik  
Training on algorithms from Yandex

### Languages
English (A2)

[link to cv](https://koteikanata.github.io/rsschool-cv/cv)
