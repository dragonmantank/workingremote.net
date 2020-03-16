# workingremote.net
Backend and content for WorkingRemote.net

This repo will house all the content and code for the website. For the moment, please submit a Github issue with a link to the article/twitter thread/whatever that you think will be useful for people.

If you would like to write something directly, feel free to either post to your personal blog and submit a link, or create a github issue with the content in Markdown form and I'll get it worked in once the content backend is set up.

Feel free to also provide any other feedback or help, this website is open source under the GPL v3.

## Adding Content

There are three ways that you can add content to this website

1. Write an article yourself and post it to your personal blog. You can then submit an issue and we'll slot it into one of the sections of the site.
2. Submit an article, in markdown, as an issue. We'll work with you on getting it put into the site if it is deemed appropriate.
3. Fork this repository and submit a Pull Request with the changes. This is a more involved process, but is more appropriate for larger changes like layout or new sections.

### Forking and Pull Requests

If you would like to fork and submit a full pull request, feel free! The site is built using [Sculpin](https://sculpin.io/), a static site generator. All written content resides in the `source/` folder. New sections are made by creating a new Markdown file in the `source/` folder.

### Building the Website Locally 

You can view how your changes affect the site by building the website locally. It requires PHP and NPM to be installed locally on your computer. To build the website:

1. Run `composer install` to download the PHP dependencies
2. Run `npm install` to download the NodeJS dependencies
3. Run `composer run --timeout=0 serve` to build and start the website
4. Visit `http://localhost:8000` in your browser!

A couple of notes, however:

- Changes to `src/css/main.css` will not be picked up by Sculpin, you will need to stop the server with CTRL+C and restart it
- Sometimes new templates and layouts are not picked up, so you may need to restart the server
- By default, Sculpin does not clear out it's output directory, so you may want to stop and restart the server to flush out old content if you move content to new files

## Built Using

- [Sculpin](https://sculpin.io/)
- [Tailwind CSS](https://tailwindcss.com/)