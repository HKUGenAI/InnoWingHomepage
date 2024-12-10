# HKU Innowing GenAI Homepage 
Built with Next.js Notion Starter Kit, deployed on Vercel.

[![Next.js](https://ziadoua.github.io/m3-Markdown-Badges/badges/NextJS/nextjs1.svg)](https://nextjs.org/) [![Vercel](https://ziadoua.github.io/m3-Markdown-Badges/badges/Vercel/vercel1.svg)](https://vercel.com) ![Notion](https://ziadoua.github.io/m3-Markdown-Badges/badges/Notion/notion3.svg)

## Setup

**All config is defined in [site.config.ts](./site.config.ts).**

This project requires a recent version of Node.js (we recommend >= 16).

1. Fork / clone this repo
2. Change a few values in [site.config.ts](./site.config.ts)
3. `npm install`
4. `npm run dev` to test locally

### Deployment

If the local Vercel CLI is not logged-in you need to loggin first by
1. `vercel login`
2. Select Continue with Email
3. Enter email: genai.innowing@gmail.com
4. Finish login by clicking the verification link sent to our email

Then simply run `npm run deploy`, if asked "Link to existing project?" answer yes and choose "innowing-homepage"

### Editing Metadata

Only need to edit the `rootNotionPageId` in [site.config.ts](./site.config.ts). All page under the root page will be visible on the website.

`rootNotionPageId` for InnoWing GenAI Homepage is: **InnoWing-GenAI-Homepage-12da31d3d5b58026bf2bce49f50d00be**

## Adding new pages

Simply go to our [Root Notion Page](https://www.notion.so/innowinggenai/InnoWing-GenAI-Homepage-12da31d3d5b58026bf2bce49f50d00be?pvs=4) and edit there.

You may also want the url path name tobe different of the page name, see below for instruction.


## URL Paths

The app defaults to slightly different URL paths in dev vs prod (though pasting any dev pathname into prod will work and vice-versa).

In development, it will use `/nextjs-notion-blog-d1b5dcf8b9ff425b8aef5ce6f0730202` which is a slugified version of the page's title suffixed with its Notion ID. I've found that it's really useful to always have the Notion Page ID front and center during local development.

In production, it will use `/nextjs-notion-blog` which is a bit nicer as it gets rid of the extra ID clutter.

If you wish to override a url path modify `pageUrlOverrides` in [site.config.ts](./site.config.ts)


## Styles

All CSS styles that customize Notion content are located in [styles/notion.css](./styles/notion.css). They mainly target global CSS classes exported by react-notion-x [styles.css](https://github.com/NotionX/react-notion-x/blob/master/packages/react-notion-x/src/styles.css).

Every notion block gets its own unique classname, so you can target individual blocks like this:

```css
.notion-block-260baa77f1e1428b97fb14ac99c7c385 {
  display: none;
}
```


