# BadgeKeep interview research site

A small, static, self-serve research survey for UK Blue Badge holders and carers. It is independent product research, not GOV.UK or a council service.

## Wire up Formspree

1. Create a form at [Formspree](https://formspree.io/).
2. Copy the form ID from the Formspree endpoint.
3. In `index.html`, replace `FORM_ID_PLACEHOLDER` in the form action with that ID:
   ```html
   action="https://formspree.io/f/your-form-id"
   ```
4. Keep the `_subject` and `_next` hidden fields. The relative `_next` value sends respondents to `thank-you.html` after a successful submission.
5. In Formspree, check the notification and spam-protection settings before sharing the page. Do not collect badge numbers, National Insurance numbers, medical details or documents.

## Enable GitHub Pages

1. Put `index.html`, `thank-you.html` and this `README.md` in the root of a GitHub repository (or a folder you will publish).
2. Commit and push the files to the branch you want to publish, usually `main`.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select the publishing branch and the `/ (root)` folder, then select **Save**.
5. Wait for the Pages deployment, then open the URL shown in the Pages settings. Test both the survey page and a Formspree submission; GitHub Pages itself only serves the static files.

If the repository is a project site, Formspree's relative redirect to `thank-you.html` will resolve within that project site. If you later change the thank-you page location, update the `_next` value too.
