# Browser technologies

## Table of contents
1. [Live demo](#live-demo)
2. [Installation](#installation)
3. [Research](#research)

## Live demo
Check out my live demo on my server: [bt.gijsbertcharles.com](https://bt.gijsbertcharles.com)

## Installation
Clone this repo
```bash
git clone https://github.com/gijslaarman/browser-technologies-1920.git
```

Change directory to server directory:
```shell
cd browser-technologies-1920/server
```

Install dependencies:
```shell
npm install
```

Creating a .env environment:
```shell
touch .env
```
And fill in the following things: (This is mongodb server)
```env
DB_URL=<your_db_url>
DB_PORT=<your_db_port>
PORT=<your_server_port>
```

Scripts for running:
```shell
'npm run dev' // Testing environment, detects server changes.
'npm start' // production environment.
```

Enjoy!

## Research
I've done research on testing two subjects:
- Color / color blindness
- Not using any cookies

Check it out [here](research/Ppdracht1.1.md)

And tested out my own previously hacked prototype, you can see the results [here](research/Opdracht1.2.md)

### Wireframes
Lo-fi
![LoFi sketches of my idea.](research/img/Sketches.jpg)
Let's work that out into something a bit more understandable.

Hi-fi(er)
![Sketch: My photo's](research/img/IMG_5159.jpg)
![Sketch: Carousel page](research/img/IMG_5160.jpg)
![Sketch: Showcase](research/img/IMG_5161.jpg)

This gave me a global idea of how I wanted to achieve the goal. Since there's a lot of room for my own ideas and how to do stuff I decided that as I would code I would make my decisions (Not just being lazy but also to gain more experience on the progressive enhancement stuff, since I knew I would have to rewrite a lot of parts).

## Progressive enhancement
- In HTML you can upload, delete and select the images you want to show in the carousel. Only the carousel itself doesn't work.
I should have split up the images per page where you can navigate easily through the pages with links.
> I lost track here of the progressive enhancement, basically I had in mind that css works 99% of the time so it wouldn't be an issue.

- In CSS the carousel works, and you can scroll through the carousel without Javascript being used. It's not fancy and the user experience isn't optimal but it works.

- With javascript you can flick through the images with the keyboard buttons & the buttons are fixed so you can easily scroll through. I would have liked to be able to drag the carousel with your finger, but I didn't figure that out would need more time to do that.

## Fallbacks
- If the user has no javascript enabled then the user can still scroll through the carousel with buttons. Using the \<noscript> tag the browser detects if the buttons per image should be visible.
#### Could be features & their fallbacks:
- With javascript enabled the user can select their carousel selection without having to click "save selection".
- Reduce the two pages to one, UX wise it's horrible. But that's what HTML/CSS only permits. So if javascript is enabled it's easy to merge the two pages together. The fallback would still be the two pages.

## Browser support
Tested on these browsers currently have no issues (nor css defects) Windows & Mac:
- Chrome
- Firefox
- Safari
- Edge

> I'm going to be honest, the site isn't complex enough on the frontend for it to really have any troubles. I used conventions already supported by every browser except internet explorer, but nobody is going to use internet explorer on their own personal devices, because in this case it's personal use (personal gallery). (Internet explorer is not even in the Windows OS package anymore.)

## To do's
- [ ] Split up the carousel into 1 image per page. And progressive enhance the swiping through by handling the next image with Javascript.
- [ ] Save selection without having to click save selection.
- [ ] If javascript is enabled the carousel & overview pages can be merged. But has to be seperate to keep it working on HTML/CSS only.
- [ ] If CSS supports scroll-snapping use that. If not (how do I check that?) fall back to the javascript version.

Submit an [issue](https://github.com/gijslaarman/browser-technologies-1920/issues/new) if you find any bugs, state the OS, Browser & version.