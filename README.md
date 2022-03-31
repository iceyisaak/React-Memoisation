# React Memo & Callback

### React.Memo() vs useMemo() vs useCallback()

By default, when the data is changed, the entire component is rerendered. If that component has a child component, the child component also gets rerendered, causing unnecessary resource consumption.

With Memo & Callback, the data gets memoised, allowing the data to be cached and only rendered when the data really gets updated.

Memoising always come with a cost. Only use when neccessary.

<br/> 
<br/>
<br/> 

### React.Memo()
**Purpose:** <br/>
  - Use for memoising the component in order to avoid unnecessary rerendering of a child component by caching the value used by the child component
**Use Case:** <br/>
  - To only rerender the child component when the prop actually changes, and not rerender the exact same value all over gain when no changes really occur
**Beware:** <br/>
  - No referrential equality is checked (Only works if the value is a string or a number)

<br/> 
<br/> 

### useMemo()

**Purposes:**<br/>
  1. Use for memoising the data value used and so that only the child component is rendered when its props really change.
  2. The value referrential equality is checked (Working with all data types)
  
**Use Case:**<br/>
  - To cache data of all types in a child component so the data only be rerendered when changes to data really occured.
 
**Beware:**<br/> 
  1. `useMemo()`Doesn't work with functions. Use `useCallback()` instead.
  2. Don't use `useMemo()` to call other hooks.

<br/> 
<br/> 

### useCallback()

**Purpose:**<br/> 
  - Use for memoising the function, allowing it to be cached and only be executed when its dependecy changes.

**Use Case:**<br/> 
  - To allow function to run only when the dependency is updated. This avoid the function in a child component to be triggered when the parent component is rerendered.

**Beware**: 
  - `useCallback()` consume a lot of resources. Only use when necessary.

---

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `yarn build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
