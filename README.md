# backslashart.org

Backslash Art website.

# Changes from Previous Rep

- Update to Jekyll 4.2.2
- Update to Ruby 3.1.2
- Moved content pages to `_pages`
- Fixed 404 page
- Tested Netlify Deploy

# Making Edits

1. Navigate to the repo on Github
2. From the `Code` button dropdown choose `Codespaces` > `Create Codespace`

   This should open a new browser tab with VS Code running in a "codespace". The process hung for me, but a browser reload quickly fixed it.

3. Make some edits

   A good place to make some test edits is `_pages/test.md`

4. Commit your edits

5. Netlify should see your commit and rebuild and publish your changes.

   See your changes at https://backslashart.netlify.app/
   
   You can also work in a branch if you want to preview your changes without publishing to the main site.



# Build and Run Locally

This website is built with Jekyll.

```bash
bundle exec jekyll serve
```
