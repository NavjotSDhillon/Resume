# How to Host Your Resume on GitHub Page

Jekyll is a tool used to create static website that can be pushed to GitHub Pages. There are many Jekyll templates available online that supports GitHub Pages which can be used to create a website easily.

In this guide we will fork a Jekyll resume template, edit and run it locally. The changes will be then pushed to the GitHub repository. Then content in the repository is hosted on the GitHub Pages.

## Audience

This tutorial is targeted for those who have some or more experience in using Atom( or any other text editor that supports YAML and markdown), GitHub and Markdown. There is no prior experience required in Jekyll.

## Prerequisites

There are few requirements that are required to be met before Jekyll could be installed. Verify if these dependencies are already installed and have the required version using the provided Command Line Interface(CLI) commands:
  - Git: `git --version`.

  - Ruby version 2.4.0 or above: `ruby -v`

  - RubyGems: `gem -v`

  - GCC: `gcc -` and `g++ -v`

  - Make: `make -v`

[Here](https://jekyllrb.com/docs/installation/) is the guide that needs to be followed for installing Jekyll and for any of the missing dependencies.

## Instructions
### How to initially setup GitHub Pages?
1. Find a Jekyll theme online that supports GitHub Pages.
    > Here are few links where you can find templates:
    > - https://jamstackthemes.dev/ssg/jekyll/
    > - http://jekyllthemes.org/
    > - https://jekyllthemes.io/
2. Fork the chosen pre-existing Jekyll theme to get the copy in your own repository.
3. Rename the forked repository based on the requirement.
![](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/GitHub_Forking.gif?raw=true)
4. Verify if the branch is 'gh-pages'. If not then create the branch named 'gh-pages'.
4. Verify if the template is setup and runs properly in the GitHub Pages by following these steps:
  a. Go to the Setting tab.
  b. Verify 
4. Run the forked template to see if there are no issue running the template.
5. To run the template, go to settings tab in github. Under heading GitHub Pages, check if the site is successfully published. If not follow the instructions provided.
6. The most common issue is that the original developer maybe using a CNAME which can't be same for any two repositories.

### How to run the website locally?
1. Clone the repository locally to update the resume.
2. After cloning, go to the project folder using terminal and run the following commands to start the Jekyll server:
```
$bundle install
$bundle exec jekyll serve
```
3. There maybe a scenario where the bundle install may fail to install a dependency but try reinstalling that dependency using the link provided in the error.
4. From the terminal there is a server address that is provided in the terminal. Mostly it is http://127.0.0.1:4000 or http://localhost:4000

### Where to update the content of the resume?
1. After successfully running the template locally, make the required chanegs in \_config.yml like updating the name and other information.
2. There are other settings also like enabling or disabling the different parts of the template like any section or images.
3. If the template uses an image, then simply replace the image with the one that is more appropriate. The images might be under images folder in the root directory of the project.
4. Update the content of the resume under the \_data folder.
5. There might be a single or multiple YAML files used depending on the resume structure.
6. Update the values in the key-value pair and add/remove the number of parts required.

### Final 
1. After doing all the changes, commit and push the repository to the GitHub.
2. Run the GitHub Pages link for that repository to verify if the website is running correctly.

## More Resources

Tutorial to learning more about Jekyll and hosting the webpages on GitHub Pages - https://www.mikedane.com/static-site-generators/jekyll/

## Author and Acknowledgements

https://jekyllrb.com/docs/
https://jekyllrb.com/resources/
Resume used - https://github.com/jglovier/resume-template ([Joel Glovier](https://github.com/jglovier/))  
Group Members -
  - Wahegurupal Mankoo
  - Dilawer Hussain

## FAQs

Q - Why the changes are not reflected when the page is reloaded locally?
A - If the changes are made in the \_congif.yml file, then the server is required to be restarted. If the changes are made in any other file, then there is a high possibility of a syntax error in the changes that were made. Review the changes.

Q - Why the changes made in the \_config.yml file not reflected in the website running locally.
A - When changes are made to the config files the server is required to be restarted.
