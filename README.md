<p align="center">
  <a href="" rel="noopener">
 <img width=150px height=150px src="https://www.hackyourfuture.dk/static/logo-dark.svg" alt="Project logo"></a>
</p>

<h3 align="center">Rate my cv</h3>

---

## π Table of Contents

- [π Table of Contents](#-table-of-contents)
- [π§ About <a name = "about"></a>](#-about-)
- [βοΈ Built Using <a name = "built_using"></a>](#οΈ-built-using-)
- [π Project's Calendar](#-projects-calendar)
- [π©π»βπΌπ‘π¨π½βπΌ The Customer](#-the-customer)
  - [πΌ Business Glossary](#-business-glossary)
  - [ποΈ Database Model Diagram](#οΈ-database-model-diagram)
  - [πΌ Mockup](#-mockup)
  - [πΌ Features](#-features)
- [π Process ππ](#-process-)
  - [π» Working with code](#-working-with-code)
  - [π§± Guidelines for building components](#-guidelines-for-building-components)
    - [A note about React Hooks](#a-note-about-react-hooks)
    - [Proptypes](#proptypes)
    - [Using Storybook](#using-storybook)
    - [How to create a new story](#how-to-create-a-new-story)
      - [Adding knobs (optional)](#adding-knobs-optional)
    - [Breaking down components](#breaking-down-components)
    - [Coding guidelines for components](#coding-guidelines-for-components)
  - [π¨ Theming and global styling](#-theming-and-global-styling)
  - [π§± Component styling](#-component-styling)
  - [π€ π₯ Inline CSS vs Stylesheets](#--inline-css-vs-stylesheets)
  - [ππ½ Code best practices](#-code-best-practices)
  - [<img width=20px height=20px src="/git-logo.png" alt="GitHub logo"></a> Working with GIT](#a-working-with-git)
  - [<img width=15px height=30px src="/heroku-logo.svg" alt="Heroku logo"></a> Working with Heroku and Deployment](#a-working-with-heroku-and-deployment)
  - [<img width=59x height=20px src="/knex-logo.png"  alt="Knex logo"></a> Working with Knex and Migrations](#a-working-with-knex-and-migrations)
  - [<img width=25px height=25x src="/swagger-logo.png"  alt="Swagger logo"></a> Working with API Documentation - Swagger](#a-working-with-api-documentation---swagger)
  - [<img width=20px height=20x src="/storybook.svg"  alt="Storybook logo"></a> Working with Storybook](#a-working-with-storybook)
  - [<img width=30px height=30x src="/aws.svg"  alt="AWS S3 logo"></a><img width=30px height=30x src="/s3.png"  alt="AWS S3 logo"></a> Working with AWS - Amazon Services](#aa-working-with-aws---amazon-services)
  - [Testing](#testing)
  - [Making authenticated requests through firebase (useFetch hook)](#making-authenticated-requests-through-firebase-usefetch-hook)
    - [What is it?](#what-is-it)
    - [Usage](#usage)
- [π Getting Started](#-getting-started)
  - [πΎ Installations](#-installations)
    - [Errors](#errors)
  - [Code linting](#code-linting)
- [π Getting the HackYourFuture certificate](#-getting-the-hackyourfuture-certificate)
- [π¨πΎβπ» Authors](#-authors)
- [π License](#-license)

## π§ About <a name = "about"></a>

This repository is for Class15 Final Project - Rate my cv

Production website: https://rate-my-cv-production.herokuapp.com/

Staging website: https://rate-my-cv-staging.herokuapp.com/

## βοΈ Built Using <a name = "built_using"></a>

- [React](https://reactjs.org/) - Web Framework
- [NodeJs](https://nodejs.org/en/) - Server Environment
- [MySQL](https://www.mysql.com/) - Database
- [Express](https://expressjs.com/) - Server Framework - Server and Client side structure
- [Knex](http://knexjs.org/) - Database management
- [Swagger](https://swagger.io/) - API Documentation
- [Storybook](https://storybook.js.org/) - Tool for developing UI components in isolation
- [Prettier](https://prettier.io/) - Code formatter

## π Project's Calendar

_Class Dates_

- Week 1 β> 17-Jan-2021
  - Intro to Rate-my-cv
    - Main features
    - Who is it for?
  - Working in the final project
    - What is expected from you?
      - In my eyes you are web developers now!
        - In the start that can be a bit tough cause i expect a lot from you
      - Proactive
        - Fix things yourself (to a certain degree)
        - If you see something that could be improved then improve it!
      - No more teacing topics (you figure out how things work yourself)
        - Or maybe someone from the class studies a topic and teaches the rest of the class
      - Work together
  - How will the classes be run?
  - It is okay to make mistakes. But you have to learn from them
  - Reviewing each others PR's
    - [Review checklist](https://github.com/HackYourFuture-CPH/curriculum/blob/master/review/review-checklist.md)
  - There are lost of tasks not related to coding
    - Creating good PR's
    - Updating your story
    - Figuring out what your story is about
    - Linking issues with PR's
    - Testing
  - Practicalities
    - You will be surprised how little time you will be writing code
    - Small PR's!!!!!!!111!!11!!!!!!!!!!!!!
  - Communication
    - Very important
  - Getting the certificate: https://github.com/HackYourFuture-CPH/chattie/blob/develop/certificate.md
- Week 2 β> 24-Jan-2021
  - Overview of project (where is develop)
  - Version 1.0 should be everybodies focus
    - The different milestones: https://github.com/HackYourFuture-CPH/rate-my-cv/milestones
  - Talk about the checklist (linking story in PR, updating story in project board, checking files changed, testing etc)
  - Remember the focus. One story at a time. And the responsibility what do i need to worry about and what do i not need to worry about
  - How to remove something from files changed
    - If you want to remove whole file: `git checkout origin/master src/index.js`, then `add`, `commit` and `push` the change
    - If you want to remove specific line either change it back to the original or maybe try [this](https://stackoverflow.com/questions/6963129/is-it-possible-to-git-checkout-a-single-line-instead-of-the-entire-file)
  - Get latest changes into your branch:
    - Using an example of a branch called `user-login` with no files changes (remember to do `git status` and add changes to your branch before doing the changes below)
    - First checkout develop: `git checkout develop`
    - Then pull the latest changes on develop: `git pull`
    - Then checkout the branch you were working in: `git checkout user-login`
    - Then merge the latest changes from `develop` into your branch: `git merge develop`
- Week 3 β> 31-Jan-2021
  - Status of develop
  - Be respoctful of mentors time! Try figure it out yourself first (i definitely know you do that) If that is not working, reach out to a classmate, then maybe the support channels. Then if you still cannot figure it out the reach out to mentors. Study group
  - Restate the focus on Files changed and why it is so important
  - Start giving reviews to each other as classmates
  - Really good to see how you are working as a team! It makes me super happy and proud!
  
- Week 4 β> 7-Feb-2021
  - Knex Migrations && Seeding
  - PR Flow
  - Milestones
- Week 5 β> 14-Feb-2021
- Week 6 β> 21-Feb-2021
- Week 7 β> 28-Feb-2021
  Graduation Wednesday 3rd of March

## π©π»βπΌπ‘π¨π½βπΌ The Customer

HackYourFuture

#### πΌ Business Glossary

_Add here information about the Business Glossary_
[Business Glossary](/BusinessGlossary.md)

#### ποΈ Database Model Diagram

Check the DB Model Diagram [here](https://dbdiagram.io/d/6009d76480d742080a375e16)

- [How to make changes on the diagram](/diagram.md)

#### πΌ Mockup

Check the mockup [here](https://www.figma.com/file/0ST4EGb45fiNtMqFl4WgBc/Review-Resume)

Design style guide here: https://github.com/ghofranebenhmaid/review-resume/

#### πΌ Features

Go to the project board [here](https://github.com/orgs/HackYourFuture-CPH/projects/2/)

## π Process ππ

### π» Working with code

- ALWAYS run code before a PR is made.
- No committing `console.log`
- No committing merge conflicts!
- Work in separate files! When you make a new feature, the first thing you do is create a new file for that (of course if it makes sense). Especially for components.

### π§± Guidelines for building components

Generally there are 2 types of components: _presentational_ and _container_ components. Please review the differences below:

|                       | Presentational components                           | Container components                                                                                                                                                      |
| --------------------- | --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Also known as         | "dumb" components, functional stateless components  | "smart" components, stateful components                                                                                                                                   |
| Lives in this folder  | `/components`                                       | `/containers`                                                                                                                                                             |
| Purpose               | Determines what a component looks like              | Determines how the applications works                                                                                                                                     |
| Communication         | Can only communicate by receiving and passing props | Can communicate via props, can call APIs, can manipulate the DOM with REFs, etc.                                                                                          |
| Markup                | Contains most of the markup for the application     | Should generally have as little markup as possible. A container `<div>` or an `<ul>` tag is ok, but if you need more, consider making a separate presentational component |
| Storybook             | Can easily be mocked in Storybook                   | Cannot easily be mocked in Storybook, would require mocking API calls, etc.                                                                                               |
| Can have side effects | No                                                  | Yes                                                                                                                                                                       |  |

#### A note about React Hooks

These are general distinctions. In the past you could only make container components as class components as functions could not have state, but with React Hooks functional components can now have state. And with the addition of Context API components can easily communicate with their siblings and jump multiple steps in the hierarchy outside of how props are used to communicate between components. This is very powerful and can be convenient, but can easily make the application overly complex, so the advice is to stick to the separation between Presentational and Container components as closely as possible and only apply for example Context API where there is a justified need.

#### Proptypes

It is highly recommended, but not a requirement, to add proptypes to your components. Proptypes does two things:

- Give you an understandable error in the browser console when you try to use a component with wrong props specified.
- Provide a way for others to quickly reason about how to use your component when they read your code.

To add proptypes, simply import the proptypes package and specify exactly what data you expect your props to contain on the propTypes property of your component:

    ...

    import PropTypes from 'prop-types;

    ...
    [your component code]
    ....

    YourComponent.propTypes = {
      firstProp: PropTypes.string.isRequired,
      secondProp: PropTypes.number.isRequired
    }

Note the capitalization in the example above. It's easy to get wrong. Refer to the [proptypes npm package for further documentation](https://www.npmjs.com/package/prop-types).

#### Using Storybook

Checkout this great video from Zaki Wasik: https://www.youtube.com/watch?v=_AZhtGTWN8k

Storybook provides a _sandbox environment_ where it is easy to mock components in a visual way. When you create a _presentational component_ you should always add a story so it shows up in storybook. Benefits of using Storybook is:

- Clear overview of which components are implemented and which are not.
- Ability to experiment with applying different props to components to learn whether a given component could be used in another use-case.
- Makes it easier to perform a visual review of components (does it look like the original design?), as the reviewee would not have to put the application in a certain state to view the component (might otherwise involve performing SQL queries to populate the database and cleanup would also be required after).

Storybook runs as a separate web application parallel to the main application. Run storybook with the following command

    npm run storybook

The storybook application will become available on [http://localhost:3007](http://localhost:3007). From here you can browse and review the available components.

Some components may have "knobs" which are UI controls that allows you to interactively play with the props of a given component. It is up to the author of the component to set up knobs.

#### How to create a new story

Checkout this video: https://www.youtube.com/watch?v=jjH1cKGkt3o

The most basic way to create a story for your component is to put this code in your the stories file for your component (my-component.stories.js):

    import React from 'react';
    import MyComponent from './my-component.component';

    export default { title: 'Some title' };

    export const basicStory = () => <MyComponent firstProp={1} secondProp={2} />;

If you open Storybook, you should see your component under the headline "Some title".

You can have multiple Stories (i.e. multiple mutations of the same component) in your stories file. Just add another export. The story will take its name from the exported variable name:

    ...

    export const basicStory = () => <MyComponent firstProp={1} secondProp={2} />;
    export const advancedStory = () => <MyComponent firstProp={() => callMagicFunction()} secondProp={{ ...mysteriousObject }} />;

This will result in two stories under the headline "Some title".

You can also add folders to add hierarchical organization to your stories:

    ...

    export default { title: 'Secret Folder/Some title' };

    ...

##### Adding knobs (optional)

You can add "knobs", i.e. form elements that will allow you to interact with your component by manipulating props in real time, by importing `withKnobs` from the `@storybook/addon-knobs` package and using it as a decorator.

    import React from 'react';
    import MyComponent from './my-component.component';
    import { withKnobs, boolean, number } from "@storybook/addon-knobs";

    export default { title: 'CardLayouts/Status Card', decorators: [withKnobs] };

    export const WithKnobs = () => <MyComponent isTrue={boolean('Toggle is true', true)} theNumber={number('Change the number', 42)} />;

Boolean and number which are also imported are widgets to manipulate the props. Boolean will provide a simple true/false checkbox and number will provide a number input. But you can add [many different knobs](https://www.npmjs.com/package/@storybook/addon-knobs), including dropdown selects and color pickers.

#### Breaking down components

Always think about how you can break your UI into meaningful reuseable components. On one hand you want to be able to re-use your code as much as possible and on the other you want to avoid premature abstraction into components, meaning that you don't want to create a lot of components that are never actually re-used.

Please refer to [this article](https://reactjs.org/docs/thinking-in-react.html) for the basics about breaking UI elements into components.

#### Coding guidelines for components

1. When relevant pre-fix your component with the domain it is addressing. For example if it is a list showing motorcycles, call it `MotorcycleList`, not `ListMotorcycle`. This way components will be grouped by domain when sorted alphabetically in a folder. If it is a generic list component that can contain many things, omit the domain and call it `List`.
2. Put Presentational components in a folder inside `/Components` and postfix their name with `.component`.
3. Put container components in a folder inside `/Containers` and postfix their name with `.container`.
4. All assets (styles, test, stories) associated with a component lives in the component folder.
5. Postfix filenames with type of the file to make it easier to search for a given file in VSCode. Examples:
   - `/MotorcycleList/MotorcycleList.container.js`
   - `/MotorcycleCard/MotorcycleCard.component.js`
   - `/MotorcycleCard/MotorcycleCard.styles.css`
   - `/MotorcycleCard/MotorcycleCard.stories.js`
   - `/MotorcycleCard/MotorcycleCard.test.js`
6. File names should be `PascalCased`.
7. Component names (i.e. the name of the function in JS) should be `PascalCased` by general React conventions. Don't include `.component` or `.container` in the JS name.

### π¨ Theming and global styling

For global styles (i.e. styles that shall affect all components) use `src/client/index.css`. Global styles should be very rare and should typically be reserved for things like CSS resets, importing fonts and utilities.

For theming, use the file `src/client/theme.css`. Theming covers everything related to the visual presentation of the site that needs to be re-used often. That means colors, borders, paddings, shadows, etc.

### π§± Component styling

Components should always have a unique CSS class to make it easy to apply styles and styles. For example the "label" component should have a class "label". To easily concatenate different classes or apply classes conditionally, use the `classnames` npm package. Example of a label component that has a class "label" and will receive additional classes as props:

    ...
    import classNames from 'classnames';

    export default function Label({ title, className }) {
      return <span className={classNames('label', className)}>{title}</span>;
    }
    ...

Only put styling that is relevant to the individual component in the component CSS file. If it covers multiple components, put it in `theme.css` or `index.css`.

### π€ π₯ Inline CSS vs Stylesheets

Generally components should be styled using a dedicated stylesheet per component (see naming conventions in the section above). Exceptions can be made for values that are dynamically updated - i.e. a width that can any arbitrary value. If you need to change between two colors, apply css classes to the element in question style those classes and use react to switch out the css classes. For example:

    .label-primary {
      background-color: var(--primary-color);
      color: var(--white);
    }

### ππ½ Code best practices

Follow these best practices for coding: [HERE](https://github.com/HackYourFuture-CPH/curriculum/blob/master/review/review-checklist.md)

This can be used as a checklist for every PR you make. Go through the list and see if you have used all the best practices

### <img width=20px height=20px src="/git-logo.png" alt="GitHub logo"></a> Working with GIT

[Working with GIT](/working-with-git.md)

### <img width=15px height=30px src="/heroku-logo.svg" alt="Heroku logo"></a> Working with Heroku and Deployment

[Working with Heroku and Deployment](/deployment.md)

### <img width=59x height=20px src="/knex-logo.png"  alt="Knex logo"></a> Working with Knex and Migrations

[Working Knex and migrations](/knex-and-migrations.md)

### <img width=25px height=25x src="/swagger-logo.png"  alt="Swagger logo"></a> Working with API Documentation - Swagger

When running the API, you will automatically be running the API Documentation
which is based on Swagger. Just go to
[localhost:3000/api/documentation](http://localhost:3000/api/documentation) to
read the specifications for the API.

You can use your api token to authorize in Swagger and you will be able to
perform test calls against the API directly from Swagger.

If you need to make changes to the specification, this can be done via the
[Swagger.json](/src/server/config/swagger.json) file.

### <img width=20px height=20x src="/storybook.svg"  alt="Storybook logo"></a> Working with Storybook

Tool for developing UI components in isolation

Check here https://storybook.js.org/

### <img width=30px height=30x src="/aws.svg"  alt="AWS S3 logo"></a><img width=30px height=30x src="/s3.png"  alt="AWS S3 logo"></a> Working with AWS - Amazon Services

AWS is used for uploading files on a AWS S3 bucket. There is a user on the AWS that has `AmazonS3FullAccess`. There is not a AWS root key, but ONLY a key and a secret key for the AWS user.

If you need the key and secret to put into the .env file, write to the project manager of the project.

REMEMBER, this key should be kept super secret!!! NEVER add this to any PR!!

### Testing

To make a new test, add a `COMPONENT_NAME.test.js` to a component. See fx the `Home` component to get an example of a simple test.

To run all test, write this command:

`npm run test`

To run the tests when you change a test file, run:

`npm run test:watch`

### Making authenticated requests through firebase (useFetch hook)

#### What is it?

We created a small hook wrapper the `fetch` API to abstract away the authorization headers.

It also has some other bells and whistles to make data fetching simpler such as:

- loading state
- error state

#### Usage

Let's say I have a component which needs to fetch some data, this is how you could use it.

```javascript
function App() {
  const { response, loading, error } = useFetch(
    '[SOME URL HERE TO AN API ENDPOINT]'
    {} // here you can pass other options just like usual with the fetch API
  );
  const renderLoading = () => loading && <p>Loading...</p>;
  const renderError = () => error && <p>Something went wrong...</p>;
  const renderData = () => response && <p>{response.title}</p>;
  return (
    <div className="App">
      <h1>I want to loading some data</h1>
      {renderLoading()}
      {renderError()}
      {renderData()}
    </div>
  );
}
```

checkout the hook code here: [useFetch](src/client/hooks/useFetch.js)

## π Getting Started

First clone the repo on your local machine using a terminal or a git client.

#### πΎ [Installations](/installations.md)

##### Errors

If you get this error: `Error: ENOENT: no such file or directory, scandir`

Then try and run this script: `npm rebuild node-sass`

#### Code linting

To ensure we all code the same way, we are using linting in this project! We use prettier to do the linting for us. To Use the linting in this project, set your code editor up with the `.prettierrc.js` files.

In Visual Studio code, go to file -> Preferences -> settings -> Search for `prettier: config path` -> In the input write `.prettierrc.js`

## π [Getting the HackYourFuture certificate](/certificate.md)

## π¨πΎβπ» Authors

- [**Benjamin Hughes**](https://github.com/benna100)

## π License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
