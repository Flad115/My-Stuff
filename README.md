# Always include a README in your projects

<div align="center"><img src="./langan-polygon.svg" /></div>

## Good Habits

- Include a README markdown file in you projects
- Use the [Prettier extension](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) to format your documents, especially your code files.
- Use [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) to check spelling in your documents.
- Use [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint) to find potential problems with your JavaScript before you run it. To use this extension you will need to install ESLint. Read the instructions on the link above to learn how to do this.

## Notes

- These are three tools that, in the long run, will make your life much much easier. These are not the only tools you will eventually come to rely on but I wanted to nudge you in the direction of adopting tools when it makes sense to do so.
- Like any new tools, however, they come with a learning curve. Trust me, they are well worth it and you would discover that on your own in time once you understand the problems they solve. I will provide a brief description of a problem that each of these tools solve.
- `Prettier:` This tool formats your code. For example, it decides how many spaces are used for indentation and it is NOT configurable. You might not think this is a big deal at first but consider what happens if you have two developers working on the same project.
  - Developer Tom uses four spaces for indentation because he knows really big indents are best for readability. Developer Dylan, on the other hand, uses two spaces for indentation because he knows that all that white space is inefficient.
  - Now, like I said, they are both working on the same project. Furthermore, they are also using git to track code changes and using Github as their central repo for the project. Every time Tom edits a file he uses his preferred indentation. In fact, he has his environment set up to "fix" all indentation on file save. Dylan has also implemented this "time saving" strategy. You see where this is going. Every time either developer pushes their changes to the central repo it appears that they have altered every single line of every file that they saved, even if they had made no changes.
  - If Tom makes changes to a file and pushes it to the repo and then, a little later, Dylan tries to push his changes to that file to the repo Github will refuse as their is a conflict that needs resolution. At this point Tom & Dylan get into a heated debate over what indentation is best waisting time and energy on a decision that can be made by a tool. That tool is Prettier!
  - I can't tell you how many times I have seen developers waisting time debating what the best way to format their code is. Who cares! That's not what's important. What is important is that there is a standard that is enforced so all code bases look consistent and we should be debating what the code does, not how it is formatted.
- `cSpell:` This one is obvious, it just highlights misspelled words. It is also more clever than that.
  - For example, developers often use camel case or snake case to name variables. Consider these two JavaScript variable declarations:
    ```
    var someVariableName = "camel case variable name"
    var some_other_variable_name = "snake case variable name"
    ```
    In each case cSpell will consider these two variable names to be properly spelled words as each of the pieces of the variable names are properly spelled.
  - Also, you can used directives to tell cSpell that some misspellings should be allowed or that whole sections of a file should be ignored.
  - Suffice it to say, misspellings will always occur and its nice to have cSpell watching your back.
- `ESLint:` ESLint is much more complicated than Prettier and cSpell. I am not going to try to describe for you that much of what it does but trust me, it is a must.
  - There is overlap between ESLint and Prettier because ESlint will also try to enforce code formatting rules. Whenever I am using them together which is pretty much in serious project I configure ESLint to defer to Prettier for code formatting.
  - [Here](https://medium.com/@dhinesh4668/a-comprehensive-guide-to-eslint-from-basics-to-advanced-4defc05800e0) is a nice and fairly brief description of ESLint.
