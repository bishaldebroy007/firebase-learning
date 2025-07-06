# Firebase

In this repo, I have kept all my practice materials for Firebase throughout my learning journey. 

## Installation and Setup

Use the package manager [yarn](https://yarnpkg.com/) to install.

```
yarn
```
***Or,***
```
yarn install
```
**Run the project:**
```
yarn dev
```

**Do not forget to install the package**
```
yarn add firebase
```
***Or, if npm is used***
```
npm install firebase
```

## Learning Doc:
**Google Authentication:**

***Button.jsx***
```jsx
import React from 'react'
import { getAuth, signInWithPopup, GoogleAuthProvider } from "firebase/auth";
import { app } from '../Firebase/firebaseInit';

const SignInPage = () => {
    const auth = getAuth(app);
    const provider = new GoogleAuthProvider();

    const SignInClick = () => {
        signInWithPopup(auth, provider)
            .then(result => {
                console.log(result);
            }).catch(error => {
                console.log('some error', error);
            })
    }
    return (
        <div>
            <button onClick={SignInClick} className='border-1 bg-amber-200 hover:scale-105 duration-200 p-10 rounded-2xl cursor-pointer shadow-2xl hover:shadow-3xl'>Sign in with google</button>
        </div>
    )
}

export default SignInPage

```

![image](https://github.com/user-attachments/assets/d5e05f01-1553-4d61-9bb4-8d4f12d56a68)


## Acknowledgement

Thanks to [@Programming Shikhbo](https://www.youtube.com/c/ProgrammingShikhbo)
