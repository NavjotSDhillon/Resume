# How to Host Your Resume with Jekyll and GitHub Pages

Jekyll is a tool used to create static website that can be pushed to GitHub Pages. There are many Jekyll templates available online that supports GitHub Pages which can be used to create a website easily.

In this guide we will fork a Jekyll resume template, edit and run it locally. The changes will be then pushed to the GitHub repository. Then content in the repository is hosted on the GitHub Pages.

Click on the [link](https://navjotsdhillon.github.io/Resume/) to view the webpage.

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
    1. Go to the Setting tab.
    2. Verify under heading GitHub Pages if it gives a message that the site is successfully published and 'gh-pages' branch is selected.
    ![](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/Website_published.png?raw=true)
        > If the original developer is using CNAME, there will be an error message shown mentioning the CNAME. This error is shown because CNAME is the custom domain and there shouldn't be more than one repository with the same CNAME.  
    3. Click on the link which should be in format: `https://{GitHub_Username}.github.io/{Repository_Name}/`  
        > Note: It may take few minutes for the website to load.
  
### How to run the website locally?
After successfully running the website with the template resume on GitHub Pages, run the webpage on the local machine using Jekyll server. It is good idea to run it locally so that you can easily make changes and verify the changes locally without pushing the changes to the github repository. To run the website locally:
1. Clone the repository on your local system.
2. After cloning, go to the project folder in your CLI and run the following commands to start the Jekyll server:
  ```
  $bundle install
  $bundle exec jekyll serve
  ```
  > The `$bundle install` command is required only once whereas to run the server jekyll serve you need to enter `$bundle exec    jekyll serve` command every time.  

  > There maybe a scenario where the bundle install may fail to install a dependency but try reinstalling that dependency         using the link provided in the error.
4. From the terminal there is a server address that is provided in the CLI. Mostly it is http://127.0.0.1:4000 or http://localhost:4000
![](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/Jekyll_Server_Start.png?raw=true)

### Where to update the content of the resume?
After running the template successfully on the local system, make changes in different files like \_config.yml and all files in folder \_data. The changes required varies from template to template but will mostly be in the mentioned files. Most changes are in the files with extension `yml` which can be opened using different text editors like Atom. Here are the different required changes in the files to make this resume your own:
1. Update the information like name, title, links in \_config.yml file that gets displayed on the webpage.
2. Enable or disable different configurations in \_config.yml file to hide or show different sections of the resume.
3. Update the image if required by simply replacing the image with the one that is more appropriate in the images folder.
4. Update the content of different sections of the resume under the \_data folder.
   - There might be a single or multiple YAML files that covers different sections of the resume.
   - Update the values for each key-value pairs. Comment the key-value pair that is not required.
   - Depending on the content you need to insert into that section, the object of that sectioned can be inserted or removed (In screenshot below, each of these green boxes represent different objects of the section)
   ![](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/Objects.png?raw=true)

### What to do once the changes are made?
After the resume is updated, upload the changes to the GitHub repository. Once the repository is updated with new content, use the link used previously to load the webpage using GitHub Pages. You Resume is now published online using Jekyll and GitHub Pages.

## More Resources
Tutorial to learning more about Jekyll and hosting the webpages on GitHub Pages - https://www.mikedane.com/static-site-generators/jekyll/

## Author and Acknowledgements
[Jekyll brief installtion guide](https://jekyllrb.com/docs/)  
[Jekyll Resources with all the links](https://jekyllrb.com/resources/)  
[Joel Glovier's Template](https://github.com/jglovier/resume-template) (Resume template used in this guide)
Group Members -
  - Wahegurupal Mankoo
  - Dilawer Hussain

## FAQs
Q - Why the changes are not reflected when the page is reloaded locally?  
A - If the changes are made in the \_congif.yml file, then the server is required to be restarted. If the changes are made in any other file, then there is a high possibility of a syntax error in the changes that were made. Review the changes.

Q - How to fix the issue if `ffi` installation is failing while installing the bundle?  
A - Try to manually install `ffi` using the link given in the error. If it is failing again, refer to paulomcnally's comment on this [link](https://github.com/ffi/ffi/issues/611#issuecomment-364621532).
