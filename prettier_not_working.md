### Problem : Even on installing extension [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) and it is not working i.e not formatting the code

---

### Solution :

- Open VS Code settings.json file by pressing `Ctrl + Shift + P` and typing "settings.json" and selecting "Preferences: Open Settings (JSON)".
- check for `"editor.defaultFormatter": "esbenp.prettier-vscode"` and `"editor.formatOnSave": true` entries in settings.json file. If not present, add them.

from : https://www.youtube.com/watch?v=zd_aDbwr4pY :P
