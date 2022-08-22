
[official tailwind installation docs link](https://tailwindcss.com/docs/installation)

## steps

### 1

```shell
npm init -y
```

### 2

```shell
npm i tailwindcss -D
```

### 3 create config file

```shell
npx tailwindcss init
```

### 4 past this in config
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
	content: ["./*.html"],
	theme: {
		extend: {},
	},
	plugins: [],
}

```

### 5 create input.css in src add this to it

```css
@tailwind base; 
@tailwind components; 
@tailwind utilities;
```

### 6 add this in package.json

```json
{
  "name": "",
  "version": "",
  "description": "",
  "main": "index.js",
  "scripts": {
    "build": "tailwindcss -i ./input.css -o ./css/style.css",
    "watch": "tailwindcss -i ./input.css -o ./css/style.css -w"
  }
}
```

### 7 add this in index html

```html
<link rel="stylesheet" href="./css/style.css" />
```

## start build script then watch script

```shell
npm run build
```

```shell
npm run watch
```