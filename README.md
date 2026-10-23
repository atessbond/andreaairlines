# Andrea Airlines -- The Sophisticated AA

Deployed on Cloudflare at https://www.andreaairlines.com/.

## Working here

`site/` is what is served, and it is served as it stands --- three files, no
build. `npm run dev` serves it locally through sirv; `npm run preview` serves
the same folder through wrangler, as Cloudflare will.

Cloudflare deploys every push to `main`. The `build` script does nothing on
purpose: once a `package.json` exists Cloudflare runs its build step, and a
missing script fails it --- which leaves the previous deploy serving and looks
exactly like nothing happening.
