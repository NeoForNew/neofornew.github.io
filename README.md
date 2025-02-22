This website is built from the template of [academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io) and my operating system is macOS. It was my first time using Jekyll so I took around 1h to set up the environment even though I am familiar with Git and installation packages on MacOS. The target of this post is to summarize my steps and can be referred to by readers with limited computer knowledge.

# Instructions
## Github Setting
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Clone your forked repo under your repos.
1. Go to the repository's settings (the rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io" under the setting, which will also be your website's URL.
1. Check the status by going to the repository "Settings". In the "Pages" section, choose source "Deploy from a branch" and select "master", "/root" under "Branch". Click "save".
See more info at [academicpages.github.io](https://academicpages.github.io/)

## Package installation
open terminal in your apps.
follow the following tutorial to install brew, jekyll and so on:
[Jekyll Installation for macOS](https://jekyllrb.com/docs/installation/macos/).
You should also install bundle after the above setup
By running:

`gem install jekyll bundler`

### Debug info

error: bundler: failed to load command: jekyll (/Users/jrdnbwmn/.rbenv/versions/3.0.2/bin/jekyll)
eval (eval at <anonymous> ((execjs):1:213), <anonymous>:1:10): TypeError: Cannot read property 'version' of undefined (ExecJS::ProgramError)
- solution command: `bundle add webrick`

For other error: you can search on stackoverflow or ask chatgpt using a prompt like'debug ...'

## Run command in your terminal
1. run `cd path-to-your-cloned repo/` (replace path with your own path)   
1. Run `bundle clean` to clean up the directory (no need to run `--force`)
1. Run `bundle install` to install ruby dependencies. If you get errors, delete `Gemfile.lock` and try again.
1. Run `bundle exec jekyll liveserve` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on 
### Debug info
error: when running 'bundle exec jekyll liveserve'
- solution command: `bundle exec jekyll serve`

## Edit your project
- If you are familiar with Git, it is recommended to edit all the contents on your local computer and then push your project to the remote repository.
- If you are not familiar with Git, you can edit the files directly in the web user interface.

For both cases, it is recommended to read the instructions provided by [academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io). You do not need to learn a new programming language. Simply follow their example files to create your own website content. If you are not familiar with Markdown, you can ask ChatGPT to assist you in formatting the files into Markdown format. **Notion** is also a good tool to generate Markdown format files.

If you have any additional inquiries, the first step is to consult ChatGPT or utilize Google for assistance. Should you encounter further difficulties, please don't hesitate to send me an email. Make sure to provide a thorough description of the error information and include details about your operating system. 

If you are not fond of this template, you can explore other templates on GitHub that suit your preferences. Many personal websites are built using jekyll, and you typically won't need to reinstall any additional packages for them.