# EQ-5D-5L Thai Interpreter

A static, browser-only website for calculating the Thai EQ-5D-5L index value from a five-dimension health profile and a self-rated EQ VAS score.

## Features
- Select one level from 1–5 for all 5 EQ-5D-5L dimensions using radio cards
- Enter and/or slide EQ VAS from 0–100 in the browser
- Validate missing answers and out-of-range VAS values before calculation
- Calculate the Thai EQ-5D-5L index using the published rounded decrement weights for Thailand
- Display the health state profile, index value, VAS score, dimension detail table, and individualized summary
- Clear the form and results without transmitting any health information to a server

## GitHub Pages deployment
1. Push this repository to GitHub.
2. Open the repository in GitHub.
3. Go to Settings → Pages.
4. Under Build and deployment, choose:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
5. Save.
6. GitHub Pages will provide a public URL similar to:
   `https://<username>.github.io/<repository-name>/`

## Local use
Open `index.html` directly in a browser or serve the repository with any static file server.

## Calculation method
This prototype uses the published rounded Thai EQ-5D-5L decrement weights reported in the literature and computes:

Index = 1 − sum of decrements for the selected 5 dimensions

The coefficients are rounded to three decimal places and used exactly as published for the Thailand value set. This implementation is performed entirely in the browser; no health-state data are transmitted to any backend or external service.

## Test cases
- 11111 → Index 1.000
- 21232 → Index 0.751
- 11121 → Index 0.944

## References
- Pattanaphesaj J, et al. The EQ-5D-5L valuation study in Thailand. Expert Review of Pharmacoeconomics & Outcomes Research. 2018;18(5):551–558.
  https://doi.org/10.1080/14737167.2018.1494574
- EuroQol Research Foundation. EQ-5D-5L information and user support.
  https://euroqol.org/information-and-support/
- Thai EQ-5D-5L decrement weights are applied in the browser using the published rounded coefficients for levels 2–5 from the Thailand value set.

## Notes
- This tool is for educational and demonstration purposes and is not a clinical diagnosis tool.
- The website does not store or transmit personal health data.
- It is designed for static GitHub Pages deployment without backend services or databases.
