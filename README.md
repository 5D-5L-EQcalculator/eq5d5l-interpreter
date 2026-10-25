# EQ-5D-5L Thai Interpreter

A static, browser-only website for calculating the Thai EQ-5D-5L index value from a five-dimension health profile and a self-rated EQ VAS score.

## Features
- Select level 1–5 for all 5 EQ-5D-5L dimensions
- Enter and/or slide EQ VAS from 0–100
- Calculate the Thai EQ-5D-5L index value locally in the browser
- Display the profile code, index value, VAS score, and dimension detail table
- Clear form and recalculate without sending any data to a server

## Deployment on GitHub Pages
1. Push this repository to GitHub.
2. In GitHub, open the repository.
3. Go to Settings → Pages.
4. Under Build and deployment, choose:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
5. Save.
6. GitHub Pages will provide a public URL such as:
   https://<username>.github.io/<repository-name>/

## Local use
Open `index.html` directly in a browser or host the repository via a static server.

## Calculation method
This prototype uses the rounded Thai EQ-5D-5L decrement weights reported in the literature and computes:

Index = 1 − sum of decrements for the selected 5 dimensions

The implementation is performed entirely in the browser with JavaScript; no health-state data are transmitted to any backend or external service.

## References
- Roudijk B, Ludwig K, Devlin N. EQ-5D-5L Value Set Summaries, Table 4.29: Thailand. NCBI Bookshelf.
  https://www.ncbi.nlm.nih.gov/books/NBK589305/table/ch4.Tab29/
- Pattanaphesaj J, et al. The EQ-5D-5L valuation study in Thailand. Expert Review of Pharmacoeconomics & Outcomes Research. 2018;18(5):551–558.
  https://doi.org/10.1080/14737167.2018.1494574
- EuroQol Research Foundation. FAQ and digital questionnaire support.
  https://euroqol.org/information-and-support/user-support/faqs/

## Notes
- This is an academic technical prototype.
- The calculation is based on published rounded Thai decrement values and is intended for demonstration and educational use.
- The website does not store or transmit health responses; it runs locally in the browser.
- It is not a clinical diagnosis tool.
