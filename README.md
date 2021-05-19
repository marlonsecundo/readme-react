<h2 align="center">💡 NOTE: Read the entire document carefully</h2>

<br/>
<br/>

<h4 align="center">
 <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/a/a7/React-icon.svg/1200px-React-icon.svg.png" alt="Project logo" width="50%" />
</h4>

<h2 align="center"><b>PROJECT NAME</b></h3>

---

<h3 align="center">project description</h3>
<br/>
<br/>

# 🏁 Getting Started

## 🔧 Env Requirements

- list
- of
- programs
- or resources
- needed to be
- installed
- on the dev system

### Installing

```sh
# Example
commands for the installation process
```

### Running

```sh
# Example
commands to running the project
```

<br/>
<br/>

# 👨‍💻️ Development Team Guidelines

- ## Clean Code

<br/>

- ## Make the code implementation easier for a new member to understand, if not possible, leave a comment explaining

<br/>

- ## Modularize reutilizables components, dont repeat yourself

<br/>

- ## Separe the logic application code from the react view code, logic application are put in services.

<br/>
<br/>

# ⌨️ Code Guidelines

- Language: English
- Programming Language: Typescript
- File compound names are separated with **kebab-case** (-).

```sh
# example
home-screen.tsx
```

- All services are classes, and named with **.service** in the end of file name

```ts
// example
// ws-client.service.ts

import { Client } from "socket.io";

class WsClient {
  public io: Client;
  private booted = false;

  public init() {
    if (this.booted) {
      return;
    }

    this.booted = true;
    this.io = new Client();
  }
}

export default new WsClient();
```

- Export compound names are written with **PascalCase**

```ts
// example
export default SplashScreen;
```

- **Enums** are named with the letter E in the beginning, and defined in the **enums.ts** file.

```ts
// example
export enum EResultStatus {
  ERROR,
  DONE,
  EMPTY,
  LOADING,
}
```

- **Interfaces** are named with the letter **I** in the beginning, and defined in the **types.ts** file.

```ts
// example
export interface IStore {
  isDarkMode: boolean;
}
```

<br/>
<br/>

# 📁 Directory Structure

- **hooks/** -> React hooks
- **components/** -> Atomic react components
- **pages/** -> a view/screen with a group of components/
  - example-screen
    - **components/** -> components **only** that remains in that especific page
- **services/** -> the application logic stays here, dont code application logic inside of views.
- **styles/** -> styles variables
- **store/** -> state managment

<br/>
<br/>

# 📐 Code Lint

- Eslint
- Prettier

**Priorize prettier in styling conflits**

<br/>
<br/>

# 🔘 Design and UI Components

_Project Design UI Link_

**Example**

This project use the RNUI, a components library to create UI and layout with a design system.

See more in:

https://wix.github.io/react-native-ui-lib/

<br/>
<br/>

# ⌨️ Root Import

To import componets from another locations aways use the **src** root import!

Example:

```tsx
// routes.tsx

import React from "react";

// Root import
import SplashScreen from "src/pages/splash-screen";
import StartScreen from "src/pages/start-screen";

// DONT DO THIS! 🤦
import example from "../../../example";
```

<br/>
<br/>

# 👨‍💻️ Git Commit Guidelines

### Type

Must be one of the following:

- **feat**: A new feature
- **fix**: A bug fix
- **docs**: Documentation only changes
- **style**: Changes that do not affect the meaning of the code (white-space, formatting, missing
  semi-colons, etc)
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **perf**: A code change that improves performance
- **test**: Adding missing or correcting existing tests
- **chore**: Changes to the build process or auxiliary tools and libraries such as documentation
  generation
- **wip**: Work in Progress

**Example:**

```sh
git commit -m "feat: sigaa login form"
```

<br/>
<br/>

# ⛏️ Built Using

### **General**

- **Typescript:** Static type-checking along with the latest ECMAScript features.
- [**Expo:**](https://expo.io/) To create react native app
- **Eslint** Enforce code style
- **Prettier:** Code style and code Formatter
- [**Pullstate:**](https://lostpebble.github.io/pullstate/docs/quick-example) For state managment
- [**React Navigation V5:**](https://reactnavigation.org/) For navigation
  <br/>
  <br/>
