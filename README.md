## 🚀 Hot reload reload

Issue: https://github.com/gatsbyjs/gatsby/issues/27626

Run:

```bash
yarn install
GATSBY_HOT_LOADER=fast-refresh yarn develop
```

Load http://localhost:8000/

Try editing `src/pages/index.js`, save file.

_Expected behavior:_ Hot reload should work.

_Actual behavior:_ Hot reload does not work.

If you save the file again, or `touch src/pages/index.js`, hot reload will work again.

Maybe there is a weird interaction/race with `.linaria-cache/src/pages/index.linaria.css`?

Related issues:
- https://github.com/gatsbyjs/gatsby/issues/26192
- https://github.com/gatsbyjs/gatsby/issues/26580
- https://github.com/callstack/linaria/issues/682
- https://github.com/callstack/linaria/issues/642
