Workspace: Collecting workspace informationThis project appears to be a collection of HTML files that simulate boot animations for various themes, such as Windows 7, Windows 10, Windows 11, and other creative designs like Mario, Pac-Man, and more. Here's a summary of the workspace structure and its contents:

### Workspace Structure
```
boot/
  balls.html
  cartoon.html
  chineese.html
  mario.html
  no_animated.html
  pacman.html
  slider.html
  vazir.html
  win10.html
  win11.html
  win7.html
  .github/
    workflows/
      static.yml
  fonts/
    balls.otf
    segoen_slboot.ttf
    seguiemj.ttf
    vazir.TTF
  images/
    coin.gif
    logo_doodle.png
    mario_angry.gif
    mario_luige.gif
    mario_rich.gif
    mario_run.gif
    mario.gif
    sonic.gif
    win10.png
    win11.png
    win7.gif
```

### Key Files
1. **HTML Files**: Each file represents a different boot animation or theme:
   - win7.html, win10.html, win11.html: Simulate boot animations for Windows versions.
   - mario.html, pacman.html, cartoon.html: Creative animations inspired by games and cartoons.
   - slider.html: Includes a slider to control animation speed.
   - no_animated.html: A static version without animations.
   - balls.html, chineese.html, vazir.html: Other themed animations.

2. **Fonts**: Custom fonts used in the animations, such as `segoen_slboot.ttf` and `vazir.TTF`.

3. **Images**: Assets like logos and animated GIFs for the boot screens.

4. **GitHub Workflow**: The static.yml file contains a GitHub Actions workflow for deploying the project to GitHub Pages.

### Example Boot Animation
Here’s an example from win11.html:

```html
<img src="./images/win11.png" alt="Logo">
<div id="anim"></div>

<script>
  const start = 0xE100; // Unicode start
  const end = 0xE176;   // Unicode end
  const chars = [];

  for (let i = start; i <= end; i++) {
    chars.push(String.fromCharCode(i));
  }

  const animEl = document.getElementById('anim');
  let index = 0;

  setInterval(() => {
    animEl.textContent = chars[index];
    index = (index + 1) % chars.length;
  }, 20);
</script>
```

### Deployment
The project can be deployed to GitHub Pages using the workflow defined in static.yml. It automates the process of deploying static content to a GitHub Pages site.

Let me know if you need help with any specific part of the project!

peymanx: عالی
قابل کپی کردن بهم بده
اینجوری نمیشه

GitHub Copilot: Here’s a clean and copyable version of your README file:

```markdown
# Boot Animation Project

This project is a collection of HTML files that simulate boot animations for various themes, such as Windows 7, Windows 10, Windows 11, and other creative designs like Mario, Pac-Man, and more. Here's a summary of the workspace structure and its contents:

## Workspace Structure
- **HTML Files**: Each file represents a different boot animation or theme:
  - `win7.html`, `win10.html`, `win11.html`: Simulate boot animations for Windows versions.
  - `mario.html`, `pacman.html`, `cartoon.html`: Creative animations inspired by games and cartoons.
  - `slider.html`: Includes a slider to control animation speed.
  - `no_animated.html`: A static version without animations.
  - `balls.html`, `chineese.html`, `vazir.html`: Other themed animations.
- **Fonts**: Custom fonts used in the animations, such as `segoen_slboot.ttf` and `vazir.TTF`.
- **Images**: Assets like logos and animated GIFs for the boot screens.
- **GitHub Workflow**: The `static.yml` file contains a GitHub Actions workflow for deploying the project to GitHub Pages.

## Example Boot Animation
Here’s an example from `win11.html`:

```html
<img src="./images/win11.png" alt="Logo">
<div id="anim"></div>

<script>
  const start = 0xE100; // Unicode start
  const end = 0xE176;   // Unicode end
  const chars = [];

  for (let i = start; i <= end; i++) {
    chars.push(String.fromCharCode(i));
  }

  const animEl = document.getElementById('anim');
  let index = 0;

  setInterval(() => {
    animEl.textContent = chars[index];
    index = (index + 1) % chars.length;
  }, 20);
</script>
```

## Deployment
The project can be deployed to GitHub Pages using the workflow defined in `static.yml`. It automates the process of deploying static content to a GitHub Pages site.

Let me know if you need help with any specific part of the project!
```