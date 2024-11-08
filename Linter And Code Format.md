# Linter And Code Format

## 1. Introduction

You know that each person is unique in their own way, and the same goes for the code. Some people prefer to write code in a certain way, and some people prefer to write code in another way. We cannot change the way other people think, but since working in a team is a must in the real world, we need to find a way to make everyone's code follow the same standard that is easy to understand and maintain.

## 2. Linter

A linter is a tool that helps us to catch errors and enforce code standards. It might not be able to catch all the errors, but it can ensure that everyone's code follows the same standard that specified for each project.

For JavaScript and TypeScript, the most popular linter is ESLint. It has a lot of plugins and configurations that you can use to enforce code standards for your team, and the configurations can be changed to fit the project's needs. Plus, they are run as a script, so ESLint will always follow the rules that we specified, therefore ensuring that everyone's code matching the rules.

Read more about ESLint [here](https://eslint.org/).

## 3. Code Format

Unlike linter that catches errors, code format is about making the code more readable and consistent. It doesn't catch any errors, but it ensures that the code format is on par with the team's standard.

For JavaScript and TypeScript, the most popular code formatter is Prettier. Same as ESLint, Prettier has a lot of configurations that you can use to enforce code standards for your team, and the configurations can be changed to fit the project's needs. Combine with ESLint, you can ensure that the code is both error-free and formatted consistently. No more arguing over tabs vs spaces.

Read more about Prettier [here](https://prettier.io/).


## 4. Additional Tools

Combine both ESLint and Prettier, there are some additional tools that you can use to make the development process more efficient.

### 4.1. Husky

Husky is a tool that allows you to run scripts before committing your code. You can use it to run ESLint and Prettier before committing your code, so you can catch errors and format the code before the code is committed.

Read more about Husky [here](https://typicode.github.io/husky/#/).

### 4.2. Using CI/CD pipeline

Most of the time, we will use a CI/CD pipeline to run the linter and formatter scripts before merging the code to the main branch. Since this is run on the server side, team members will have to pass the CI/CD pipeline before their code can be merged. This ensure that they don't do awkward things like bypassing the linter and formatter in their local environment and push bad code to the branch with the hope of getting it merged. 

For me, this is a must in any project that I work on. Read more about how CI/CD pipeline works [here](https://www.redhat.com/en/topics/devops/what-is-ci-cd).

## 5. Conclusion

Linter and formatter are powerful tools that can help us to catch errors and enforce code standards. They are not a replacement for testing, since we can still write bad code login that still passes the check. But if it formatted correctly, it will be easier for other people to understand the code, thus fixing it should be a breeze.