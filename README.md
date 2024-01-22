# Personal Website React SPA

Forked from [JoHoop](https://github.com/JoHoop/personal-website-react).

# Customizations

- Add more social media buttons? Go to `\src\pages\Resume.js`
- Want to change sphere colors? Go to `\src\components\background\DisplacementSphere.js` and modify the following:
```
    useEffect(() => {
        const dirLight = new DirectionalLight(
            rgbToThreeColor("250 50 100"),
            0.6
        );
        const ambientLight = new AmbientLight(
            rgbToThreeColor("250 50 100"), // here
            theme === "light" ? 0.8 : 0.1
        );
```