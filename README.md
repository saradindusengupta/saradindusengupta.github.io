A Github Pages for Software Developers, Data Scientist and Researchers. This was forked from originally [Barry Clark](https://github.com/barryclark/jekyll-now) and then added themes and components from the [Academic Pages](https://github.com/academicpages/academicpages.github.io),  See LICENSE.md.

In this version Travis CI is added for monitoring build issues and code scan is enabled for monitoring quality checks from PRs.

### Note: if you are using this repo and now get a notification about a security vulnerability, delete the Gemfile.lock file. 

# Instructions

1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
2. Fork [this repository](https://github.com/saradindusengupta/saradindusengupta.github.io) by clicking the "fork" button in the top right. 
3. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL unless you want to use your own custom domain for this github page [ To see on how to get your personal domain and attach it to this Github Page see below].
4. Set site-wide configuration and create content & metadata in the file `_config.yml`. [Optional] Change the theme from the Settings tab. 
5. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
6. Check status by going to the repository settings, in the "GitHub pages" section


See more info at https://saradindusengupta.ml/

## To run locally (not on GitHub Pages, to serve on your own computer)

1. Clone the repository and made updates as detailed above
1. Make sure you have ruby-dev, bundler, and nodejs installed: `sudo apt install ruby-dev ruby-bundler nodejs`
1. Run `bundle clean` to clean up the directory (no need to run `--force`)
1. Run `bundle install` to install ruby dependencies. If you get errors, delete Gemfile.lock and try again.
1. Run `bundle exec jekyll liveserve` to generate the HTML and serve it from `localhost:4000` the local server will automatically rebuild and refresh the pages on change.

## Setting up Custom Domain and enabling HTTPS
The best free custom domains can be acquired from [Freenom](https://www.freenom.com/en/index.html?lang=en). Before this your Github Pages repository should be set up.
### Steps
1. Signup for an Account
2. Choose one of the free domain names. ('.ml','tk' domains are generally free)
3. Register for the the domain and wait for 5 to 10 minutes for confirmation
4. Log back in and go to your 'My Domain' page -> 'Manage Domain' Settings and add the following entry 
   
|  Type|TTL  |Target
|--|--|--|
|  A|  14400|185.199.108.153
|A|14400|185.199.109.153
|A|14400|185.199.110.153
|A|14400|185.199.111.153
|CNAME|14400|saradindusengupta.github.io 
5. Add the domain name in your Github Pages repository settings option under `Custom Domain`. Enable HTTPS tick mark and Give 30 to 40 minutes to SSL certificates being assigned and distributed. This will also create a `CNAME` file in root of the project directory.
   
For in depth understanding and further trouble shooting follow the official docs at [Github Docs](https://docs.github.com/en/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site)
# Changelog -- bugfixes and enhancements

All the change logs can be found [CHANGELOG](CHANGELOG.md)
