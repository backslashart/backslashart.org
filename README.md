# backslashart.org

Backslash Art website.

Production:
https://backslashart.netlify.app/

Preview:
https://preview--backslashart.netlify.app/

# Changes from previous repo

- Update to Jekyll 4.2.2
- Update to Ruby 3.1.2
- Moved content pages to `_pages`
- Fixed 404 page
- Tested Netlify deploy
- Tested making edits with Github Codespaces

# Making edits

<details><summary>Using Github (Recommended)</summary>

1. Open [the repo](https://github.com/jbakse/backslashart.org) on github.
2. Switch to the preview branch.
3. Use the Github editor to edit content on a page. Commit edit with pithy commit message.
4. See changes on https://preview--backslashart.netlify.app/
5. Issue pull request to request your changes be merged into `main`.
</details>

<details><summary>Using Codespaces</summary>

1. Navigate to the repo on Github
2. From the `Code` button dropdown choose `Codespaces` > `Create Codespace`

   This should open a new browser tab with VS Code running in a "codespace". The process hung for me, but a browser reload quickly fixed it.

3. Make some edits

   A good place to make some test edits is `_pages/test.md`

4. Run Jekyl locally to preview your edits
   `bundle install`
   `bundle exec jekyll serve`

5. Commit your edits

6. Netlify should deploy your changes.

   This typically takes 1 to 5 minutes.

   See your changes at https://backslashart.netlify.app/

   You can also work in a branch if you want to preview your changes without publishing to the main site.

</details>
   
# Deploying with Netlify

This site is deplyed with Netlify. When new commits are added to the `main` branch, netlify automatically pulls the changes, rebuilds the site with Jekyll, and publishes at https://backslashart.netlify.app/

# Build and run locally or on Codespace

You may wish to see your changes as you work, before making a commit and deploying with Netlify. You can run Jekyll locally for a fast development cycle. You will need Ruby installed. Tested with ruby 2.7.2 and ruby 3.1.2

```bash
bundle install
bundle exec jekyll serve
```

If you are running locally, open 127.0.0.1:4000 in a new browser tab.

If you are running in the codespace, a prompt should appear to open a tab to the server.

Jekyll will watch your content pages for changes and rebuild automatically. The browser is not reloaded automatically, so you need to manually reload to see your changes.
