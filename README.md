# How to Host Your Resume with Jekyll and GitHub Pages

Jekyll is a static site generator which is used to create websites that can be hosted via GitHub Pages. There are many Jekyll templates available online that support GitHub Pages which allow for an easy updates of content.

In this guide we will:
- Fork a Jekyll resume template
- Edit and run it locally
- Host it on GitHub Pages

We will be creating a [Single Page Resume](https://navjotsdhillon.github.io/Resume/).

## Audience

This guide is targeted for those who have some or more experience in using GitHub, Markdown, and Atom (or any other text editor that supports YAML and markdown). There is no prior experience required to work with Jekyll.

## Prerequisites

This [Official Documentation](https://jekyllrb.com/docs/installation/)  provided by the creators of Jekyll can be used to ensure all dependencies are installed and up to date, along with their specific versions.

There are a few requirements that need to be met before Jekyll can be installed. You must verify that these dependencies are  installed properly and have the required version using your Command Line Interface (CLI) commands:

  - Git: `git --version`.

  - Ruby version 2.4.0 or above: `ruby -v`

  - RubyGems: `gem -v`

  - GCC: `gcc -` and `g++ -v`

  - Make: `make -v`

## Instructions
### How to setup GitHub Pages?
Firstly, find a Jekyll theme online that supports GitHub Pages.
  > Here are few links where you can find templates
  > - https://jamstackthemes.dev/ssg/jekyll/
  > - http://jekyllthemes.org/
  > - https://jekyllthemes.io/  
  
Once you find the template that fits your requirements, follow these instructions to host that template on your GitHub Pages:

1. Fork the chosen Jekyll Themes repository to get the copy in your own repository.

2. Rename the forked repository based on your preference.

![](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/GitHub_Forking.gif?raw=true)

3. Ensure if the branch is set to 'gh-pages'. If not, then create a new branch and name it 'gh-pages'.

4. Verify if the template is setup and runs properly in the GitHub Pages by following these steps:

    1. Go to the Setting tab.

    2. Verify under GitHub Pages section in your repository settings. If you see a message that that says, "Your site is published at {your url}". That means your Jekyll Theme successfully compiled.
    ![Website URL](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/Website_published.png?raw=true)

        > If the original developer is using CNAME, there will be an error message shown mentioning the CNAME. This error is shown because CNAME is the custom domain and there shouldn't be more than one repository with the same CNAME.  
    3. Click on the link which should be in format: `https://{GitHub_Username}.github.io/{Repository_Name}/`  
        > Note: It may take a few minutes for the website to load.

### How to run the website locally?
After successfully running the website with the template resume on GitHub Pages, you can also run the website locally using Jekyll. It is a good idea to run it locally so that you can easily make changes and verify the changes locally without pushing the changes to the GitHub repository.

To run the website locally:
  1. Clone the repository on your local system.

  2. After cloning, `cd` into the project folder in your CLI and run the following commands to start the Jekyll server:
  ```
  $bundle install
  $bundle exec jekyll serve
  ```
  > The `$bundle install` command is required only once.
  > To run the server enter `$bundle exec jekyll serve` command every time.  
  3. In the output of the previous command, there is a server address that is provided. Usually it is http://127.0.0.1:4000 or http://localhost:4000 (localhost on port 4000)
  ![](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/Jekyll_Server_Start.png?raw=true)

### Where to update the content of the resume?
After running the template successfully on the local system, make changes in different files like `\_config.yml` and all files in folder `\_data`. The changes required varies from template to template but will mostly be in the mentioned files. Most changes are in the files with extension `yml` which can be opened using different text editors such as Atom.

Here are the different required changes in the files to make this resume your own:
1. Update the information such as your `name`, `title`, `links` in `\_config.yml` file that gets displayed on the webpage.

2. Enable or disable different configurations in `\_config.yml` file to hide or show different sections on the website.

3. Update the image if required by simply replacing the image with the one that is more appropriate in the images folder.

4. Update the content of different sections of the resume under the `\_data` folder.
   - There might be a single or multiple `YAML` files that covers different sections of the resume.
   - Update the values for each `key-value` pairs. Comment the `key-value` pairs which are not required.
   - Depending on the content you need to insert into that section, the object(s) of that section(s) can be inserted or removed (As show in the screenshot below, each of these green boxes represent different objects of the specific sections)
   ![](https://github.com/NavjotSDhillon/Resume/blob/gh-pages/Objects.png?raw=true)

### What to do once the changes are made?
After the resume is updated, upload the changes to the GitHub repository. Once the repository is updated with new content, use the link used previously to load the webpage using GitHub Pages. You Resume is now published online using Jekyll and GitHub Pages.
Finally, create a `README.md` file in markdown to give the description of the project, acknowledgements and any other important details.
  > The `README.md` will be in the main directory of the repository. It can be editted locally using Atom and pushed back again or can be edited directly in GitHub.

## More Resources
Here are a few useful links which are great for learning more about:
 - [Markdown](https://github.github.com/gfm/)
 - [Jekyll and hosting the webpages on GitHub Pages](https://www.mikedane.com/static-site-generators/jekyll/)

## Author and Acknowledgements
[Jekyll Resources with other useful links](https://jekyllrb.com/resources/)

[Jekyll brief installtion guide](https://jekyllrb.com/docs/)    

[Joel Glovier's Template](https://github.com/jglovier/resume-template) (Resume template used in this guide)

Group Members:
  - Wahegurupal Mankoo
  - Dilawer Hussain

## FAQs
#### Q. - Why the changes are not reflected when the page is reloaded locally?  
A. - If the changes are made in the `\_congif.yml` file, then the server is required to be restarted. If the changes are made in any other file, then there is a high possibility of a syntax error in the changes that were made. Review the changes.

#### Q. - How to fix the issue if `ffi` installation is failing while installing the bundle?  
A. - Try to manually install `ffi` using the link given in the error. If it is failing again, refer to paulomcnally's comment on this [link](https://github.com/ffi/ffi/issues/611#issuecomment-364621532).
