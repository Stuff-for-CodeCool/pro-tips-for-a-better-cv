# Pro Tips for a Better CV
You are preparing to become a professional developer. Congratulations!
As we all know, while your technical skills are important (and indeed what you will be using in your career as a developer), it is *at least* as important to be able to show off these skills. After all, in order to demonstrate what you know, you must first *advertise* what you know.
Fortunately, you've had a year's worth of experience, as evidenced by all the projects built during your CodeCool TeamWork weeks.
Of course, these projects are private, so you will not be able to show them off as-is. The material, however, belongs to *you*, so there is no restriction to what you can do with it.
What you *should* do with it is to put these projects on your personal github profiles.
## Putting a repo on your Github profile
First of all, you will want to clone the repo from the CodeCool repo. To do this, simply `git clone` the repo.
Then, on your Github profile, create a new repository with the appropriate name (for instance, `askmate`). Make sure this repo is set to **Public** (you can check this in an incognito window). In the folder where you've cloned the CodeCool repo, open a new terminal, and add the new remote:
```shell
git remote add codecool https://github.com/you-username-here/your-cc-repo-here
```
Set the current branch as main if it's not (`git branch -M main`) then merge the CodeCool branch into it:
```shell
git checkout main
git merge codecool/development
```
Solve any conflicts that might arise, then *make sure you clean up the repo*.
This is important. This code is what any potential employer will see, and you will want to make a good impression.
So, in order:
1. Delete any files/folders that are not needed
2. Anything that gets automatically generated but is not strictly needed to get the project going goes in the `.gitignore` file. This means virtual environments, cache files, build folders, IDE configurations, that sort of thing. Unsure of what this file should contain? [Have a look here](https://github.com/github/gitignore). This file can be also [created automatically](https://elanderson.net/2020/10/add-git-ignore-to-an-existing-visual-studio-solution-new-git-experience/), if you use Visual Studio.
3. `git add`, `git commit` with relevant and descriptive commit messages.
4. Any system-centric variable goes in a `.env` file. Do not leave API keys, users/passwords or any other project-specific data lying around, put it all in `.env`. This file will *also* go into `.gitignore` because you don't want to expose sensitive data.
5. If you've created an `.env` file, also create a `.env.template` file. This will have all the keys needed and none of the values, and also it does NOT go into `.gitignore`. Its purpose is to help whoever wants to set up a copy of your project, by indicating which system variables the project expects.
6. `git add`, `git commit`
7. Do you use a database? Clean up all the non-essential info, any test users (but maybe leave a guest account if needed), any lorem ipsum that might be there, then export the relevant SQL data into an `sample_data.sql` file. Add this file to the repo.
8. `git add`, `git commit`
9. Run your project again, making sure everything does what's expected and there are no bugs. If there are any, fix them now.
10. `git add`, `git commit`
11. If you're generating any HTML files, run them through a code validator. [W3C's Unicorn](https://validator.w3.org/unicorn/#validate-by-input+task_conformance) is your best bet. Fix any errors indicated.
12. `git add`, `git commit`
13. All the code should go through a linter. This will ensure your code is properly formatted, documented, and lacking any "spontaneous undocumented features" (ie, bugs).
14. `git add`, `git commit`
15. Did you refactor your code? Refactor again. Clean code is never clean enough. Make sure you follow naming conventions. You can find Google's recommendations [here](https://google.github.io/styleguide/). Just look up the appropriate language, and search the naming conventions.
16. `git add`, `git commit`
17. Finally, show some love to your `README.md` file. What should go in there? What the rationale behind the project is, a short description, technologies used (PRO TIP: nobody cares what IDE you've used or how you've communicated with your team. Put in the languages used, any external applications (JAVA, Python, PostgreSQL, mongodb, that sort of thing), system requirements and such). Be sure to add step-by-step installation instructions.
18. `git add`, `git commit`
Once you've done all that and are fairly happy with the project and feel anyone is able to install it on their machine, push it to your Github repo.
Now do this for all other projects you've enjoyed and/or are proud of.
 
## Showing contributions to private repos
 
Most of your commits will not be visible on your profile page, as they will be made to private repos. In order to show that you have, in fact, committed things, you will need to follow the steps outlined [here](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/publicizing-or-hiding-your-private-contributions-on-your-profile).
## What's better than a CV?
Simple: a proper Github profile. Ain't nobody got time to look through documents, if a simple click will reveal the same information.
So, head back to github. Create a new repo, *with the same name as your github username*.
This magic repo will contain at least a `README.md` file.
This is where your CV's contents go. This is what people will see when they access your github profile.
The file itself is formatted using `markdown`. By now you should be familiar with the syntax, but just in case you're not, [this is where you can learn it](https://www.markdownguide.org/getting-started/).
It might help to add some github-specific stats to your profile. These can currently be found [here](https://github.com/anuraghazra/github-readme-stats). Implement them in your `README.md`, but don't go overboard with the options. Remember, *less is more*.
Add, Commit, Push, then stare in wonder at your shiny new github profile.
 
 