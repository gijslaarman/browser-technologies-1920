# Testen van OBA 
[Link naar mijn OBA project](https://github.com/gijslaarman/project-1-1920)

## Table of contents


## Testing on devices

### iPod touch (4th generation)
- Ios version: 6.0.1 (10A523)
- Browser: Safari 

```
Mozilla/5.0 (iPod; CPU iPhone OS 6_0_1 like Mac OS X) AppleWebKit/536.26 (KHTML, like Gecko) Version/6.0 Mobile/10A523 Safari/8536.25
```

#### Foundings
1. The CSS is fine, but I couldn't fully test if it worked since I never could see a detailpage.
1. Interaction did not work, the javascript didn't fire. There is a preventDefault set on the form submit, yet this does not work. 

#### Solution
There are two ways to fix the javascript not being used:
1. Use [Babel](https://babeljs.io/) to maybe fix the javascript and set it over to more browser compatibility.
2. _Better option_, Handle the submit server side, and return HTML.