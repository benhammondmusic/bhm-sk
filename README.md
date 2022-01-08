# BenHammondMusic - SvelteKit Refactor

Once ready, this site build will replace benhammondusic.com, but for now the work in progress site is deployed via Netlify:

> https://bhm-sk.netlify.app/

## Why rebuild benhammondmusic.com ?

- I kept hearing great things about Svelte and Sveltekit and wanted to mess around with it in a low-stakes way

- My music site was built with simply hard coded HTML ad CSS; since I'm using React daily in my work it's painful and annoying to go back to a componentless structure
- I was already able to save myself $12 a month simply moving my site from Hostgator to Netlify (and using a real CI/CD process via GitHub/Netlify instead of just dumping raw files onto the server via FTP like I've done since 2005)
- My career transition from full-time musician to full-time software engineer has given me the space to slow down on gig promotion and some flexibility in disrupting my website / online presence.


# create-svelte documentation


Everything you need to build a Svelte project, powered by [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte);

## Creating a project

If you're seeing this, you've probably already done this step. Congrats!

```bash
# create a new project in the current directory
npm init svelte@next

# create a new project in my-app
npm init svelte@next my-app
```

> Note: the `@next` is temporary

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

Before creating a production version of your app, install an [adapter](https://kit.svelte.dev/docs#adapters) for your target environment. Then:

```bash
npm run build
```

> You can preview the built app with `npm run preview`, regardless of whether you installed an adapter. This should _not_ be used to serve your app in production.
