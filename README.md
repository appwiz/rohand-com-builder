# rohand-com-builder
Automated workflow to build [rohand.com](https://rohand.com/).

## Workflow
1. Checkout and build appwiz/hn-cli
2. Run appwiz/hn-cli and save output to hn-favs.json
3. Checkout and build appwiz/gh-cli
4. Run appwiz/gh-cli and save output to gh-links.json
7. Merge hn-favs.json and gs-links.json
8. Remove duplicates
9. Sort alphabetically
10. Generate canonical slugs for each link
11. Checkout appwiz/appwiz.github.io
12. For each slug,
  1. if a page for a slug does not exist, then create a new page from the page template
  2. update the index page with the new slug in the appropriate spot
13. Update the last generated timestamp in the index page
