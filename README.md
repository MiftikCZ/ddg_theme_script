# DDG Theme Script
Simple and minimal duckduckgo script for making custom themes

## usage
- go on https://duckduckgo.com
- open developer console by right click > inspect > console
- paste this script and customize it
- *this script has mine gray config for pulse browser (a better fork of Firefox)*

```js
(function() {
  const ct = {
    base: "#26222A",
		clicked:"#C555F2",
		text:"#F2F1F4",
		head: "#1A171C",
		link: "#6D98F3",
		fullLink: "#C2D4FA"
  };
  const theme = [
    `21=${ct.head}`,
    `7=${ct.base}`,
    `8=${ct.text}`,
    `9=${ct.link}`,
    `aa=${ct.clicked}`,
    `ae=${ct.base}`,
    `j=${ct.head}`,
    `x=${ct.fullLink}`,
  ];

  for (const item of theme) {
    document.cookie = `${item}; max-age=126144000; samesite=lax; secure`;
  }
})();
```
![Snímek obrazovky_2023-03-23_19-39-22](https://user-images.githubusercontent.com/89579269/227315603-465f4cd3-3688-4390-87f0-5a830b490672.png)
- *this is how it looks*
