###### EUID ╳ Likelion

# Tailwind CSS

멋쟁이 사자처럼 프론트엔드 스쿨 TailwindCSS 예제 저장소

** degit으로 src 폴더 복사 **

```sh
cd learn-sass
degit seulbinim/euid-tailwind/src src
```

**src 폴더 복사**

**package.json 스크립트 명령**

```js
"scripts": {
  "dev": "run-p tailwind:watch serve",
  "serve": "five-server",
  "tailwind": "tailwind -i ./src/css/input.css -o ./src/css/output.css",
  "tailwind:watch": "npm run tailwind -- --watch",
  "tailwind:build": "npm run tailwind -- --minify",
  "clean": "rimraf css/"
},
```

**fiveserver.config.js**

```js
module.exports = {
  port: 8085,
  root: 'src/',
  open: ['index.html', 'login.html'],
  host: 'localhost',
  browser: 'chrome',
  https: false,
  watch: 'src/',
};
```

**tailwind.config.js**

```
module.exports = {
  content: ['./src/**/*.html'],
  darkMode: 'class', // or 'media' or 'class'
  theme: {
    extend: {
      backgroundImage: (theme) => ({
        'checkbox-default': "url('/images/checkbox-default.svg')",
        'checkbox-checked': "url('/images/checkbox-checked.svg')",
      }),
      colors: {
        white: '#ffffff',
        black: '#000000',
        gray1: '#333333',
        gray2: '#4f4f4f',
        gray3: '#828282',
        gray4: '#bdbdbd',
        gray5: '#e0e0e0',
        gray6: '#f2f2f2',
        gray7: '#f9f9f9',
        primary: '#373E6A',
        secondary: '#699AFE',
      },
      fontFamily: {
        sans: ['Noto Sans KR', 'sans-serif'],
      },
      fontSize: {
        '10xl': '120px',
      },
    },
  },
  plugins: [],
};
```
