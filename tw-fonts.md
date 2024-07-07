## How to setup Tailwind CSS fonts (with example)

Step 1: Copy the link tag from google fonts of the specific font that you are using:

```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet">
```

Step 2: Paste this into the extend{} of your tailwind.config.js file:

```
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {
      fontFamily: {
        Poppins: ['Poppins', defaultTheme.fontFamily.sans],
      },
    },
  },
  plugins: [],
}
```

Step 3: Now add this class to your element in your html file:

```
<body class="font-fontcustomid">
```

### Note: The 'fontcustomid' can be replaced by any name, and the ', defaultTheme.fontFamily.sans' is used so if for some reason your font doesn't load, then the sans font loads.