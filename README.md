# Personal Website React SPA

Forked from [JoHoop](https://github.com/JoHoop/personal-website-react).

![image](/current-state-of-website.JPG)

# Customizations

- Add more social media buttons? Go to `\src\settings\Resume.json` and modify `{"basics" : { ..., "profiles" : [array]}`
- Want to change sphere colors? Go to `\src\components\background\DisplacementSphere.js` and modify the following:
```
    useEffect(() => {
        const dirLight = new DirectionalLight(
            rgbToThreeColor("250 50 100"),
            0.6
        );
        const ambientLight = new AmbientLight(
            rgbToThreeColor("250 50 100"),              // <--- here
            theme === "light" ? 0.8 : 0.1
        );
```
- Selection color? Go to `\src\index.css` and modify the following:
```
::-moz-selection {
    background: red;               // <--- here
    color: #fafafa;
    text-shadow: none;
}
::selection {
    background: red;               // <--- here
    color: #fafafa;
    text-shadow: none;
}
```

# TODO
- Implement a blog button by modifying sponsor button where
```
\src\pages\home.js

export const Home = () => {
  const classes = useStyles();

  return (
    <>
        ...
        {/* <FooterText /> Needs to be uncommented and modified to Blog button*/} <---
      </div>
    </>
  );
};
```
and the router DOM pages needs to be modified in `App.js` & `FooterText.js`.
- Potentially move out of AWS and back to github pages?
