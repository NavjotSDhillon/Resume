# How to Host Your Resume on GitHub Page

This tutorial is for hosting a resume to GitHub pages by using Jekyll templates to stylize the resume.

### Audience

This tutorial is for those who have some or more experience in using Atom, GitHub and Markdown with no prior experience in Jekyll.

### Prerequisites

- Create a GitHub account.
- Install Jekyll by following the guide on this [link](https://jekyllrb.com/docs/installation/) for different Operating Systems if not already installed. Jekyll requires Ruby, RubyGems and GCC and Make for which the guide is already provided in the given link.

### Instructions

1. Find a Jekyll theme online that supports GitHub Pages.
2. Fork the pre-existing Jekyll theme to get your own copy.
3. Rename the forked repository if required.
![](GitHub_Forking.gif)
4. Run the forked template to see if there are no issue running the template.
5. To run the template, go to settings tab in github. Under heading GitHub Pages, check if the site is successfully published. If not follow the instructions provided.
6. The most common issue is that the original developer maybe using a CNAME which can't be same for any two repositories.
7. Clone the repository locally to update the resume.
8. After cloning, go to the project folder using terminal and run the following commands to start the Jekyll server:
```
$bundle install
$bundle exec jekyll serve
```
9. There maybe a scenario where the bundle install may fail to install a dependency but try reinstalling that dependency using the link provided in the error.
10. From the terminal there is a server address that is provided in the terminal. Mostly it is http://127.0.0.1:4000 or http://localhost:4000
11. After successfully running the template locally, make the required chanegs in \_config.yml like updating the name and other information.
12. There are other settings also like enabling or disabling the different parts of the template like any section or images.
13. If the template uses an image, then simply replace the image with the one that is more appropriate. The images might be under images folder in the root directory of the project.
14. Update the content of the resume under the \_data folder.
15. There might be a single or multiple YAML files used depending on the resume structure.
16. Update the values in the key-value pair and add/remove the number of parts required.

17. After doing all the changes, commit and push the repository to the GitHub.
18. Run the GitHub Pages link for that repository to verify if the website is running correctly.

### More Resources

Detail tutorial for Jekyll integration with GitHub Pages - https://www.mikedane.com/static-site-generators/jekyll/

#### Author and Acknowledgements

Resume used - https://github.com/jglovier/resume-template ([Joel Glovier](https://github.com/jglovier/))  
Group Members -
  - Wahegurupal Mankoo
  - Dilawer Hussain

### FAQs

Q - Why the changes are not reflected when the page is reloaded locally?
A - This happens when there is a syntax error in the changes that were made. Review the changes.

Q - Why the changes made in the \_config.yml file not reflected in the website running locally.
A - When changes are made to the config files the server is required to be restarted.
