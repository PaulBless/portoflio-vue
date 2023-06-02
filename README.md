# Personal Portfolio 
Hi there!, I am Paul, this is a repository for my personal portfolio built with Vue, Bootstrap & Firebase. 
Everything is included. Written in VueJS, Bootstrap and Tailwind CSS!


## Porftolio URL

<a href="https://iampaul.netlify.app/">Visit Portfolio</a>

## Features [특징]

-   Simple, responsive design
-   [Vue.js v3](https://vuejs.org) with [Vue Router](https://router.vuejs.org)
-   [Tailwind CSS v3](https://tailwindcss.com)
-   Vue transitions
-   Reusable Components
-   V-motion Animations
-   Firebase Config, Hosting
-   Responsive Bottom Navbar


## Installation

1. ##### Make sure you have NodeJS installed.

-   [Download it from nodejs.org](https://nodejs.org)
-   [Install it using NVM ](https://github.com/nvm-sh/nvm)
-   If you're on Mac, Homebrew is a good option too:

```
brew install node
```

2. ##### Clone the reposity:

```
git clone https://github.com/PaulBless/portfolio-vuejs.git
```

3. ##### Open the folder:

```
cd portfolio-vue
```

4. ##### Install packages and dependencies:

```
npm install
```

5. ##### Start a local dev server at `http://localhost:8080`:

```
npm run serve
```

## Interesting Informations

##### 1.Firebase Config [ v8 version ]

```
import firebase from "firebase/compat/app";
import "firebase/compat/auth";
import "firebase/compat/firestore";


const firebaseConfig = {
    apiKey: "",
    authDomain: "",
    databaseURL: "",
    projectId: "",
    storageBucket: "",
    messagingSenderId: "",
    appId: "",
    measurementId: "",
};

const firebaseApp = firebase.initializeApp(firebaseConfig);

const db = firebaseApp.firestore();
const auth = firebase.auth();

export { auth, db };

```
<br><br>
